# 📊 Limechat Database Schema Documentation

> **Generated:** 2025-11-11 at 15:49:04
> **Total Tables:** 1

## 📑 Table of Contents

- [accounts](#accounts)

---

## accounts

> **Model:** `Account`

### 📝 Table Description

# Accounts Table

The **Accounts** table serves as the central tenant/organization configuration entity in the system, representing each customer company or workspace using the platform. It stores core business settings including billing information (billing_email, currency), feature flags, localization preferences (locale), conversation management rules (auto_resolve_duration, assignment_logic), and UI customization options (hide_all_tab, hide_bot_conversations). With 74 relationships (primarily has_many), this table acts as the top-level parent entity that owns and orchestrates all other resources including conversations, users (agents), contacts (customers), and inboxes. Common use cases include tenant-level feature toggling, billing operations, workspace configuration management, and enforcing account-wide policies like contact masking and tagging requirements.

**Key Relationships:** Parent to conversations, users, contacts, inboxes, and other workspace resources  
**Primary Configuration Areas:** Billing, features, localization, conversation handling, UI preferences  
**Note:** Uses soft deletion (deleted_at) and includes enterprise-specific settings (is_enterprise, grace_extension)

### 📋 Columns

| Column | Type | Length | Nullable | Default | Enum Values | Validations | Constraints | Description |
|--------|------|--------|----------|---------|-------------|-------------|-------------|-------------|
| **id** 🔑 | `integer` | - | ✗ | - | - | - | NOT NULL, PRIMARY KEY | **Primary identifier for account records. This is a sequentially increasing integer that uniquely identifies each account entry and serves as the PRIMARY KEY of the accounts table.** |
| assignment_logic | `integer` | - | ✗ | `load_balanced` | round_robin(0), load_balanced(1) | - | NOT NULL | ## assignment_logic

Determines the algorithm used for automatically assigning conversations to agents within the account. Accepts two strategies: `round_robin` (distributes conversations sequentially across available agents) or `load_balanced` (assigns based on current agent workload), with `load_balanced` as the default method. |
| auto_resolve_duration | `integer` | - | ✓ | - | - | numericality | - | **auto_resolve_duration** (integer, nullable)

Duration in days after which an open conversation is automatically resolved without agent interaction. Must be at least 1 day when enabled; when null, auto-resolution is disabled for the account. |
| billing_email | `string` | - | ✓ | - | - | - | - | **billing_email**

Email address designated for receiving billing-related communications and invoices for the account. This field is optional and may differ from the primary account contact email, allowing organizations to route financial correspondence to accounting departments or specific billing contacts. |
| contact_masking | `boolean` | - | ✓ | `FALSE` | - | - | - | ## contact_masking

**Description:** Indicates whether contact (customer) personal information is masked or hidden for privacy purposes in this account. When enabled (TRUE), sensitive customer data such as phone numbers, email addresses, or other identifying information will be obscured from view.

**Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| currency | `text` | - | ✓ | `INR` | - | - | - | **currency**

`text` | Nullable | Default: `INR`

Specifies the currency code for the account's financial transactions and monetary values. Defaults to INR (Indian Rupees) when not explicitly set, supporting multi-currency account operations. |
| deleted_at | `datetime` | - | ✓ | - | - | - | - | ## deleted_at

**Type:** datetime | **Nullable:** True

**Description:**
UTC timestamp indicating when the account was soft-deleted. A NULL value indicates the account is active, while a populated timestamp marks the account as deleted and typically excludes it from standard queries (soft delete pattern). |
| domain | `string` | 100 | ✓ | - | - | - | - | ## domain

**Description:** Stores the domain name or web address associated with the account, typically representing the customer's organization website or email domain. This optional field helps identify and categorize accounts by their online presence.

**Data Format:** String up to 100 characters (e.g., "example.com", "subdomain.company.org") |
| enforce_tagging | `boolean` | - | ✓ | `FALSE` | - | - | - | ## enforce_tagging

**Description:** Determines whether tagging is mandatory for conversations within the account. When set to TRUE, agents must apply tags before closing or completing conversations; defaults to FALSE allowing optional tagging.

**Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| feature_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | ## feature_flags

**Type:** integer | **Nullable:** No | **Default:** 0

**Description:** A bitmask integer storing boolean feature toggles for the account, where each bit position represents an enabled/disabled feature flag. The default value of 0 indicates all features are disabled by default, and specific features are enabled by setting corresponding bit values. |
| grace_added_on | `datetime` | - | ✓ | - | - | - | - | ## grace_added_on

**Description:** UTC timestamp indicating when a grace period was granted to the account. This field remains null if no grace period has been applied to the account.

**Data Format:** datetime (UTC)

**Business Context:** Tracks the specific date and time when account grace period benefits were activated, typically used for managing temporary extensions or trial periods beyond normal account limits. |
| grace_extension | `boolean` | - | ✓ | `FALSE` | - | - | - | **grace_extension**

`boolean` | Nullable | Default: `FALSE`

Indicates whether the account has been granted a grace period extension, typically allowing continued access or delayed enforcement of account restrictions (e.g., suspension, feature limitations) beyond the standard policy timeframe. When set to TRUE, the account operates under extended terms that override default expiration or enforcement rules. |
| hide_all_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | **hide_all_tab**

Boolean flag indicating whether the "All" tab should be hidden from view in the account's interface. When set to TRUE, the tab displaying all conversations/items will be concealed; defaults to FALSE to show the tab by default. |
| hide_all_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | ## hide_all_tab_for_supervisor

**Type:** boolean | **Nullable:** Yes | **Default:** FALSE

**Description:**

Controls visibility of the "All" tab for users with supervisor role. When set to TRUE, supervisors will not see the "All" tab in their interface, limiting their view to only assigned or filtered conversations/items.

**Business Context:**

This setting enables account-level configuration to restrict supervisors' access to viewing all conversations or tickets, useful for enforcing role-based access control and data privacy requirements within the help desk system. |
| hide_bot_conversations | `boolean` | - | ✓ | `FALSE` | - | - | - | **hide_bot_conversations**

Boolean flag indicating whether conversations handled solely by bots should be hidden from the account's view. When set to TRUE, filters out bot-only conversations from the account's conversation list, allowing agents to focus on human-assisted interactions. |
| hide_out_of_stock | `boolean` | - | ✓ | `FALSE` | - | - | - | ## hide_out_of_stock

**Type:** boolean | **Nullable:** Yes | **Default:** FALSE

**Description:**

Determines whether out-of-stock products should be hidden from display in the account's storefront or catalog. When set to TRUE, products with zero inventory will be automatically concealed from customer view; when FALSE (default), out-of-stock items remain visible but are marked as unavailable. |
| hide_queued_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | ## hide_queued_tab

**Description:** Controls the visibility of the queued conversations tab for the account. When set to TRUE, the queued tab is hidden from the account's interface; defaults to FALSE to display the tab by default.

**Business Context:** This is an account-level UI preference setting that allows customization of which conversation tabs are visible to agents, specifically managing whether conversations in a queued state are shown. |
| hide_queued_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | ## hide_queued_tab_for_supervisor

**Description:** Controls whether the queued conversations tab is hidden from supervisor users in the dashboard interface. When set to TRUE, supervisors for this account will not see the queued tab; defaults to FALSE to display the tab by default.

**Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| is_enterprise | `boolean` | - | ✓ | `FALSE` | - | - | - | **is_enterprise**

`boolean` | Nullable | Default: `FALSE`

Indicates whether the account is classified as an enterprise-tier account. This flag is used to distinguish enterprise customers from standard accounts, typically affecting feature availability, pricing tier, and support level access across the platform. |
| locale | `integer` | - | ✓ | `en` | see enum details | - | - | ## locale

**Description:** Stores the preferred language setting for the account as an integer code mapped from ISO 639-1 language codes defined in LANGUAGES_CONFIG. Defaults to English ('en') and is used to determine the interface language and localized content for the account. |
| name | `string` | - | ✗ | - | - | required | NOT NULL | ## name

**Description:** The account name or display identifier. This field is required and serves as the primary label for identifying and referencing the account throughout the system.

**Data Requirements:** Non-nullable string field with presence validation enforced. |
| on_grace_period | `boolean` | - | ✓ | `FALSE` | - | - | - | ## on_grace_period

**Description:** Indicates whether the account is currently in a grace period status, typically following subscription expiration or payment failure, during which service access may continue while awaiting resolution. Defaults to FALSE when not applicable or when the account is in good standing.

**Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| on_shopify_custom_plan | `boolean` | - | ✓ | `FALSE` | - | - | - | ## on_shopify_custom_plan

**Description:** Indicates whether the account is subscribed to a custom Shopify pricing plan rather than a standard tier. Defaults to FALSE; when TRUE, signifies the account has negotiated custom terms with Shopify. |
| partner_billed | `boolean` | - | ✗ | `FALSE` | - | - | NOT NULL | ## partner_billed

**Description:** Indicates whether the account has been billed through a partner relationship. When set to TRUE, signifies that billing is handled via a partner rather than direct billing; defaults to FALSE for standard direct-billed accounts.

**Type:** boolean | **Nullable:** No | **Default:** FALSE |
| password | `string` | - | ✓ | - | - | - | - | ## password

**Description:** Stores the hashed/encrypted password credential for account authentication. This field is nullable to support accounts using alternative authentication methods (e.g., SSO, OAuth) that don't require traditional password-based login.

**Data Format:** String (hashed value recommended for security) |
| payment_pending | `boolean` | - | ✓ | `FALSE` | - | - | - | ## payment_pending

**Description:** Indicates whether there is an outstanding payment action required for the account. Defaults to FALSE; when TRUE, signifies that a payment transaction is awaiting processing or completion.

**Data Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| preferred_billing_currency | `integer` | - | ✓ | `USD` | INR(0), USD(1) | - | - | ## preferred_billing_currency

**Description:** Specifies the account's preferred currency for billing transactions and invoicing. Accepts integer-mapped enum values (INR, USD), with USD as the default currency when not explicitly set.

**Business Context:** This field determines the currency in which the account will be billed for services, allowing multi-currency support across different geographical regions. |
| settings_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | **settings_flags**

`integer` | NOT NULL | Default: 0

Stores bitwise flags representing various account-level configuration settings and feature toggles. Each bit position represents a specific boolean setting, allowing multiple configuration options to be efficiently stored in a single integer field. |
| shopify_access_token | `string` | - | ✓ | - | - | - | - | ## shopify_access_token

**Description:** OAuth access token used to authenticate and authorize API requests to the associated Shopify store. This token enables secure integration with Shopify services for the account and should be treated as sensitive credential data.

**Data Format:** String (nullable) - Standard Shopify OAuth token format |
| shopify_app_reinstalled | `boolean` | - | ✓ | `FALSE` | - | - | - | ## shopify_app_reinstalled

**Description:** Boolean flag indicating whether the Shopify app has been reinstalled for this account. Defaults to FALSE and is set to TRUE when the account reinstalls the app after a previous uninstallation. |
| shopify_country_code | `string` | - | ✓ | - | - | - | - | ## shopify_country_code

**Type:** string | **Nullable:** Yes

**Description:** Stores the two-letter ISO country code associated with the account's Shopify store location (e.g., "US", "CA", "GB"). This field is populated when the account is integrated with Shopify and is used to identify the geographic region of the store for localization and analytics purposes. |
| shopify_country_name | `string` | - | ✓ | - | - | - | - | **shopify_country_name**

Type: string | Nullable: True

**Description:**

Stores the country name associated with the account's Shopify store location or primary business address. This field is nullable as it only applies to accounts with Shopify integration enabled. |
| shopify_deleted | `boolean` | - | ✓ | `FALSE` | - | - | - | ## shopify_deleted

**Description:** Indicates whether the account has been deleted from Shopify. When set to TRUE, the account is marked as removed from the Shopify platform; defaults to FALSE for active accounts.

**Data Type:** Boolean | **Nullable:** Yes | **Default:** FALSE |
| shopify_store_url | `string` | - | ✓ | - | - | - | - | ## shopify_store_url

**Description:** Stores the Shopify store URL associated with the account, used to identify and link the account to a specific Shopify merchant store. This field is optional and will be populated only for accounts that have integrated with Shopify.

**Format:** String containing the full URL (e.g., "https://store-name.myshopify.com") |
| source | `string` | - | ✓ | - | - | - | - | ## source

**Description:** Indicates the origin or channel through which the account was created or acquired (e.g., website signup, API integration, mobile app, referral). This nullable field helps track account acquisition channels for analytics and attribution purposes. |
| support_email | `string` | 100 | ✓ | - | - | - | - | **support_email**

*string, Length: 100, Nullable: True*

Email address designated for customer support inquiries associated with the account. This field is optional and may be used to route support-related communications or identify the primary support contact point for the account. |
| template_last_synced_at | `datetime` | - | ✓ | - | - | - | - | ## template_last_synced_at

**Description:** Timestamp (UTC) indicating when the account's templates were last synchronized. This nullable field tracks the most recent synchronization event for template-related data associated with the account, remaining NULL if no synchronization has occurred. |
| username | `string` | - | ✓ | - | - | - | - | ## username

**Description:** The login identifier or display name for the agent associated with the account. This field is nullable to accommodate accounts that may not have an assigned username at creation time.

**Business Context:** Used to identify and authenticate agents (users) across the system, particularly when tracking agent interactions in conversations and analytics. |
| website_url | `string` | - | ✓ | - | - | - | - | **website_url**

The URL of the website or web property associated with the account. This field is optional and stores the primary web address where the account's business or organization can be accessed online. |
| created_at | `datetime` | - | ✗ | - | - | - | NOT NULL | **created_at**

*Type: datetime | Nullable: False*

UTC timestamp indicating when the account record was initially created in the system. This serves as an immutable audit field to track account origination and is automatically set upon account registration. |
| updated_at | `datetime` | - | ✗ | - | - | - | NOT NULL | **updated_at**

`datetime` | NOT NULL

UTC timestamp indicating when the account record was last modified. This field is automatically updated whenever any changes are made to the account, enabling tracking of the most recent modification time for audit and synchronization purposes. |
| customer_id | `string` | - | ✓ | - | - | - | - | **customer_id**

Unique identifier linking the account to the corresponding customer (contact). References the customer's ID to establish the account ownership relationship, stored as a string value that may be null for accounts not yet associated with a customer. |

#### 🏷️ Enum Details

**assignment_logic:**
```ruby
round_robin: 0
load_balanced: 1
```

**preferred_billing_currency:**
```ruby
INR: 0
USD: 1
```

**locale:**
```ruby
[External: LANGUAGES_CONFIG.to_h { |key, val| [val[:iso_639_1_code], key] }]
```

#### 🚩 Flags (settings_flags)

- 1 => custom_email_domain_enabled

### ✅ Validations

| Field | Rule |
|-------|------|
| `name` | presence: true |
| `auto_resolve_duration` | numericality: { greater_than_or_equal_to: 1, allow_nil: true } |

### 🔍 Indexes

| Index Name | Columns | Unique |
|------------|---------|--------|
| index_accounts_on_deleted_at | `deleted_at` | ✗ |
| index_accounts_on_updated_at | `updated_at` | ✗ |

### 🔗 Foreign Keys

| Constraint | Column | References | Type |
|------------|--------|------------|------|
| fk_account_users_accounts | `account_id` | `account_users.account_id` → `accounts.id` | Implicit |
| fk_acl_accounts | `account_id` | `acl.account_id` → `accounts.id` | Implicit |
| fk_agent_analytics_accounts | `account_id` | `agent_analytics.account_id` → `accounts.id` | Implicit |
| fk_agent_bot_inboxes_accounts | `account_id` | `agent_bot_inboxes.account_id` → `accounts.id` | Implicit |
| fk_api_accounts | `account_id` | `api.account_id` → `accounts.id` | Implicit |
| fk_article_accounts | `account_id` | `article.account_id` → `accounts.id` | Implicit |
| fk_attendances_accounts | `account_id` | `attendances.account_id` → `accounts.id` | Implicit |
| fk_automation_rules_accounts | `account_id` | `automation_rules.account_id` → `accounts.id` | Implicit |
| fk_broadcasts_accounts | `account_id` | `broadcasts.account_id` → `accounts.id` | Implicit |
| fk_canned_responses_accounts | `account_id` | `canned_responses.account_id` → `accounts.id` | Implicit |
| fk_category_accounts | `account_id` | `category.account_id` → `accounts.id` | Implicit |
| fk_chatapi_accounts | `account_id` | `chatapi.account_id` → `accounts.id` | Implicit |
| fk_clevertap_accounts | `account_id` | `clevertap.account_id` → `accounts.id` | Implicit |
| fk_contacts_accounts | `account_id` | `contacts.account_id` → `accounts.id` | Implicit |
| fk_conversation_analytics_accounts | `account_id` | `conversation_analytics.account_id` → `accounts.id` | Implicit |
| fk_conversation_trackers_accounts | `account_id` | `conversation_trackers.account_id` → `accounts.id` | Implicit |
| fk_conversations_accounts | `account_id` | `conversations.account_id` → `accounts.id` | Implicit |
| fk_crm_accounts | `account_id` | `crm.account_id` → `accounts.id` | Implicit |
| fk_csat_survey_responses_accounts | `account_id` | `csat_survey_responses.account_id` → `accounts.id` | Implicit |
| fk_custom_fields_accounts | `account_id` | `custom_fields.account_id` → `accounts.id` | Implicit |
| fk_email_accounts | `account_id` | `email.account_id` → `accounts.id` | Implicit |
| fk_exotelvoice_accounts | `account_id` | `exotelvoice.account_id` → `accounts.id` | Implicit |
| fk_exotelwebrtcvoice_accounts | `account_id` | `exotelwebrtcvoice.account_id` → `accounts.id` | Implicit |
| fk_facebook_posts_accounts | `account_id` | `facebook_posts.account_id` → `accounts.id` | Implicit |
| fk_facebookpage_accounts | `account_id` | `facebookpage.account_id` → `accounts.id` | Implicit |
| fk_freshchat_accounts | `account_id` | `freshchat.account_id` → `accounts.id` | Implicit |
| fk_gupshup_accounts | `account_id` | `gupshup.account_id` → `accounts.id` | Implicit |
| fk_gupshupenterprise_accounts | `account_id` | `gupshupenterprise.account_id` → `accounts.id` | Implicit |
| fk_hook_accounts | `account_id` | `hook.account_id` → `accounts.id` | Implicit |
| fk_ics_accounts | `account_id` | `ics.account_id` → `accounts.id` | Implicit |
| fk_inboxes_accounts | `account_id` | `inboxes.account_id` → `accounts.id` | Implicit |
| fk_infobip_accounts | `account_id` | `infobip.account_id` → `accounts.id` | Implicit |
| fk_karix_accounts | `account_id` | `karix.account_id` → `accounts.id` | Implicit |
| fk_karixrcm_accounts | `account_id` | `karixrcm.account_id` → `accounts.id` | Implicit |
| fk_knowlarity_accounts | `account_id` | `knowlarity.account_id` → `accounts.id` | Implicit |
| fk_labels_accounts | `account_id` | `labels.account_id` → `accounts.id` | Implicit |
| fk_maytapi_accounts | `account_id` | `maytapi.account_id` → `accounts.id` | Implicit |
| fk_message_analytics_accounts | `account_id` | `message_analytics.account_id` → `accounts.id` | Implicit |
| fk_message_charges_accounts | `account_id` | `message_charges.account_id` → `accounts.id` | Implicit |
| fk_messages_accounts | `account_id` | `messages.account_id` → `accounts.id` | Implicit |
| fk_myoperatorvoice_accounts | `account_id` | `myoperatorvoice.account_id` → `accounts.id` | Implicit |
| fk_netcore_accounts | `account_id` | `netcore.account_id` → `accounts.id` | Implicit |
| fk_notification_settings_accounts | `account_id` | `notification_settings.account_id` → `accounts.id` | Implicit |
| fk_outbound_bots_accounts | `account_id` | `outbound_bots.account_id` → `accounts.id` | Implicit |
| fk_portal_accounts | `account_id` | `portal.account_id` → `accounts.id` | Implicit |
| fk_shopify_scheduled_account_deletion_accounts | `account_id` | `shopify_scheduled_account_deletion.account_id` → `accounts.id` | Implicit |
| fk_shopify_webhooks_accounts | `account_id` | `shopify_webhooks.account_id` → `accounts.id` | Implicit |
| fk_sinch_accounts | `account_id` | `sinch.account_id` → `accounts.id` | Implicit |
| fk_sla_policies_accounts | `account_id` | `sla_policies.account_id` → `accounts.id` | Implicit |
| fk_sla_trackers_accounts | `account_id` | `sla_trackers.account_id` → `accounts.id` | Implicit |
| fk_subscriptions_accounts | `account_id` | `subscriptions.account_id` → `accounts.id` | Implicit |
| fk_teams_accounts | `account_id` | `teams.account_id` → `accounts.id` | Implicit |
| fk_telegram_bots_accounts | `account_id` | `telegram_bots.account_id` → `accounts.id` | Implicit |
| fk_templates_accounts | `account_id` | `templates.account_id` → `accounts.id` | Implicit |
| fk_threesixtydialog_accounts | `account_id` | `threesixtydialog.account_id` → `accounts.id` | Implicit |
| fk_transaction_ledgers_accounts | `account_id` | `transaction_ledgers.account_id` → `accounts.id` | Implicit |
| fk_trustsignal_accounts | `account_id` | `trustsignal.account_id` → `accounts.id` | Implicit |
| fk_twiliosms_accounts | `account_id` | `twiliosms.account_id` → `accounts.id` | Implicit |
| fk_twitterprofile_accounts | `account_id` | `twitterprofile.account_id` → `accounts.id` | Implicit |
| fk_twofactor_accounts | `account_id` | `twofactor.account_id` → `accounts.id` | Implicit |
| fk_valuefirst_accounts | `account_id` | `valuefirst.account_id` → `accounts.id` | Implicit |
| fk_wallet_accounts | `account_id` | `wallet.account_id` → `accounts.id` | Implicit |
| fk_wati_accounts | `account_id` | `wati.account_id` → `accounts.id` | Implicit |
| fk_webengage_accounts | `account_id` | `webengage.account_id` → `accounts.id` | Implicit |
| fk_webhook_watchers_accounts | `account_id` | `webhook_watchers.account_id` → `accounts.id` | Implicit |
| fk_webhooks_accounts | `account_id` | `webhooks.account_id` → `accounts.id` | Implicit |
| fk_webwidget_accounts | `account_id` | `webwidget.account_id` → `accounts.id` | Implicit |
| fk_whatsapp_messages_accounts | `account_id` | `whatsapp_messages.account_id` → `accounts.id` | Implicit |
| fk_whatsappclevertap_accounts | `account_id` | `whatsappclevertap.account_id` → `accounts.id` | Implicit |
| fk_whatsappcloudapi_accounts | `account_id` | `whatsappcloudapi.account_id` → `accounts.id` | Implicit |
| fk_working_hours_accounts | `account_id` | `working_hours.account_id` → `accounts.id` | Implicit |
| fk_zoko_accounts | `account_id` | `zoko.account_id` → `accounts.id` | Implicit |

### 🔄 Relationships

#### Belongs To

| Relationship | Target Model | Dependent | Foreign Key |
|--------------|--------------|-----------|-------------|
| - | - | - | - |

#### Has One

| Relationship | Target Model | Dependent | Foreign Key |
|--------------|--------------|-----------|-------------|
| `web_engage` | `::Integrations::WebEngage` | `destroy` | `account_id` |
| `clever_tap` | `::Integrations::CleverTap` | `destroy` | `account_id` |
| `crm` | `::Integrations::Crm` | `destroy` | `account_id` |
| `shopify_scheduled_account_deletion` | `Shopify_scheduled_account_deletion` | `destroy` | `account_id` |
| `wallet` | `Wallet` | `destroy` | `account_id` |

#### Has Many

| Relationship | Target Model | Dependent | Foreign Key |
|--------------|--------------|-----------|-------------|
| `account_users` | `Account_users` | `destroy` | `account_id` |
| `attendances` | `Attendances` | `destroy` | `account_id` |
| `agent_bot_inboxes` | `Agent_bot_inboxes` | `destroy` | `account_id` |
| `outbound_bots` | `Outbound_bots` | `destroy` | `account_id` |
| `broadcasts` | `Broadcasts` | `destroy` | `account_id` |
| `csat_survey_responses` | `Csat_survey_responses` | `destroy` | `account_id` |
| `users` | `Users` | `-` | `(through account_users)` |
| `inboxes` | `Inboxes` | `destroy_async` | `account_id` |
| `conversations` | `Conversations` | `destroy` | `account_id` |
| `conversation_analytics` | `Conversation_analytics` | `destroy` | `account_id` |
| `message_analytics` | `Message_analytics` | `destroy` | `account_id` |
| `agent_analytics` | `Agent_analytics` | `destroy` | `account_id` |
| `messages` | `Messages` | `destroy` | `account_id` |
| `contacts` | `Contacts` | `destroy` | `account_id` |
| `telegram_bots` | `Telegram_bots` | `destroy` | `account_id` |
| `facebook_pages` | `::Channel::FacebookPage` | `destroy` | `account_id` |
| `twilio_sms` | `::Channel::TwilioSms` | `destroy` | `account_id` |
| `chat_apis` | `::Channel::ChatApi` | `destroy` | `account_id` |
| `maytapis` | `::Channel::Maytapi` | `destroy` | `account_id` |
| `acls` | `::Channel::Acl` | `destroy` | `account_id` |
| `freshchats` | `::Channel::Freshchat` | `destroy` | `account_id` |
| `two_factors` | `::Channel::TwoFactor` | `destroy` | `account_id` |
| `watis` | `::Channel::Wati` | `destroy` | `account_id` |
| `value_firsts` | `::Channel::ValueFirst` | `destroy` | `account_id` |
| `zokos` | `::Channel::Zoko` | `destroy` | `account_id` |
| `gupshups` | `::Channel::Gupshup` | `destroy` | `account_id` |
| `gupshup_enterprises` | `::Channel::GupshupEnterprise` | `destroy` | `account_id` |
| `ics` | `::Channel::Ics` | `destroy` | `account_id` |
| `infobip` | `::Channel::Infobip` | `destroy` | `account_id` |
| `netcores` | `::Channel::Netcore` | `destroy` | `account_id` |
| `sinch` | `::Channel::Sinch` | `destroy` | `account_id` |
| `karixes` | `::Channel::Karix` | `destroy` | `account_id` |
| `karixrcms` | `::Channel::Karixrcm` | `destroy` | `account_id` |
| `valuefirsts` | `::Channel::Valuefirst` | `destroy` | `account_id` |
| `trust_signals` | `::Channel::TrustSignal` | `destroy` | `account_id` |
| `whatsapp_clever_tap` | `::Channel::WhatsappCleverTap` | `destroy` | `account_id` |
| `twitter_profiles` | `::Channel::TwitterProfile` | `destroy` | `account_id` |
| `web_widgets` | `::Channel::WebWidget` | `destroy` | `account_id` |
| `email_channels` | `::Channel::Email` | `destroy` | `account_id` |
| `knowlarity_channels` | `::Channel::Knowlarity` | `destroy` | `account_id` |
| `exotel_voice_channels` | `::Channel::ExotelVoice` | `destroy` | `account_id` |
| `my_operator_voice_channels` | `::Channel::MyOperatorVoice` | `destroy` | `account_id` |
| `exotel_webrtc_voice_channels` | `::Channel::ExotelWebrtcVoice` | `destroy` | `account_id` |
| `api_channels` | `::Channel::Api` | `destroy` | `account_id` |
| `whatsapp_cloud_apis` | `::Channel::WhatsappCloudApi` | `destroy` | `account_id` |
| `three_sixty_dialogs` | `::Channel::ThreeSixtyDialog` | `destroy` | `account_id` |
| `canned_responses` | `Canned_responses` | `destroy` | `account_id` |
| `templates` | `Templates` | `destroy` | `account_id` |
| `webhooks` | `Webhooks` | `destroy` | `account_id` |
| `labels` | `Labels` | `destroy` | `account_id` |
| `notification_settings` | `Notification_settings` | `destroy` | `account_id` |
| `whatsapp_messages` | `Whatsapp_messages` | `destroy` | `account_id` |
| `hooks` | `Integrations::Hook` | `destroy` | `account_id` |
| `working_hours` | `Working_hours` | `destroy` | `account_id` |
| `kbase_portals` | `::Kbase::Portal` | `destroy` | `account_id` |
| `kbase_categories` | `::Kbase::Category` | `destroy` | `account_id` |
| `kbase_articles` | `::Kbase::Article` | `destroy` | `account_id` |
| `teams` | `Teams` | `destroy` | `account_id` |
| `subscriptions` | `Subscriptions` | `destroy` | `account_id` |
| `shopify_webhooks` | `Shopify_webhooks` | `destroy` | `account_id` |
| `automation_rules` | `Automation_rules` | `destroy` | `account_id` |
| `webhook_watchers` | `Webhook_watchers` | `destroy` | `account_id` |
| `conversation_trackers` | `Conversation_trackers` | `destroy` | `account_id` |
| `facebook_posts` | `Facebook_posts` | `destroy` | `account_id` |
| `custom_fields` | `Custom_fields` | `destroy` | `account_id` |
| `sla_policies` | `Sla_policies` | `destroy` | `account_id` |
| `sla_trackers` | `Sla_trackers` | `destroy` | `account_id` |
| `message_charges` | `Message_charges` | `destroy` | `account_id` |
| `transaction_ledgers` | `Transaction_ledgers` | `destroy` | `account_id` |

---

## 📈 Summary Statistics

| Metric | Count |
|--------|------:|
| Total Tables | 1 |
| Total Columns | 42 |
| Total Indexes | 2 |
| Total Foreign Keys | 73 |
| Total Relationships | 74 |

### Largest Tables (by column count)

| Table | Columns | Relationships |
|-------|--------:|--------------:|
| accounts | 42 | 74 |

