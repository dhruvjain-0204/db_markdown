# 📊 Limechat Database Schema Documentation

> **Generated:** 2025-12-09 at 11:55:36
> **Total Tables:** 1

## 📑 Table of Contents

- [accounts](#accounts)

---

## accounts

> **Model:** `Account`

### 📋 Columns

| Column | Type | Length | Nullable | Default | Enum Values | Validations | Constraints |
|--------|------|--------|----------|---------|-------------|-------------|-------------|
| **id** 🔑 | `integer` | - | ✗ | - | - | - | NOT NULL, PRIMARY KEY |
| assignment_logic | `integer` | - | ✗ | `load_balanced` | round_robin(0), load_balanced(1) | - | NOT NULL |
| auto_resolve_duration | `integer` | - | ✓ | - | - | numericality | - |
| billing_email | `string` | - | ✓ | - | - | - | - |
| contact_masking | `boolean` | - | ✓ | `FALSE` | - | - | - |
| currency | `text` | - | ✓ | `INR` | - | - | - |
| deleted_at | `datetime` | - | ✓ | - | - | - | - |
| domain | `string` | 100 | ✓ | - | - | - | - |
| enforce_tagging | `boolean` | - | ✓ | `FALSE` | - | - | - |
| feature_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL |
| grace_added_on | `datetime` | - | ✓ | - | - | - | - |
| grace_extension | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_all_tab | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_all_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_bot_conversations | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_out_of_stock | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_queued_tab | `boolean` | - | ✓ | `FALSE` | - | - | - |
| hide_queued_tab_for_supervisor | `boolean` | - | ✓ | `FALSE` | - | - | - |
| is_enterprise | `boolean` | - | ✓ | `FALSE` | - | - | - |
| locale | `integer` | - | ✓ | `en` | see enum details | - | - |
| name | `string` | - | ✗ | - | - | required | NOT NULL |
| on_grace_period | `boolean` | - | ✓ | `FALSE` | - | - | - |
| on_shopify_custom_plan | `boolean` | - | ✓ | `FALSE` | - | - | - |
| partner_billed | `boolean` | - | ✗ | `FALSE` | - | - | NOT NULL |
| password | `string` | - | ✓ | - | - | - | - |
| payment_pending | `boolean` | - | ✓ | `FALSE` | - | - | - |
| preferred_billing_currency | `integer` | - | ✓ | `USD` | INR(0), USD(1) | - | - |
| settings_flags | `integer` | - | ✗ | `0` | - | - | NOT NULL |
| shopify_access_token | `string` | - | ✓ | - | - | - | - |
| shopify_app_reinstalled | `boolean` | - | ✓ | `FALSE` | - | - | - |
| shopify_country_code | `string` | - | ✓ | - | - | - | - |
| shopify_country_name | `string` | - | ✓ | - | - | - | - |
| shopify_deleted | `boolean` | - | ✓ | `FALSE` | - | - | - |
| shopify_store_url | `string` | - | ✓ | - | - | - | - |
| source | `string` | - | ✓ | - | - | - | - |
| support_email | `string` | 100 | ✓ | - | - | - | - |
| template_last_synced_at | `datetime` | - | ✓ | - | - | - | - |
| username | `string` | - | ✓ | - | - | - | - |
| website_url | `string` | - | ✓ | - | - | - | - |
| created_at | `datetime` | - | ✗ | - | - | - | NOT NULL |
| updated_at | `datetime` | - | ✗ | - | - | - | NOT NULL |
| customer_id | `string` | - | ✓ | - | - | - | - |

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

