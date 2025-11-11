# 📊 Limechat Database Schema Documentation

> **Generated:** 2025-11-11 at 16:09:16
> **Total Tables:** 1

## 📑 Table of Contents

- [accounts](#accounts)

---

## accounts

> **Model:** `Account`

### 📝 Table Description

## Accounts Table

The **Accounts** table serves as the primary tenant/organization entity in the multi-tenant helpdesk system, representing each customer company or workspace that uses the platform. Each account contains configuration settings for conversation management (assignment logic, auto-resolution, contact masking), billing information (currency, billing email, enterprise status), UI preferences (tab visibility, conversation filtering), and feature flags that control platform capabilities. 

This is a central hub table with **74 relationships** (primarily has_many), connecting to virtually all other entities in the system including users (agents), contacts (customers), conversations, inboxes, and analytics. Common use cases include tenant isolation, feature access control, billing management, and applying account-level configurations to conversation routing and display logic. The `deleted_at` column supports soft deletion for account deactivation.

**Note:** In this system, *contact* refers to the customer, and *user* refers to an agent.

### 📋 Columns

| Column | Type | Length | Nullable | Default | Enum Values | Validations | Constraints | Description |
|--------|------|--------|----------|---------|-------------|-------------|-------------|-------------|
| **id** 🔑 | `integer` | - | ✗ | - | - | - | NOT NULL, PRIMARY KEY | **ID** - A sequentially increasing integer that uniquely identifies each account record and serves as the PRIMARY KEY of the accounts table. This is a non-nullable unique identifier used to establish relationships with the table's 74 foreign key connections. |
| assignment_logic | `integer` | - | ✗ | `load_balanced` | round_robin(0), load_balanced(1) | - | NOT NULL | assignment_logic Determines the method used to distribute incoming conversations to available agents within the account. Can be set to `round_robin` (sequential distribution to each agent) or `load_balanced` (distribution based on current agent workload), with `load_balanced` as the default strat... |
| auto_resolve_duration | `integer` | - | ✓ | - | - | numericality | - | auto_resolve_duration **Description:** Specifies the duration (in days) after which conversations in this account will be automatically resolved. If set to null, automatic resolution is disabled for the account. **Data Type:** integer \| **Nullable:** Yes \| **Validation:** Must be ≥ 1 day when e... |
| billing_email | `string` | - | ✓ | - | - | - | - | **billing_email** The email address designated to receive billing-related communications and invoices for the account. This field is optional and may differ from the account's primary contact email, allowing organizations to route financial correspondence to accounting departments or billing admi... |
| contact_masking | `boolean` | - | ✓ | `FALSE` | - | - | - | contact_masking **Description:** Indicates whether contact (customer) personal information should be masked or hidden for privacy purposes. When set to TRUE, sensitive customer data associated with this account will be obscured in the system interface and reports. **Technical Details:** Boolean f... |
| currency | `text` | - | ✓ | `INR` | - | - | - | **currency** *text* \| Nullable \| Default: `INR` Specifies the currency code for the account's monetary transactions and balances, defaulting to INR (Indian Rupee) when not explicitly set. This column determines the currency context for all financial calculations and displays associated with the... |
| deleted_at | `datetime` | - | ✓ | - | - | - | - | **deleted_at** Timestamp (UTC) indicating when the account was soft-deleted; NULL value indicates the account is active. Used for soft deletion pattern to maintain data integrity across the 74 related tables while logically removing accounts from active use. |
| domain | `string` | 100 | ✓ | - | - | - | - | **domain** (string, 100, nullable) The domain or website URL associated with the account, typically representing the customer's business website or primary web presence. This field is optional and helps identify the organization's online property linked to their account. |
| enforce_tagging | `boolean` | - | ✓ | `FALSE` | - | - | - | enforce_tagging **Description:** Determines whether tagging is mandatory for conversations or tickets within the account. When set to TRUE, agents must apply appropriate tags before completing certain actions (such as closing conversations); defaults to FALSE to allow optional tagging. |
| feature_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | feature_flags **Type:** integer \| **Nullable:** No \| **Default:** 0 **Description:** A bitmask field storing boolean feature toggles for the account, where each bit position represents a specific feature's enabled/disabled state. The integer value is computed by summing powers of 2 for each ena... |
| grace_added_on | `datetime` | - | ✓ | - | - | - | - | grace_added_on **Description:** UTC timestamp indicating when a grace period was applied to the account. This tracks the specific date and time when account privileges or services were extended beyond the normal expiration, typically used for billing or subscription management purposes. |
| grace_extension | `boolean` | - | ✓ | `FALSE` | - | - | - | grace_extension **Description:** Indicates whether the account has been granted a grace period extension beyond the standard terms. When set to TRUE, this flag typically allows continued access or delayed enforcement of account restrictions (e.g., payment deadlines, feature limitations) for the s... |
| hide_all_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_all_tab **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Controls the visibility of the "All" tab in the account's interface. When set to TRUE, the "All" tab is hidden from view for users associated with this account; defaults to FALSE to display the tab by default. |
| hide_all_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_all_tab_for_supervisor **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Controls visibility of the "All" tab for supervisor-role users in the dashboard interface. When set to TRUE, supervisors will not see the "All" tab that typically displays conversations/ticke... |
| hide_bot_conversations | `boolean` | - | ✓ | `FALSE` | - | - | - | **hide_bot_conversations** Boolean flag indicating whether conversations handled by bots should be hidden from view for this account. When set to TRUE, conversations where bot interactions occurred will be filtered out from the account's conversation displays and analytics; defaults to FALSE to s... |
| hide_out_of_stock | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_out_of_stock **Type:** boolean \| **Nullable:** True \| **Default:** FALSE **Description:** Controls the visibility of out-of-stock products for the account. When set to TRUE, products with zero inventory will be hidden from display; when FALSE (default), out-of-stock items remain visible to... |
| hide_queued_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_queued_tab **Description:** Controls the visibility of the queued conversations tab in the agent dashboard. When set to TRUE, the queued tab is hidden from the account's interface; defaults to FALSE to display the tab by default. |
| hide_queued_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_queued_tab_for_supervisor **Type:** boolean \| **Nullable:** True \| **Default:** FALSE **Description:** Controls the visibility of the queued conversations tab for supervisors in the dashboard interface. When set to TRUE, supervisors will not see the queued tab, restricting their view to ot... |
| is_enterprise | `boolean` | - | ✓ | `FALSE` | - | - | - | is_enterprise **Description:** Indicates whether the account is classified as an enterprise-level account. This boolean flag defaults to FALSE and can be used to differentiate enterprise customers from standard accounts for feature access, billing, or support prioritization purposes. **Type:** bo... |
| locale | `integer` | - | ✓ | `en` | see enum details | - | - | locale **Type:** integer \| **Nullable:** Yes \| **Default:** en **Description:** Specifies the language preference for the account using ISO 639-1 language codes mapped to integer values. The mapping is defined in LANGUAGES_CONFIG, with 'en' (English) as the default language setting. |
| name | `string` | - | ✗ | - | - | required | NOT NULL | accounts.name **Description:** The display name of the account. This is a required, non-nullable string field that serves as the primary identifier for the account throughout the system and is likely referenced across multiple related tables (given the 74 table relationships). **Format:** String ... |
| on_grace_period | `boolean` | - | ✓ | `FALSE` | - | - | - | on_grace_period **Description:** Indicates whether the account is currently in a grace period status, typically allowing continued access to services after subscription expiration or payment issues. Defaults to FALSE when not explicitly set, with NULL values permitted for legacy or special-case a... |
| on_shopify_custom_plan | `boolean` | - | ✓ | `FALSE` | - | - | - | on_shopify_custom_plan **Description:** Indicates whether the account is subscribed to a custom Shopify plan rather than a standard pricing tier. Defaults to FALSE; when TRUE, signifies the account has negotiated custom pricing or features with Shopify. |
| partner_billed | `boolean` | - | ✗ | `FALSE` | - | - | NOT NULL | partner_billed **Description:** Indicates whether the account is billed through a partner/reseller relationship rather than directly. When TRUE, billing and invoicing are handled by the partner organization; when FALSE (default), the account follows standard direct billing procedures. **Type:** B... |
| password | `string` | - | ✓ | - | - | - | - | **password** (string, nullable) Stores the encrypted/hashed password credential for account authentication. This field may be null for accounts using alternative authentication methods (e.g., SSO, OAuth) or for system-generated accounts that don't require password-based login. |
| payment_pending | `boolean` | - | ✓ | `FALSE` | - | - | - | payment_pending **Description:** Indicates whether the account has an outstanding payment that has not been processed or completed. When TRUE, signifies that payment collection is awaiting action or confirmation; defaults to FALSE for accounts with no pending payment obligations. |
| preferred_billing_currency | `integer` | - | ✓ | `USD` | INR(0), USD(1) | - | - | preferred_billing_currency **Description:** Specifies the currency preference for billing and invoicing the account. Accepts integer-encoded values representing INR (Indian Rupee) or USD (US Dollar), with USD as the default currency when not explicitly set. **Business Context:** Used to determine... |
| settings_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | **settings_flags** Integer-based bitwise flag field that stores multiple boolean account settings or preferences as a single numeric value. Each bit position represents a different account configuration option, with a default value of 0 indicating no flags are set. |
| shopify_access_token | `string` | - | ✓ | - | - | - | - | shopify_access_token **Description:** Stores the OAuth access token for authenticating and authorizing API requests to the associated Shopify store account. This token enables the system to interact with Shopify's API on behalf of the account owner and should be securely encrypted at rest. **Addi... |
| shopify_app_reinstalled | `boolean` | - | ✓ | `FALSE` | - | - | - | shopify_app_reinstalled **Description:** Indicates whether the Shopify app has been reinstalled for this account. This boolean flag is set to TRUE when an account reinstalls the application after a previous uninstallation, defaulting to FALSE for initial installations or accounts that have never ... |
| shopify_country_code | `string` | - | ✓ | - | - | - | - | shopify_country_code **Description:** Stores the two-letter ISO country code associated with the account's Shopify store location (e.g., "US", "CA", "GB"). This field is nullable as it only applies to accounts integrated with Shopify and is used for regional analytics and store-specific configura... |
| shopify_country_name | `string` | - | ✓ | - | - | - | - | **shopify_country_name** *Type: string \| Nullable: True* Stores the country name associated with the Shopify account, typically derived from the shop's primary location or regional settings. This field may be null for accounts not integrated with Shopify or where country information is unavailable. |
| shopify_deleted | `boolean` | - | ✓ | `FALSE` | - | - | - | shopify_deleted **Description:** Indicates whether the account has been deleted from Shopify. When TRUE, the account has been removed from the Shopify platform; defaults to FALSE for active accounts. **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE |
| shopify_store_url | `string` | - | ✓ | - | - | - | - | **shopify_store_url** The URL of the customer's Shopify store associated with this account. This field is optional and enables integration tracking and identification of accounts using Shopify as their e-commerce platform. |
| source | `string` | - | ✓ | - | - | - | - | source **Description:** Indicates the origin or acquisition channel through which the account was created or obtained (e.g., web signup, API integration, referral). This helps track account acquisition patterns and marketing effectiveness. **Data Format:** String value (nullable), typically conta... |
| support_email | `string` | 100 | ✓ | - | - | - | - | support_email **Description:** Email address designated for customer support inquiries related to this account. This optional field allows accounts to specify a dedicated support contact, separate from the primary account email, for handling customer service requests and helpdesk communications. ... |
| template_last_synced_at | `datetime` | - | ✓ | - | - | - | - | template_last_synced_at **Description:** Timestamp (UTC) indicating when templates associated with this account were last synchronized. Used to track template synchronization status and determine when the next sync operation should occur. |
| username | `string` | - | ✓ | - | - | - | - | username **Description:** The login identifier for an agent account in the system. This string field is nullable and serves as the primary way to identify and authenticate agents who handle customer conversations, as referenced throughout analytics and conversation tracking. **Data Format:** Stri... |
| website_url | `string` | - | ✓ | - | - | - | - | **website_url** The URL of the website or web property associated with the account. This field is optional and typically stores the primary domain or web address linked to the customer's business or organization. |
| created_at | `datetime` | - | ✗ | - | - | - | NOT NULL | **created_at** `datetime` \| NOT NULL UTC timestamp indicating when the account record was initially created in the system. This immutable field serves as the definitive audit trail for account origination and is used for chronological tracking and reporting purposes. |
| updated_at | `datetime` | - | ✗ | - | - | - | NOT NULL | **updated_at** `timestamp` \| UTC \| NOT NULL Timestamp indicating when the account record was last modified. This field is automatically updated whenever any changes are made to the account entry, enabling tracking of data freshness and audit trails. |
| customer_id | `string` | - | ✓ | - | - | - | - | **customer_id** (string, nullable) Unique identifier for the customer (contact) associated with the account. References the contact/customer record and may be null for accounts not yet linked to a specific customer. |

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

