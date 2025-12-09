# 📊 Limechat Database Schema Documentation

> **Generated:** 2025-12-09 at 11:58:48
> **Total Tables:** 1

## 📑 Table of Contents

- [accounts](#accounts)

---

## accounts

> **Model:** `Account`

### 📝 Table Description

## Accounts Table

**Primary entity representing customer organizations/tenants in the multi-tenant helpdesk system.** Each account corresponds to a company using the platform and contains configuration settings including assignment logic, currency preferences, feature flags, contact masking options, and UI customization (e.g., hiding specific tabs for agents/supervisors). 

The account serves as the top-level parent entity with 74 relationships cascading down to conversations, users (agents), contacts (customers), inboxes, and other core system resources. Key use cases include tenant isolation, billing management (via `billing_email` and `currency`), feature enablement through `feature_flags`, enterprise tier identification (`is_enterprise`), and workspace-level settings like auto-resolve duration and tag enforcement.

**Note:** Supports soft deletion via `deleted_at` timestamp.

### 📋 Columns

| Column | Type | Length | Nullable | Default | Enum Values | Validations | Constraints | Description |
|--------|------|--------|----------|---------|-------------|-------------|-------------|-------------|
| **id** | `integer` | - | ✗ | - | - | - | NOT NULL, PRIMARY KEY | **Primary Key** - ID is a sequentially increasing integer that uniquely identifies each account record and serves as the PRIMARY KEY of the accounts table. |
| assignment_logic | `integer` | - | ✗ | `load_balanced` | round_robin(0), load_balanced(1) | - | NOT NULL | assignment_logic **Description:** Determines the algorithm used to distribute incoming conversations to available agents within the account. Values include `round_robin` (sequential distribution to agents in order) and `load_balanced` (default; distributes based on current agent workload to optim... |
| auto_resolve_duration | `integer` | - | ✓ | - | - | numericality | - | auto_resolve_duration **Description:** Specifies the time duration (in days) after which inactive conversations in this account will be automatically resolved. When set, conversations remain open for this number of days before being automatically closed; if null, auto-resolution is disabled for t... |
| billing_email | `string` | - | ✓ | - | - | - | - | **billing_email** Email address designated for receiving billing-related communications and invoices for the account. This field is optional and may differ from the primary account contact email, allowing separate routing of financial correspondence. |
| contact_masking | `boolean` | - | ✓ | `FALSE` | - | - | - | contact_masking **Boolean flag indicating whether contact (customer) personal information should be masked or hidden for privacy/security purposes.** When enabled (TRUE), the customer's sensitive contact details are obfuscated in the system interface and reports; defaults to FALSE allowing full c... |
| currency | `text` | - | ✓ | `INR` | - | - | - | Currency **Type:** text \| **Nullable:** Yes \| **Default:** INR **Description:** Specifies the currency code for the account's financial transactions and balances. Defaults to INR (Indian Rupee) when not explicitly set, and can be null for accounts where currency context is not applicable. |
| deleted_at | `datetime` | - | ✓ | - | - | - | - | deleted_at **Type:** datetime \| **Nullable:** True **Description:** UTC timestamp indicating when the account was soft-deleted. When NULL, the account is active; when populated, the account is marked as deleted and typically excluded from standard queries (soft delete pattern). |
| domain | `string` | 100 | ✓ | - | - | - | - | **domain** (string, 100, nullable) The domain name or web address associated with the account, typically representing the organization's primary website or branded subdomain where the helpdesk/dashboard service is deployed. This field is optional and may be used to identify and differentiate mult... |
| enforce_tagging | `boolean` | - | ✓ | `FALSE` | - | - | - | enforce_tagging **Description:** Determines whether tagging of conversations is mandatory for agents within the account. When enabled (TRUE), agents must apply relevant tags before closing or completing conversations; when disabled (FALSE, default), tagging remains optional. **Type:** Boolean \| ... |
| feature_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | feature_flags **Description:** A bitmask integer field used to enable or disable specific account-level features through binary flags. Each bit position represents a distinct feature toggle, allowing multiple features to be stored efficiently in a single column (e.g., bit 0 for feature A, bit 1 f... |
| grace_added_on | `datetime` | - | ✓ | - | - | - | - | grace_added_on **Description:** Records the UTC timestamp when a grace period was granted to the account. This nullable field tracks when temporary extension privileges were applied, typically used for billing or service continuity purposes. **Data Type:** datetime (UTC) **Nullable:** Yes |
| grace_extension | `boolean` | - | ✓ | `FALSE` | - | - | - | **grace_extension** `boolean` \| Nullable \| Default: `FALSE` Indicates whether the account has been granted a grace period extension, typically allowing continued access or functionality beyond the standard expiration date. When set to TRUE, the account receives temporary reprieve from suspensio... |
| hide_all_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_all_tab **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Controls the visibility of the "All" tab in the account's interface. When set to TRUE, the "All" tab is hidden from view for users associated with this account, allowing administrators to customize the navi... |
| hide_all_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_all_tab_for_supervisor **Description:** Controls visibility of the "All" tab for users with supervisor role. When set to TRUE, supervisors will not see the "All" conversations/tickets tab in their dashboard view, limiting their view to only assigned or team-specific items. **Data Format:** B... |
| hide_bot_conversations | `boolean` | - | ✓ | `FALSE` | - | - | - | **hide_bot_conversations** Boolean flag that controls the visibility of bot-handled conversations in the account's interface. When set to TRUE, conversations where only the bot was involved (no agent interaction) are filtered from the conversation views, helping agents focus on human-assisted int... |
| hide_out_of_stock | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_out_of_stock **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Controls whether out-of-stock products are hidden from display for this account. When set to TRUE, products with zero inventory will be automatically filtered from the account's product catalog or stor... |
| hide_queued_tab | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_queued_tab **Type:** boolean \| **Nullable:** True \| **Default:** FALSE **Description:** Controls the visibility of the queued conversations tab in the agent dashboard. When set to TRUE, the queued tab is hidden from the account's interface, allowing accounts to customize their conversation... |
| hide_queued_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - | hide_queued_tab_for_supervisor **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Controls visibility of the queued conversations tab for supervisor-level users. When set to TRUE, supervisors will not see the queued tab in their dashboard interface, allowing account-lev... |
| is_enterprise | `boolean` | - | ✓ | `FALSE` | - | - | - | is_enterprise **Description:** Indicates whether the account is classified as an enterprise-tier account. This boolean flag (defaulting to FALSE) is used to differentiate enterprise customers from standard accounts, typically affecting feature access, billing tier, and service level agreements. *... |
| locale | `integer` | - | ✓ | `en` | see enum details | - | - | locale **Type:** integer \| **Nullable:** Yes \| **Default:** en **Description:** Stores the preferred language setting for the account using ISO 639-1 language codes (mapped as integers via LANGUAGES_CONFIG). Determines the localization and language preferences for the account's interface and co... |
| name | `string` | - | ✗ | - | - | required | NOT NULL | **name** `string` · Required The account name identifier that uniquely represents the organization or workspace. This is a mandatory field used throughout the system to reference and display the account across all 74 relationship connections. |
| on_grace_period | `boolean` | - | ✓ | `FALSE` | - | - | - | on_grace_period **Description:** Indicates whether the account is currently in a grace period, typically after a subscription or payment issue, allowing continued access to services before enforcement of restrictions. Defaults to FALSE when not explicitly set. **Business Context:** Used to manage... |
| on_shopify_custom_plan | `boolean` | - | ✓ | `FALSE` | - | - | - | on_shopify_custom_plan **Description:** Indicates whether the account is subscribed to a custom Shopify pricing plan rather than a standard tier. Defaults to FALSE; when TRUE, signifies the account has negotiated custom terms or enterprise-level pricing with Shopify. |
| partner_billed | `boolean` | - | ✗ | `FALSE` | - | - | NOT NULL | partner_billed **Description:** Boolean flag indicating whether the account has been billed through a partner/reseller arrangement. When TRUE, denotes that billing is handled by a partner entity rather than directly; defaults to FALSE for standard direct billing accounts. |
| password | `string` | - | ✓ | - | - | - | - | **password** (string, nullable) Stores the encrypted/hashed password credential for agent authentication. This field may be null for accounts using alternative authentication methods (e.g., SSO, OAuth) or for system-generated service accounts that don't require password-based login. |
| payment_pending | `boolean` | - | ✓ | `FALSE` | - | - | - | payment_pending **Description:** Indicates whether the account has an outstanding payment that is awaiting processing or completion. Defaults to FALSE, meaning no pending payments unless explicitly set otherwise. |
| preferred_billing_currency | `integer` | - | ✓ | `USD` | INR(0), USD(1) | - | - | preferred_billing_currency **Type:** integer \| **Nullable:** True \| **Default:** USD **Description:** Specifies the account's preferred currency for billing and invoicing purposes. Accepts enumerated values: INR (Indian Rupee) or USD (US Dollar), with USD as the default currency when not explic... |
| settings_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL | **settings_flags** `integer` \| NOT NULL \| Default: 0 Stores account-level configuration preferences as bitwise flags, where each bit position represents a specific setting toggle (e.g., feature enablement, notification preferences, or access controls). The integer value is a bitmask that allows... |
| shopify_access_token | `string` | - | ✓ | - | - | - | - | **shopify_access_token** OAuth access token used to authenticate and authorize API requests to the Shopify store associated with this account. This token enables the system to perform operations on behalf of the merchant, such as syncing orders, products, and customer data from their Shopify store. |
| shopify_app_reinstalled | `boolean` | - | ✓ | `FALSE` | - | - | - | shopify_app_reinstalled **Type:** boolean \| **Nullable:** Yes \| **Default:** FALSE **Description:** Indicates whether the Shopify app has been reinstalled for this account. This flag is set to TRUE when an account that previously uninstalled the Shopify integration reinstalls it, helping track ... |
| shopify_country_code | `string` | - | ✓ | - | - | - | - | shopify_country_code **Description:** Stores the two-letter ISO country code associated with the Shopify account, indicating the primary geographic location or market where the account operates. This field is nullable and may be empty for accounts not integrated with Shopify or where country info... |
| shopify_country_name | `string` | - | ✓ | - | - | - | - | shopify_country_name **Description:** The country name associated with the account's Shopify store location or primary business address. This field is nullable and stores the full country name in string format, typically used for geographical segmentation and regional analytics. |
| shopify_deleted | `boolean` | - | ✓ | `FALSE` | - | - | - | shopify_deleted **Description:** A boolean flag indicating whether the account has been deleted from Shopify. When set to TRUE, it marks that the corresponding Shopify account is no longer active or has been removed from the Shopify platform. **Default Value:** FALSE (account is active by default) |
| shopify_store_url | `string` | - | ✓ | - | - | - | - | The Shopify store URL associated with the account, used to identify and link the account to a specific Shopify merchant store. This field is optional and should contain the full store URL (e.g., "https://storename.myshopify.com") when the account is integrated with Shopify. |
| source | `string` | - | ✓ | - | - | - | - | source Indicates the originating channel or platform through which the account was created or acquired (e.g., web signup, mobile app, API integration, referral). This nullable field helps track account acquisition channels for analytics and attribution purposes. |
| support_email | `string` | 100 | ✓ | - | - | - | - | support_email **Description:** Email address designated for customer support inquiries associated with the account. This optional field (nullable) can store up to 100 characters and serves as the primary contact point for support-related communications. **Business Context:** Used to route support... |
| template_last_synced_at | `datetime` | - | ✓ | - | - | - | - | template_last_synced_at **Description:** UTC timestamp indicating when the account's templates were last synchronized. This field remains NULL until the first template sync operation is performed for the account. **Data Type:** datetime \| **Nullable:** Yes |
| username | `string` | - | ✓ | - | - | - | - | **username** (string, nullable): The login identifier for an agent account in the system. This field may be null for accounts that are not yet fully provisioned or for system-generated entries. |
| website_url | `string` | - | ✓ | - | - | - | - | **website_url** `string \| nullable` Stores the URL of the account's website (e.g., company website or business homepage). This field is optional and helps identify the organization associated with the account. |
| created_at | `datetime` | - | ✗ | - | - | - | NOT NULL | created_at **Description:** UTC timestamp indicating when the account record was created in the system. This field is automatically populated upon account creation and cannot be null, serving as an immutable audit trail for account inception. |
| updated_at | `datetime` | - | ✗ | - | - | - | NOT NULL | updated_at **Description:** UTC timestamp indicating when the account record was last modified. This field is automatically updated whenever any changes are made to the account entry, providing an audit trail for data modifications. **Technical Details:** - Type: datetime (UTC) - Nullable: False ... |
| customer_id | `string` | - | ✓ | - | - | - | - | **customer_id** Uniquely identifies the customer (contact) associated with this account. References the customer/contact record and serves as a foreign key to link account information with the corresponding customer data across the system. |

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

