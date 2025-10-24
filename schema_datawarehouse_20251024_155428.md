# Database Schema: datawarehouse

*Generated on: 2025-10-24 15:54:28*

---

<details>
<summary><h2 style="display: inline;">📊 Database Summary</h2></summary>

- **Total Tables:** 190
- **Total Columns:** 3408
- **Database Engine:** ClickHouse
</details>

---

<details>
<summary><h2 style="display: inline;">📋 Table of Contents</h2></summary>

1. [api_users](#api-users)
2. [api_users_raw](#api-users-raw)
3. [broadcast_activity_aggregations](#broadcast-activity-aggregations)
4. [broadcast_activity_aggregations_raw](#broadcast-activity-aggregations-raw)
5. [broadcast_reports](#broadcast-reports)
6. [broadcast_reports_raw](#broadcast-reports-raw)
7. [broadcasts](#broadcasts)
8. [broadcasts_raw](#broadcasts-raw)
9. [latest_broadcast_interactions](#latest-broadcast-interactions)
10. [latest_broadcast_interactions_raw](#latest-broadcast-interactions-raw)
11. [messages](#messages)
12. [pg_hd_message_analytics](#pg-hd-message-analytics)
13. [postgres2_agent_bots](#postgres2-agent-bots)
14. [postgres2_bot_analytics](#postgres2-bot-analytics)
15. [postgres2_bot_analytics_raw](#postgres2-bot-analytics-raw)
16. [postgres2_bot_failing_data](#postgres2-bot-failing-data)
17. [postgres2_company_data](#postgres2-company-data)
18. [postgres2_csat_survey_responses](#postgres2-csat-survey-responses)
19. [postgres2_draftimprover](#postgres2-draftimprover)
20. [postgres2_gpt_langgraph_qna](#postgres2-gpt-langgraph-qna)
21. [postgres2_gpt_langgraph_qna_raw](#postgres2-gpt-langgraph-qna-raw)
22. [postgres2_gptanswer](#postgres2-gptanswer)
23. [postgres2_gptanswer_raw](#postgres2-gptanswer-raw)
24. [postgres2_gptbotcost](#postgres2-gptbotcost)
25. [postgres2_gptbotcost_raw](#postgres2-gptbotcost-raw)
26. [postgres2_gptbotlatency](#postgres2-gptbotlatency)
27. [postgres2_gptintentredirection](#postgres2-gptintentredirection)
28. [postgres2_gptmetadata](#postgres2-gptmetadata)
29. [postgres2_gptmetadata_raw](#postgres2-gptmetadata-raw)
30. [postgres2_gpttranslation](#postgres2-gpttranslation)
31. [postgres2_ndr](#postgres2-ndr)
32. [postgres2_ndr_raw](#postgres2-ndr-raw)
33. [postgres2_outbound_feedbacks](#postgres2-outbound-feedbacks)
34. [postgres2_outbound_feedbacks_raw](#postgres2-outbound-feedbacks-raw)
35. [postgres2_sentimentemotionanalyzer](#postgres2-sentimentemotionanalyzer)
36. [postgres2_summarizer](#postgres2-summarizer)
37. [postgres_account_users](#postgres-account-users)
38. [postgres_account_users_raw](#postgres-account-users-raw)
39. [postgres_accounts](#postgres-accounts)
40. [postgres_agent_agent_analytics](#postgres-agent-agent-analytics)
41. [postgres_agent_analytics](#postgres-agent-analytics)
42. [postgres_attendances](#postgres-attendances)
43. [postgres_automation_rule_analytic](#postgres-automation-rule-analytic)
44. [postgres_automation_rule_analytic_raw](#postgres-automation-rule-analytic-raw)
45. [postgres_automation_rules](#postgres-automation-rules)
46. [postgres_billing_attendances](#postgres-billing-attendances)
47. [postgres_billing_attendances_raw](#postgres-billing-attendances-raw)
48. [postgres_bot_cdc_bot_csat](#postgres-bot-cdc-bot-csat)
49. [postgres_bot_cdc_bot_csat_raw](#postgres-bot-cdc-bot-csat-raw)
50. [postgres_broadcasts](#postgres-broadcasts)
51. [postgres_channel_facebook_pages](#postgres-channel-facebook-pages)
52. [postgres_channel_gupshup_enterprises](#postgres-channel-gupshup-enterprises)
53. [postgres_channel_three_sixty_dialogs](#postgres-channel-three-sixty-dialogs)
54. [postgres_channel_whatsapp_cloud_apis](#postgres-channel-whatsapp-cloud-apis)
55. [postgres_channel_whatsapp_cloud_apis_raw](#postgres-channel-whatsapp-cloud-apis-raw)
56. [postgres_contacts](#postgres-contacts)
57. [postgres_conv_agent_analytics](#postgres-conv-agent-analytics)
58. [postgres_conv_agent_analytics_raw](#postgres-conv-agent-analytics-raw)
59. [postgres_conv_agent_bot_inboxes](#postgres-conv-agent-bot-inboxes)
60. [postgres_conv_agent_bots](#postgres-conv-agent-bots)
61. [postgres_conv_ar_internal_metadata](#postgres-conv-ar-internal-metadata)
62. [postgres_conv_billing_plans](#postgres-conv-billing-plans)
63. [postgres_conv_canned_images](#postgres-conv-canned-images)
64. [postgres_conv_channel_api](#postgres-conv-channel-api)
65. [postgres_conv_channel_knowlarities](#postgres-conv-channel-knowlarities)
66. [postgres_conv_channel_value_firsts](#postgres-conv-channel-value-firsts)
67. [postgres_conv_channel_web_widgets](#postgres-conv-channel-web-widgets)
68. [postgres_conv_channel_zokos](#postgres-conv-channel-zokos)
69. [postgres_conv_contact_inboxes](#postgres-conv-contact-inboxes)
70. [postgres_conv_contact_labels](#postgres-conv-contact-labels)
71. [postgres_conv_conversation_analytics](#postgres-conv-conversation-analytics)
72. [postgres_conv_conversations](#postgres-conv-conversations)
73. [postgres_conv_shopify_availed_trials](#postgres-conv-shopify-availed-trials)
74. [postgres_conv_subscriptions](#postgres-conv-subscriptions)
75. [postgres_conv_taggings](#postgres-conv-taggings)
76. [postgres_conv_team_members](#postgres-conv-team-members)
77. [postgres_conv_webhook_watchers](#postgres-conv-webhook-watchers)
78. [postgres_conv_working_hour_slots](#postgres-conv-working-hour-slots)
79. [postgres_conversation_labels](#postgres-conversation-labels)
80. [postgres_conversation_labels_raw](#postgres-conversation-labels-raw)
81. [postgres_conversation_trackers](#postgres-conversation-trackers)
82. [postgres_csat_survey_responses](#postgres-csat-survey-responses)
83. [postgres_csat_survey_responses_raw](#postgres-csat-survey-responses-raw)
84. [postgres_ctwa_contact_trackings](#postgres-ctwa-contact-trackings)
85. [postgres_ctwa_contact_trackings_raw](#postgres-ctwa-contact-trackings-raw)
86. [postgres_curated_views](#postgres-curated-views)
87. [postgres_curated_views_raw](#postgres-curated-views-raw)
88. [postgres_custom_field_inboxes](#postgres-custom-field-inboxes)
89. [postgres_custom_field_inboxes_raw](#postgres-custom-field-inboxes-raw)
90. [postgres_custom_field_options](#postgres-custom-field-options)
91. [postgres_custom_field_options_raw](#postgres-custom-field-options-raw)
92. [postgres_custom_field_values](#postgres-custom-field-values)
93. [postgres_custom_field_values_raw](#postgres-custom-field-values-raw)
94. [postgres_custom_fields](#postgres-custom-fields)
95. [postgres_custom_fields_raw](#postgres-custom-fields-raw)
96. [postgres_custom_views](#postgres-custom-views)
97. [postgres_custom_views_raw](#postgres-custom-views-raw)
98. [postgres_data_access_logs](#postgres-data-access-logs)
99. [postgres_data_access_logs_raw](#postgres-data-access-logs-raw)
100. [postgres_fb_account_account](#postgres-fb-account-account)
101. [postgres_fb_account_account_raw](#postgres-fb-account-account-raw)
102. [postgres_fb_account_integration](#postgres-fb-account-integration)
103. [postgres_fb_block_activities](#postgres-fb-block-activities)
104. [postgres_fb_block_activities_dup](#postgres-fb-block-activities-dup)
105. [postgres_fb_bot_builder_botcsat](#postgres-fb-bot-builder-botcsat)
106. [postgres_fb_bot_builder_botcsat_raw](#postgres-fb-bot-builder-botcsat-raw)
107. [postgres_fb_bot_builder_flow](#postgres-fb-bot-builder-flow)
108. [postgres_fb_bot_builder_flow_raw](#postgres-fb-bot-builder-flow-raw)
109. [postgres_fb_builder_user](#postgres-fb-builder-user)
110. [postgres_fb_builder_user_raw](#postgres-fb-builder-user-raw)
111. [postgres_fb_central_orders](#postgres-fb-central-orders)
112. [postgres_fb_conv_flow_messages](#postgres-fb-conv-flow-messages)
113. [postgres_fb_conv_flow_nodes](#postgres-fb-conv-flow-nodes)
114. [postgres_fb_conv_flow_nodes_raw](#postgres-fb-conv-flow-nodes-raw)
115. [postgres_fb_conversational_broadcasts](#postgres-fb-conversational-broadcasts)
116. [postgres_fb_conversational_broadcasts_raw](#postgres-fb-conversational-broadcasts-raw)
117. [postgres_fb_conversational_flow_executions](#postgres-fb-conversational-flow-executions)
118. [postgres_fb_conversational_flow_executions_raw](#postgres-fb-conversational-flow-executions-raw)
119. [postgres_fb_conversational_flows](#postgres-fb-conversational-flows)
120. [postgres_fb_conversational_flows_freetextreplies](#postgres-fb-conversational-flows-freetextreplies)
121. [postgres_fb_conversational_flows_freetextreplies_raw](#postgres-fb-conversational-flows-freetextreplies-raw)
122. [postgres_fb_igrn_broadcasts](#postgres-fb-igrn-broadcasts)
123. [postgres_fb_igrn_broadcasts_raw](#postgres-fb-igrn-broadcasts-raw)
124. [postgres_fb_igrn_optins](#postgres-fb-igrn-optins)
125. [postgres_hd_csat_survey_responses](#postgres-hd-csat-survey-responses)
126. [postgres_hd_csat_survey_responses_raw](#postgres-hd-csat-survey-responses-raw)
127. [postgres_hd_messages](#postgres-hd-messages)
128. [postgres_in_app_feedbacks](#postgres-in-app-feedbacks)
129. [postgres_inbox_members](#postgres-inbox-members)
130. [postgres_inboxes](#postgres-inboxes)
131. [postgres_labels](#postgres-labels)
132. [postgres_labels_raw](#postgres-labels-raw)
133. [postgres_lc_contacts_contacts](#postgres-lc-contacts-contacts)
134. [postgres_lk2_shopify_app_event](#postgres-lk2-shopify-app-event)
135. [postgres_lk2_shopify_app_event_raw](#postgres-lk2-shopify-app-event-raw)
136. [postgres_lk2_shopify_app_orderrefund](#postgres-lk2-shopify-app-orderrefund)
137. [postgres_lk2_shopify_app_orderrefund_raw](#postgres-lk2-shopify-app-orderrefund-raw)
138. [postgres_lk2_shopify_app_shopifyorder](#postgres-lk2-shopify-app-shopifyorder)
139. [postgres_lk2_shopify_app_shopifyorder_raw](#postgres-lk2-shopify-app-shopifyorder-raw)
140. [postgres_lk2_shopify_app_shopifyproduct](#postgres-lk2-shopify-app-shopifyproduct)
141. [postgres_lk2_shopify_app_shopifyproduct_raw](#postgres-lk2-shopify-app-shopifyproduct-raw)
142. [postgres_lk2_store_ordermodel](#postgres-lk2-store-ordermodel)
143. [postgres_lk2_store_ordermodel_raw](#postgres-lk2-store-ordermodel-raw)
144. [postgres_lk2_store_productcollectionmodel](#postgres-lk2-store-productcollectionmodel)
145. [postgres_lk2_store_productcollectionmodel_raw](#postgres-lk2-store-productcollectionmodel-raw)
146. [postgres_lk_account_accountmodel](#postgres-lk-account-accountmodel)
147. [postgres_lk_account_accountproperties](#postgres-lk-account-accountproperties)
148. [postgres_lk_account_accountproperties_raw](#postgres-lk-account-accountproperties-raw)
149. [postgres_lk_bifrostbridge_leadsqauredconvomapping](#postgres-lk-bifrostbridge-leadsqauredconvomapping)
150. [postgres_lk_bifrostbridge_leadsquaredusers](#postgres-lk-bifrostbridge-leadsquaredusers)
151. [postgres_lk_influenced_sales](#postgres-lk-influenced-sales)
152. [postgres_lk_influenced_sales_raw](#postgres-lk-influenced-sales-raw)
153. [postgres_lk_shopify_app_event](#postgres-lk-shopify-app-event)
154. [postgres_lk_shopify_app_event_raw](#postgres-lk-shopify-app-event-raw)
155. [postgres_lk_shopify_app_orderrefund](#postgres-lk-shopify-app-orderrefund)
156. [postgres_lk_shopify_app_shopifyorder](#postgres-lk-shopify-app-shopifyorder)
157. [postgres_lk_shopify_app_shopifyorder_raw](#postgres-lk-shopify-app-shopifyorder-raw)
158. [postgres_lk_store_customermodel](#postgres-lk-store-customermodel)
159. [postgres_lk_store_igmedia](#postgres-lk-store-igmedia)
160. [postgres_lk_store_ordermodel](#postgres-lk-store-ordermodel)
161. [postgres_lk_store_productcollectionmodel](#postgres-lk-store-productcollectionmodel)
162. [postgres_lk_store_productcollectionmodel_raw](#postgres-lk-store-productcollectionmodel-raw)
163. [postgres_lk_store_productmodel](#postgres-lk-store-productmodel)
164. [postgres_lk_store_store](#postgres-lk-store-store)
165. [postgres_lk_store_store_raw](#postgres-lk-store-store-raw)
166. [postgres_lk_test_lk_table_raw](#postgres-lk-test-lk-table-raw)
167. [postgres_messages_message_tags](#postgres-messages-message-tags)
168. [postgres_messages_taggables](#postgres-messages-taggables)
169. [postgres_sla_policies](#postgres-sla-policies)
170. [postgres_sla_policies_raw](#postgres-sla-policies-raw)
171. [postgres_sla_trackers](#postgres-sla-trackers)
172. [postgres_sla_trackers_raw](#postgres-sla-trackers-raw)
173. [postgres_taggables](#postgres-taggables)
174. [postgres_teams](#postgres-teams)
175. [postgres_teams_raw](#postgres-teams-raw)
176. [postgres_templates](#postgres-templates)
177. [postgres_templates_raw](#postgres-templates-raw)
178. [postgres_users](#postgres-users)
179. [postgresfb2_central_orders](#postgresfb2-central-orders)
180. [postgresfb2_central_orders_raw](#postgresfb2-central-orders-raw)
181. [postgresfb_block_activities](#postgresfb-block-activities)
182. [postgresfb_block_activities_raw](#postgresfb-block-activities-raw)
183. [postgresfb_block_activities_raw_2](#postgresfb-block-activities-raw-2)
184. [postgresfb_builder_user](#postgresfb-builder-user)
185. [postgresfb_builder_user_raw](#postgresfb-builder-user-raw)
186. [postres2_bot_analytics](#postres2-bot-analytics)
187. [subscriptions](#subscriptions)
188. [subscriptions_raw](#subscriptions-raw)
189. [templates](#templates)
190. [templates_raw](#templates-raw)
</details>

---

## api_users {#api-users}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 14

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 23.285714285714285 chars
- **Distinct Values:** 14

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 14

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 28,052.0
- **Average:** 20,419.428571428572
- **Distinct Values:** 12

### scopes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 17.928571428571427 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### token

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 28.5 chars
- **Distinct Values:** 8

</details>

</details>

---

## api_users_raw {#api-users-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users_raw`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 14

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 23.285714285714285 chars
- **Distinct Values:** 14

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 14

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 28,052.0
- **Average:** 20,419.428571428572
- **Distinct Values:** 12

### scopes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 17.928571428571427 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### token

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 28.5 chars
- **Distinct Values:** 8

</details>

</details>

---

## broadcast_activity_aggregations {#broadcast-activity-aggregations}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,999

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### broadcast

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,001

### deliveredcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 157,952.0
- **Average:** 3,681.858
- **Distinct Values:** 4,573

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### failedbybspcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 71,827.0
- **Average:** 1,927.6225
- **Distinct Values:** 3,482

### failedbyumscount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 96,703.0
- **Average:** 294.3715
- **Distinct Values:** 728

### filteredoutbyums

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3,278.0
- **Average:** 46.117852975495914
- **Distinct Values:** 226
- **Null %:** 82.9%

### optedoutbyums

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2,785.0
- **Average:** 44.8115623383342
- **Distinct Values:** 490
- **Null %:** 22.7%

### overallprogress

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 207,752.0
- **Average:** 6,469.946
- **Distinct Values:** 4,315

### readcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 70,090.0
- **Average:** 1,685.8446
- **Distinct Values:** 3,510

### sentbyumscount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 194,175.0
- **Average:** 4,205.7452
- **Distinct Values:** 4,767

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## broadcast_activity_aggregations_raw {#broadcast-activity-aggregations-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### broadcast

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### deliveredcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 157,952.0
- **Average:** 3,743.1335
- **Distinct Values:** 4,587

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### failedbybspcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 71,827.0
- **Average:** 1,761.9301
- **Distinct Values:** 3,352

### failedbyumscount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 96,703.0
- **Average:** 264.8207
- **Distinct Values:** 725

### filteredoutbyums

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3,278.0
- **Average:** 48.54331408262994
- **Distinct Values:** 265
- **Null %:** 77.5%

### optedoutbyums

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2,785.0
- **Average:** 47.12255671279783
- **Distinct Values:** 464
- **Null %:** 29.9%

### overallprogress

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 207,752.0
- **Average:** 6,386.1942
- **Distinct Values:** 4,302

### readcount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 102,969.0
- **Average:** 1,697.952
- **Distinct Values:** 3,546

### sentbyumscount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 194,175.0
- **Average:** 4,315.883099999999
- **Distinct Values:** 4,796

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## broadcast_reports {#broadcast-reports}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### broadcast

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,999

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 31.3656 chars
- **Distinct Values:** 9,539

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### reportkey

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 50.0 chars
- **Distinct Values:** 9,999

### retryreportkeys

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.0281 chars
- **Distinct Values:** 460

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 31.4576 chars
- **Distinct Values:** 9,564

</details>

</details>

---

## broadcast_reports_raw {#broadcast-reports-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,998

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### broadcast

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,999

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 30.9158 chars
- **Distinct Values:** 9,399

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### reportkey

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 50.0 chars
- **Distinct Values:** 9,998

### retryreportkeys

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.6386 chars
- **Distinct Values:** 304

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 31.031 chars
- **Distinct Values:** 9,435

</details>

</details>

---

## broadcasts {#broadcasts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts`

<details>
<summary><strong>📊 Columns (54 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### cohortid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3552 chars
- **Distinct Values:** 138

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8874 chars
- **Distinct Values:** 9,994

### csvurl

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 138.901 chars
- **Distinct Values:** 9,892

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### events

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 397.3511 chars
- **Distinct Values:** 9,909

### filteredmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 131,029.0
- **Average:** 5,837.133402813965
- **Distinct Values:** 1,242
- **Null %:** 80.8%

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,036.0
- **Average:** 15,152.7041
- **Distinct Values:** 180

### inboxid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 35,153.0
- **Average:** 27,948.071400000004
- **Distinct Values:** 252

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.11 chars
- **Distinct Values:** 8,168

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,676.5685631386405
- **Distinct Values:** 3,879
- **Null %:** 20.7%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.2879 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 7

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0006
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 492
- **Null %:** 95.1%

### requestbody_cohortid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3528 chars
- **Distinct Values:** 137

### requestbody_csvurl

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 131.1699 chars
- **Distinct Values:** 9,618

### requestbody_inboxid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 35,153.0
- **Average:** 28,126.349310903934
- **Distinct Values:** 247
- **Null %:** 1.3%

### requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 76.4068 chars
- **Distinct Values:** 2,770

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.6039 chars
- **Distinct Values:** 106

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4962 chars
- **Distinct Values:** 147

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0481 chars
- **Distinct Values:** 40

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3777 chars
- **Distinct Values:** 57

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.2471 chars
- **Distinct Values:** 11

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0885 chars
- **Distinct Values:** 77

### requestbody_metadata_fbbroadcastid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 19,026.0 to 20,318.0
- **Average:** 19,988.36170212766
- **Distinct Values:** 377
- **Null %:** 96.2%

### requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.8209 chars
- **Distinct Values:** 373

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2433 chars
- **Distinct Values:** 20

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7707 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 97.0862 chars
- **Distinct Values:** 6,849

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3581
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.6115 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 55.3345 chars
- **Distinct Values:** 921

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0407 chars
- **Distinct Values:** 20

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0289 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.022 chars
- **Distinct Values:** 3

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.004 chars
- **Distinct Values:** 4

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.863 chars
- **Distinct Values:** 8,061

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9604 chars
- **Distinct Values:** 2

### requestbody_templateid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 7,669.0
- **Average:** 1,360.8628901499796
- **Distinct Values:** 2,893
- **Null %:** 1.3%

### requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2859 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.9761784723972775
- **Distinct Values:** 7
- **Null %:** 20.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9917 chars
- **Distinct Values:** 3

### templateid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7,669.0
- **Average:** 1,358.3726
- **Distinct Values:** 2,921

### throughput

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 980.0
- **Average:** 143.4905
- **Distinct Values:** 7

### totalmessagecount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 171,562.0
- **Average:** 6,457.386099999999
- **Distinct Values:** 4,172

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8906 chars
- **Distinct Values:** 9,626

</details>

</details>

---

## broadcasts_raw {#broadcasts-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts_raw`

<details>
<summary><strong>📊 Columns (54 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,001

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### cohortid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4752 chars
- **Distinct Values:** 175

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.887 chars
- **Distinct Values:** 9,992

### csvurl

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 136.5421 chars
- **Distinct Values:** 9,846

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### events

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 378.735 chars
- **Distinct Values:** 9,857

### filteredmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 131,029.0
- **Average:** 6,005.730003755163
- **Distinct Values:** 1,602
- **Null %:** 73.4%

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,036.0
- **Average:** 14,417.352200000003
- **Distinct Values:** 181

### inboxid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 35,153.0
- **Average:** 27,082.49250000001
- **Distinct Values:** 254

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.4716 chars
- **Distinct Values:** 8,416

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,808.323686428772
- **Distinct Values:** 3,640
- **Null %:** 28.8%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.7549 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0106 chars
- **Distinct Values:** 4

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0004
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 370
- **Null %:** 96.3%

### requestbody_cohortid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4728 chars
- **Distinct Values:** 174

### requestbody_csvurl

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 126.0694 chars
- **Distinct Values:** 9,466

### requestbody_inboxid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 35,153.0
- **Average:** 27,322.53639885806
- **Distinct Values:** 245
- **Null %:** 1.9%

### requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 69.9875 chars
- **Distinct Values:** 2,626

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.6681 chars
- **Distinct Values:** 90

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3927 chars
- **Distinct Values:** 127

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0328 chars
- **Distinct Values:** 33

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3044 chars
- **Distinct Values:** 45

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.1991 chars
- **Distinct Values:** 10

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0637 chars
- **Distinct Values:** 64

### requestbody_metadata_fbbroadcastid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 19,026.0 to 20,318.0
- **Average:** 19,996.540925266905
- **Distinct Values:** 282
- **Null %:** 97.2%

### requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.6052 chars
- **Distinct Values:** 277

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2361 chars
- **Distinct Values:** 19

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7869 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 93.6962 chars
- **Distinct Values:** 6,884

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3054
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.4511 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 51.3469 chars
- **Distinct Values:** 903

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0487 chars
- **Distinct Values:** 23

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0063 chars
- **Distinct Values:** 5

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0244 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0059 chars
- **Distinct Values:** 5

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.1173 chars
- **Distinct Values:** 8,263

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9424 chars
- **Distinct Values:** 2

### requestbody_templateid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 7,669.0
- **Average:** 1,367.417720228385
- **Distinct Values:** 2,916
- **Null %:** 1.9%

### requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2784 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.695298245614035
- **Distinct Values:** 7
- **Null %:** 28.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9896 chars
- **Distinct Values:** 3

### templateid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7,669.0
- **Average:** 1,364.3954
- **Distinct Values:** 2,948

### throughput

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 980.0
- **Average:** 160.1254
- **Distinct Values:** 7

### totalmessagecount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 171,562.0
- **Average:** 6,495.0651
- **Distinct Values:** 4,197

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8911 chars
- **Distinct Values:** 9,723

</details>

</details>

---

## latest_broadcast_interactions {#latest-broadcast-interactions}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,999

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,034

### broadcastid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 1,794

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8899 chars
- **Distinct Values:** 9,992

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,003.0
- **Average:** 14,104.0922
- **Distinct Values:** 155

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8912 chars
- **Distinct Values:** 9,991

### useridentifier

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9969 chars
- **Distinct Values:** 9,998

</details>

</details>

---

## latest_broadcast_interactions_raw {#latest-broadcast-interactions-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,034

### broadcastid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 1,792

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8852 chars
- **Distinct Values:** 9,989

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,991.0
- **Average:** 14,162.0831
- **Distinct Values:** 157

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.881 chars
- **Distinct Values:** 9,995

### useridentifier

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9971 chars
- **Distinct Values:** 9,998

</details>

</details>

---

## messages {#messages}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `messages`

<details>
<summary><strong>📊 Columns (225 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,001

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,123

### batchid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.9573 chars
- **Distinct Values:** 3,302

### broadcastid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.9872 chars
- **Distinct Values:** 1,521

### bspsourceid

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 42.3313 chars
- **Distinct Values:** 9,457

### channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 8.0 chars
- **Distinct Values:** 1

### channeltype

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 17.8559 chars
- **Distinct Values:** 6

### createdat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8883 chars
- **Distinct Values:** 9,999

### dispatchtype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.0 chars
- **Distinct Values:** 2

### error

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.156 chars
- **Distinct Values:** 2

### error_data

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.5446 chars
- **Distinct Values:** 46

### error_data_code

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.8177 chars
- **Distinct Values:** 26

### error_data_data

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.1114 chars
- **Distinct Values:** 5

### error_data_errno

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_error

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_error_data_details

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.1338 chars
- **Distinct Values:** 84

### error_data_error_data_messaging_product

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2248 chars
- **Distinct Values:** 2

### error_data_error_subcode

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 33.0 to 2,593,006.0
- **Average:** 864,357.3333333334
- **Distinct Values:** 3
- **Null %:** 99.8%

### error_data_error_user_msg

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0492 chars
- **Distinct Values:** 2

### error_data_error_user_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0108 chars
- **Distinct Values:** 2

### error_data_erroredsyscall

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_errors

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_fbtrace_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7222 chars
- **Distinct Values:** 315

### error_data_href

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.2168 chars
- **Distinct Values:** 2

### error_data_is_transient

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### error_data_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.6648 chars
- **Distinct Values:** 23

### error_data_meta_api_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_meta_version

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_statuscode

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### error_data_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 5.8893 chars
- **Distinct Values:** 9

### error_data_to

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4468 chars
- **Distinct Values:** 3

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,057.0
- **Average:** 13,079.5251
- **Distinct Values:** 201

### inboxid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 467.0 to 35,153.0
- **Average:** 27,581.01019999999
- **Distinct Values:** 279

### message_account_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.1064 chars
- **Distinct Values:** 8

### message_audio_format

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0028 chars
- **Distinct Values:** 2

### message_audio_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0031 chars
- **Distinct Values:** 3

### message_audio_mimetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 2

### message_audio_sha256

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0088 chars
- **Distinct Values:** 3

### message_audio_signature

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_audio_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_broadcast_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 19,712.0 to 20,264.0
- **Average:** 20,070.333333333332
- **Distinct Values:** 4
- **Null %:** 100.0%

### message_channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_contacts

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_frequently_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_conversational_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 8,451.0 to 26,398.0
- **Average:** 19,434.0987654321
- **Distinct Values:** 52
- **Null %:** 99.2%

### message_ctwasourceid

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0144 chars
- **Distinct Values:** 9

### message_ctwasourcetype

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0016 chars
- **Distinct Values:** 2

### message_destination

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.4362 chars
- **Distinct Values:** 8,659

### message_document_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_document_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0028 chars
- **Distinct Values:** 2

### message_document_format

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.005 chars
- **Distinct Values:** 3

### message_document_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0016 chars
- **Distinct Values:** 2

### message_document_mimetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0101 chars
- **Distinct Values:** 3

### message_document_sha256

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 2

### message_document_signature

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0128 chars
- **Distinct Values:** 3

### message_document_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0605 chars
- **Distinct Values:** 3

### message_errors

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0745 chars
- **Distinct Values:** 2

### message_event

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_forwarded

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_frequently_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0095 chars
- **Distinct Values:** 9

### message_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.7184 chars
- **Distinct Values:** 777

### message_image_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0428 chars
- **Distinct Values:** 7

### message_image_format

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0869 chars
- **Distinct Values:** 4

### message_image_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0493 chars
- **Distinct Values:** 33

### message_image_mimetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.055 chars
- **Distinct Values:** 2

### message_image_sha256

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.1408 chars
- **Distinct Values:** 33

### message_image_signature

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.1472 chars
- **Distinct Values:** 24

### message_image_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.7034 chars
- **Distinct Values:** 25

### message_inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 467.0 to 35,153.0
- **Average:** 27,553.089923910524
- **Distinct Values:** 260
- **Null %:** 13.3%

### message_interaction_buttonreply___ums_bidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2.0
- **Average:** 0.49473684210526314
- **Distinct Values:** 4
- **Null %:** 98.1%

### message_interaction_buttonreply_payload

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7569 chars
- **Distinct Values:** 86

### message_interaction_buttonreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.366 chars
- **Distinct Values:** 127

### message_interaction_istemplate

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0106
- **Distinct Values:** 2

### message_interaction_listreply___ums_ridx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 8.0
- **Average:** 1.8786127167630058
- **Distinct Values:** 10
- **Null %:** 98.3%

### message_interaction_listreply___ums_sidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 2
- **Null %:** 98.3%

### message_interaction_listreply_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.127 chars
- **Distinct Values:** 20

### message_interaction_listreply_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0367 chars
- **Distinct Values:** 12

### message_interaction_listreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.2767 chars
- **Distinct Values:** 101

### message_interaction_nfmreply_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_response_json

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4824 chars
- **Distinct Values:** 3

### message_interaction_undefined_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_undefined_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_address

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_latitude

- **Type:** `Float`
- **Semantic Type:** `Latitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_longitude

- **Type:** `Float`
- **Semantic Type:** `Longitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_messageid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_mobile

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0036 chars
- **Distinct Values:** 4

### message_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.1633 chars
- **Distinct Values:** 53

### message_node_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0009 chars
- **Distinct Values:** 2

### message_order_catalogid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0015 chars
- **Distinct Values:** 2

### message_order_productitems

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0087 chars
- **Distinct Values:** 2

### message_order_text

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4107 chars
- **Distinct Values:** 135

### message_payload_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.3338 chars
- **Distinct Values:** 827

### message_payload_content_button_text

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2012 chars
- **Distinct Values:** 7

### message_payload_content_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_catalog_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_discount_offset

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_discount_value

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_items

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_shipping_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_shipping_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_subtotal_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_subtotal_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_payment_settings

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_reference_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_total_amount_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_total_amount_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_sections

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.4834 chars
- **Distinct Values:** 116

### message_payload_extra_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3582 chars
- **Distinct Values:** 349

### message_payload_extra_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.0505 chars
- **Distinct Values:** 1,550

### message_payload_extra_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2431 chars
- **Distinct Values:** 28

### message_payload_extra_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.2549 chars
- **Distinct Values:** 44

### message_payload_extra_document_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0022 chars
- **Distinct Values:** 2

### message_payload_extra_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_extra_footer

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6437 chars
- **Distinct Values:** 7

### message_payload_extra_header

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.2563 chars
- **Distinct Values:** 106

### message_payload_extra_header_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0564 chars
- **Distinct Values:** 3

### message_payload_extra_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 50.9801 chars
- **Distinct Values:** 1,655

### message_payload_extra_metadata_messageid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7812 chars
- **Distinct Values:** 218

### message_payload_extra_metadata_phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.26 chars
- **Distinct Values:** 218

### message_payload_extra_metadata_region

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0434 chars
- **Distinct Values:** 3

### message_payload_extra_preview_url

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1069
- **Distinct Values:** 2

### message_payload_extras_buttons

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_metadata_cvf_form_input

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### message_payload_substitutions

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.6704 chars
- **Distinct Values:** 2,085

### message_payload_template_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 7,677.0
- **Average:** 1,536.0652627584898
- **Distinct Values:** 1,373
- **Null %:** 47.3%

### message_payload_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0737 chars
- **Distinct Values:** 8

### message_reaction

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0198 chars
- **Distinct Values:** 4

### message_reaction_emoji

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0008 chars
- **Distinct Values:** 4

### message_reaction_message_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0186 chars
- **Distinct Values:** 4

### message_receivedat

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_receiver

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.5911 chars
- **Distinct Values:** 184

### message_referral_catalog_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_referral_product_retailer_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_reply_to

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_replyid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3037 chars
- **Distinct Values:** 505

### message_sender

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_sender_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.4343 chars
- **Distinct Values:** 1,262

### message_sender_phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.5882 chars
- **Distinct Values:** 1,326

### message_senderid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.5882 chars
- **Distinct Values:** 1,326

### message_sticker_format

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0032 chars
- **Distinct Values:** 3

### message_sticker_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0016 chars
- **Distinct Values:** 2

### message_sticker_mimetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.002 chars
- **Distinct Values:** 2

### message_sticker_sha256

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 2

### message_sticker_signature

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0064 chars
- **Distinct Values:** 2

### message_sticker_stickeranimated

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_sticker_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0303 chars
- **Distinct Values:** 2

### message_system

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_wa_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_account_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 28,057.0
- **Average:** 12,497.032424086465
- **Distinct Values:** 129
- **Null %:** 80.6%

### message_template_allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0008
- **Distinct Values:** 2

### message_template_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 57.7796 chars
- **Distinct Values:** 613

### message_template_category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.57 chars
- **Distinct Values:** 5

### message_template_complex_template_config_cards

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_complex_template_config_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_created_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.386 chars
- **Distinct Values:** 650

### message_template_created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1514
- **Distinct Values:** 2

### message_template_display_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 7,677.0
- **Average:** 1,217.1909418425116
- **Distinct Values:** 479
- **Null %:** 80.6%

### message_template_footer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.4145 chars
- **Distinct Values:** 65

### message_template_header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2958 chars
- **Distinct Values:** 30

### message_template_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 3,195.0 to 155,409.0
- **Average:** 125,369.26505404014
- **Distinct Values:** 650
- **Null %:** 80.6%

### message_template_inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 585.0 to 35,098.0
- **Average:** 26,532.213072568193
- **Distinct Values:** 156
- **Null %:** 80.6%

### message_template_language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6752 chars
- **Distinct Values:** 8

### message_template_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.217 chars
- **Distinct Values:** 2

### message_template_namespace

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.7484 chars
- **Distinct Values:** 96

### message_template_short_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.452 chars
- **Distinct Values:** 594

### message_template_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.5526 chars
- **Distinct Values:** 5

### message_template_template_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.4151 chars
- **Distinct Values:** 420

### message_template_template_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.0985 chars
- **Distinct Values:** 320

### message_template_template_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3.0
- **Average:** 0.6562017498713331
- **Distinct Values:** 5
- **Null %:** 80.6%

### message_template_updated_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3901 chars
- **Distinct Values:** 1,045

### message_templateid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_templatetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.6175 chars
- **Distinct Values:** 652

### message_timestamp

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0119 chars
- **Distinct Values:** 12

### message_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.8732 chars
- **Distinct Values:** 11

### message_unsupported

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0745 chars
- **Distinct Values:** 2

### message_video_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_video_format

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0028 chars
- **Distinct Values:** 2

### message_video_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0031 chars
- **Distinct Values:** 3

### message_video_mimetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0018 chars
- **Distinct Values:** 2

### message_video_sha256

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0088 chars
- **Distinct Values:** 3

### message_video_signature

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_video_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_wamsgid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_wanumber

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0036 chars
- **Distinct Values:** 4

### response_bulkid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0076 chars
- **Distinct Values:** 5

### response_contacts

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 21.8795 chars
- **Distinct Values:** 4,458

### response_details

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### response_errors

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### response_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.8091 chars
- **Distinct Values:** 2,066

### response_messages

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 41.6236 chars
- **Distinct Values:** 4,463

### response_messaging_product

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.5664 chars
- **Distinct Values:** 2

### response_mid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.1086 chars
- **Distinct Values:** 29

### response_phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.4771 chars
- **Distinct Values:** 2,062

### response_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.4455 chars
- **Distinct Values:** 2

### response_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### response_to

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0336 chars
- **Distinct Values:** 29

### retriesattempted

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5.0
- **Average:** 0.040580394007313905
- **Distinct Values:** 7
- **Null %:** 15.2%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.3286 chars
- **Distinct Values:** 10

### uniqueid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 21.0 chars
- **Distinct Values:** 9,998

### updatedat

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8844 chars
- **Distinct Values:** 10,001

</details>

</details>

---

## pg_hd_message_analytics {#pg-hd-message-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `pg_hd_message_analytics`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 979

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,510.0
- **Average:** 1,285.5092
- **Distinct Values:** 89

### content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 263.4057 chars
- **Distinct Values:** 1,905

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,472,691.0 to 97,616,194.0
- **Average:** 91,207,940.71720003
- **Distinct Values:** 9,980

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,137

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### is_read

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4462
- **Distinct Values:** 2

### is_replied

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2134
- **Distinct Values:** 2

### is_template

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 426,474,586.0 to 705,202,540.0
- **Average:** 663,138,806.8788992
- **Distinct Values:** 9,999

### read_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 3,680
- **Null %:** 55.4%

### reply_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.6483 chars
- **Distinct Values:** 1,262

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,360

</details>

</details>

---

## postgres2_agent_bots {#postgres2-agent-bots}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_agent_bots`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 46

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 437

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.034334763948497854 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 466

### hide_input_for_bot_conversations

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 11.141630901287554 chars
- **Distinct Values:** 436

### outgoing_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 57.94849785407725 chars
- **Distinct Values:** 433

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 466

</details>

</details>

---

## postgres2_bot_analytics {#postgres2-bot-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_analytics`

<details>
<summary><strong>📊 Columns (21 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 148

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 27,138.0
- **Average:** 7,756.4852
- **Distinct Values:** 86

### channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 11.8384 chars
- **Distinct Values:** 8

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 12,019,890.0
- **Average:** 1,981,444.4242
- **Distinct Values:** 1,496

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 81,284,613.0
- **Average:** 71,851,185.57960013
- **Distinct Values:** 1,496

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,484

### date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### distinct_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4244 chars
- **Distinct Values:** 9,312

### event_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,057,099,562.0 to 1,057,154,132.0
- **Average:** 1,057,126,400.3716
- **Distinct Values:** 9,999

### event_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.4317 chars
- **Distinct Values:** 411

### event_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 1.7003
- **Distinct Values:** 4

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 33,800.0
- **Average:** 13,594.429800000004
- **Distinct Values:** 106

### inserted_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 178

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3271
- **Distinct Values:** 2

### products

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 4.0542 chars
- **Distinct Values:** 175

### properties

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1,157.8719 chars
- **Distinct Values:** 9,883

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 57.6087 chars
- **Distinct Values:** 2,549

### timestamp

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,704,067,200.0 to 1,704,077,570.0
- **Average:** 1,704,073,386.448
- **Distinct Values:** 82

</details>

</details>

---

## postgres2_bot_analytics_raw {#postgres2-bot-analytics-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_analytics_raw`

<details>
<summary><strong>📊 Columns (21 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 27,138.0
- **Average:** 7,756.4852
- **Distinct Values:** 86

### channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 13.6257 chars
- **Distinct Values:** 8

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 12,019,890.0
- **Average:** 1,981,444.4242
- **Distinct Values:** 1,496

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 81,284,613.0
- **Average:** 71,851,185.57960013
- **Distinct Values:** 1,496

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,484

### date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### distinct_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.809 chars
- **Distinct Values:** 1,485

### event_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,057,099,562.0 to 1,057,154,132.0
- **Average:** 1,057,126,400.3716
- **Distinct Values:** 9,999

### event_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.9515 chars
- **Distinct Values:** 478

### event_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 1.7003
- **Distinct Values:** 4

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 33,800.0
- **Average:** 13,594.429800000004
- **Distinct Values:** 106

### inserted_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5189
- **Distinct Values:** 2

### products

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 3.289 chars
- **Distinct Values:** 134

### properties

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1,130.5868 chars
- **Distinct Values:** 9,856

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 52.3779 chars
- **Distinct Values:** 1,899

### timestamp

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,704,067,200.0 to 1,704,077,570.0
- **Average:** 1,704,073,386.448
- **Distinct Values:** 82

</details>

</details>

---

## postgres2_bot_failing_data {#postgres2-bot-failing-data}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_failing_data`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 471

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 28.0 to 27,070.0
- **Average:** 2,527.7313
- **Distinct Values:** 181

### bot_confidence

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.11616397 to 1.0
- **Average:** 0.684902463909
- **Distinct Values:** 5,484

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 275.0 to 12,046,151.0
- **Average:** 1,145,416.8120000002
- **Distinct Values:** 9,956

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### event_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 93,121,438.0 to 1,090,696,562.0
- **Average:** 527,041,551.0869
- **Distinct Values:** 10,000

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 33,818.0
- **Average:** 4,998.432200000001
- **Distinct Values:** 269

### inserted_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### intent

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.986 chars
- **Distinct Values:** 239

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2289
- **Distinct Values:** 2

### reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.582 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 28.1732 chars
- **Distinct Values:** 5,571

</details>

</details>

---

## postgres2_company_data {#postgres2-company-data}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_company_data`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 20

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3.0 to 27,649.0
- **Average:** 13,333.095348837209
- **Distinct Values:** 430

### auth_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.967441860465115 chars
- **Distinct Values:** 430

### company_name

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 12.26046511627907 chars
- **Distinct Values:** 428

### company_sheet

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 70.46976744186047 chars
- **Distinct Values:** 360

### convenient_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.158139534883722 chars
- **Distinct Values:** 428

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 430

### refresh_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.790697674418606 chars
- **Distinct Values:** 428

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_csat_survey_responses {#postgres2-csat-survey-responses}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_csat_survey_responses`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 289

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,219.0
- **Average:** 6,061.3139
- **Distinct Values:** 79

### assigned_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 219.0 to 50,949.0
- **Average:** 36,353.54660390045
- **Distinct Values:** 410
- **Null %:** 25.7%

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 4,950.0 to 87,329,912.0
- **Average:** 73,790,359.94189997
- **Distinct Values:** 9,911

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10,013,014.0 to 89,134,423.0
- **Average:** 76,479,264.7855
- **Distinct Values:** 9,999

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,995

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### feedback_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 21.5945 chars
- **Distinct Values:** 4,118

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 467,596,542.0 to 639,049,546.0
- **Average:** 549,459,678.8599001
- **Distinct Values:** 9,999

### rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.5854
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,993

</details>

</details>

---

## postgres2_draftimprover {#postgres2-draftimprover}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_draftimprover`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 248

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 27,678.0
- **Average:** 4,261.1514
- **Distinct Values:** 49

### agent_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 51,847.0
- **Average:** 42,325.58470000001
- **Distinct Values:** 156

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 345.0
- **Average:** 20.640700000000002
- **Distinct Values:** 119

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 9,657,924.0 to 103,665,290.0
- **Average:** 101,723,910.61470002
- **Distinct Values:** 4,075

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### latency

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.22318400093354285 to 11.49059069599025
- **Average:** 0.7803427391986686
- **Distinct Values:** 10,001

### prompt_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 119.0 to 395.0
- **Average:** 139.8091
- **Distinct Values:** 115

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,575

### total_cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.00036799999999999995 to 0.002565
- **Average:** 0.0005019901000000002
- **Distinct Values:** 822

### total_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 122.0 to 740.0
- **Average:** 160.4498
- **Distinct Values:** 201

</details>

</details>

---

## postgres2_gpt_langgraph_qna {#postgres2-gpt-langgraph-qna}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpt_langgraph_qna`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,190

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 352.1369 chars
- **Distinct Values:** 8,264

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,416

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### metadata_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,998,912.0 to 3,438,930.0
- **Average:** 2,884,548.1365
- **Distinct Values:** 9,998

### question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 61.7875 chars
- **Distinct Values:** 7,409

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_gpt_langgraph_qna_raw {#postgres2-gpt-langgraph-qna-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpt_langgraph_qna_raw`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,190

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 352.1369 chars
- **Distinct Values:** 8,264

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,416

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### metadata_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,998,912.0 to 3,438,930.0
- **Average:** 2,884,548.1365
- **Distinct Values:** 9,998

### question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 61.7875 chars
- **Distinct Values:** 7,409

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_gptanswer {#postgres2-gptanswer}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptanswer`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,673

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 280.2102 chars
- **Distinct Values:** 9,479

### context_added_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 42.1956 chars
- **Distinct Values:** 9,032

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,891

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### is_cached

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### metadata_id

- **Type:** `Float`
- **Semantic Type:** `FK`
- **Nullable:** No
- **Foreign Key:** References field ID `647547`
- **Range:** 35.0 to 668,930.0
- **Average:** 608,975.6991
- **Distinct Values:** 10,000

### question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 31.4865 chars
- **Distinct Values:** 8,807

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### translated_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.8276 chars
- **Distinct Values:** 8,639

### whatsapp_answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 299.093 chars
- **Distinct Values:** 9,774

</details>

</details>

---

## postgres2_gptanswer_raw {#postgres2-gptanswer-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptanswer_raw`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 232.4914 chars
- **Distinct Values:** 7,374

### context_added_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 42.862 chars
- **Distinct Values:** 8,336

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,940

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### is_cached

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1362
- **Distinct Values:** 2

### metadata_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 35.0 to 45,063.0
- **Average:** 24,719.9897
- **Distinct Values:** 9,999

### question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.6826 chars
- **Distinct Values:** 8,159

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### translated_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 30.6337 chars
- **Distinct Values:** 8,061

### whatsapp_answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 262.486 chars
- **Distinct Values:** 6,747

</details>

</details>

---

## postgres2_gptbotcost {#postgres2-gptbotcost}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotcost`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 574.0
- **Average:** 11.926400000000005
- **Distinct Values:** 168

### cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 0.05041551
- **Average:** 0.00213348214
- **Distinct Values:** 2,195

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,782

### embedding_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 57.0
- **Average:** 0.8595
- **Distinct Values:** 45

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### metadata_id

- **Type:** `Float`
- **Semantic Type:** `FK`
- **Nullable:** No
- **Foreign Key:** References field ID `647547`
- **Range:** 1.0 to 123,504.0
- **Average:** 24,476.7117
- **Distinct Values:** 5,998

### process

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.1578 chars
- **Distinct Values:** 7

### prompt_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 13,864.0
- **Average:** 398.7646
- **Distinct Values:** 789

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tavily_calls

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### total_chars

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2,517.0
- **Average:** 52.4794
- **Distinct Values:** 271

### total_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 13,913.0
- **Average:** 410.691
- **Distinct Values:** 871

</details>

</details>

---

## postgres2_gptbotcost_raw {#postgres2-gptbotcost-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotcost_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 273.0
- **Average:** 11.894800000000002
- **Distinct Values:** 155

### cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 0.041792300000000004
- **Average:** 0.002125577275999998
- **Distinct Values:** 2,014

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,875

### embedding_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 57.0
- **Average:** 0.9183
- **Distinct Values:** 45

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### metadata_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6,686.0
- **Average:** 3,354.2251
- **Distinct Values:** 5,948

### process

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.213 chars
- **Distinct Values:** 7

### prompt_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 13,893.0
- **Average:** 412.1227
- **Distinct Values:** 784

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tavily_calls

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### total_chars

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1,590.0
- **Average:** 49.9932
- **Distinct Values:** 213

### total_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 13,921.0
- **Average:** 424.0175
- **Distinct Values:** 864

</details>

</details>

---

## postgres2_gptbotlatency {#postgres2-gptbotlatency}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotlatency`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,317

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### metadata_id

- **Type:** `Float`
- **Semantic Type:** `FK`
- **Nullable:** No
- **Foreign Key:** References field ID `647547`
- **Range:** 106,710.0 to 233,783.0
- **Average:** 131,569.2946
- **Distinct Values:** 6,342

### process

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 11.6455 chars
- **Distinct Values:** 7

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### time_taken

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.3415517807006836 to 612.9374957671389
- **Average:** 3.4933474602692884
- **Distinct Values:** 9,995

</details>

</details>

---

## postgres2_gptintentredirection {#postgres2-gptintentredirection}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptintentredirection`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 640

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,992

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### gpt_intent

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.4308 chars
- **Distinct Values:** 3,656

### gpt_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 7.0 to 100.0
- **Average:** 67.13065
- **Distinct Values:** 18

### metadata_id

- **Type:** `Float`
- **Semantic Type:** `FK`
- **Nullable:** No
- **Foreign Key:** References field ID `647547`
- **Range:** 2,704.0 to 668,905.0
- **Average:** 172,875.4579
- **Distinct Values:** 10,000

### rasa_intents

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 417.5318 chars
- **Distinct Values:** 9,411

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### top_rasa_intent

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.1084 chars
- **Distinct Values:** 190

### top_rasa_intent_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 0.0 to 0.5574802160263062
- **Average:** 0.2956081643219292
- **Distinct Values:** 9,405

</details>

</details>

---

## postgres2_gptmetadata {#postgres2-gptmetadata}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptmetadata`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 572

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 39.0
- **Average:** 38.978
- **Distinct Values:** 3

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 100,452,530.0
- **Average:** 91,859,275.6245
- **Distinct Values:** 8,207

### conversation_uuid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 35.9892 chars
- **Distinct Values:** 8,207

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,979

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 33,901.0
- **Average:** 933.1791
- **Distinct Values:** 4

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 726,903,022.0
- **Average:** 668,755,438.5564
- **Distinct Values:** 8,955

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_gptmetadata_raw {#postgres2-gptmetadata-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptmetadata_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 11,225.0
- **Average:** 1,711.163
- **Distinct Values:** 15

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 71,526,145.0
- **Average:** 69,013,315.46449988
- **Distinct Values:** 4,258

### conversation_uuid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 35.9604 chars
- **Distinct Values:** 4,257

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,583

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 33,467.0
- **Average:** 7,997.3242
- **Distinct Values:** 32

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** -1.0 to 498,599,883.0
- **Average:** 495,993,506.7446
- **Distinct Values:** 5,840

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_gpttranslation {#postgres2-gpttranslation}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpttranslation`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,879

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### metadata_id

- **Type:** `Float`
- **Semantic Type:** `FK`
- **Nullable:** No
- **Foreign Key:** References field ID `647547`
- **Range:** 480,534.0 to 494,948.0
- **Average:** 487,766.1308
- **Distinct Values:** 9,999

### source_text

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 36.8805 chars
- **Distinct Values:** 9,161

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### translated_text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 38.1538 chars
- **Distinct Values:** 8,674

### translation_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.9839 chars
- **Distinct Values:** 2

</details>

</details>

---

## postgres2_ndr {#postgres2-ndr}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_ndr`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,539

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 27,932.0 to 27,932.0
- **Average:** 27,932.0
- **Distinct Values:** 1

### awb

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.049645390070921 chars
- **Distinct Values:** 4,703

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 18.0 to 14,717.0
- **Average:** 7,479.528109323646
- **Distinct Values:** 5,509

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,773

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,779

### modified_values

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 53.16398546964193 chars
- **Distinct Values:** 520

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### template_display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 8.0
- **Average:** 3.392146687424321
- **Distinct Values:** 6

### template_message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1,009,948,724.0
- **Average:** 960,145,495.0280229
- **Distinct Values:** 5,781

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,776

### user_entered_values

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 37.151184916104484 chars
- **Distinct Values:** 1,109

### wa_phone_no

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.998270195467912 chars
- **Distinct Values:** 4,457

</details>

</details>

---

## postgres2_ndr_raw {#postgres2-ndr-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_ndr_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,544

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 27,932.0 to 27,932.0
- **Average:** 27,932.0
- **Distinct Values:** 1

### awb

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.04817820756346 chars
- **Distinct Values:** 4,703

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 18.0 to 14,717.0
- **Average:** 7,471.0485235710585
- **Distinct Values:** 5,509

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,773

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,779

### modified_values

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 53.63581419443965 chars
- **Distinct Values:** 521

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### template_display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 8.0
- **Average:** 3.3919875669141772
- **Distinct Values:** 6

### template_message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1,009,948,724.0
- **Average:** 959,609,808.2085996
- **Distinct Values:** 5,781

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,786

### user_entered_values

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 37.59419789328268 chars
- **Distinct Values:** 1,111

### wa_phone_no

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.998273182524606 chars
- **Distinct Values:** 4,457

</details>

</details>

---

## postgres2_outbound_feedbacks {#postgres2-outbound-feedbacks}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_outbound_feedbacks`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 141

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 51.0 to 27,138.0
- **Average:** 4,824.2162
- **Distinct Values:** 50

### conv_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.0669 chars
- **Distinct Values:** 9,845

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,975

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### feedback

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.1752 chars
- **Distinct Values:** 6

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 30,219.0
- **Average:** 11,281.7534
- **Distinct Values:** 65

### followup_feedback

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6241 chars
- **Distinct Values:** 10

### order_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0125 chars
- **Distinct Values:** 13

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,966

</details>

</details>

---

## postgres2_outbound_feedbacks_raw {#postgres2-outbound-feedbacks-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_outbound_feedbacks_raw`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 16

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 31.0
- **Average:** 30.994
- **Distinct Values:** 2

### conv_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.7338 chars
- **Distinct Values:** 9,640

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,879

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### feedback

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.0828 chars
- **Distinct Values:** 3

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 30,249.0
- **Average:** 933.7679433537174
- **Distinct Values:** 4
- **Null %:** 37.9%

### followup_feedback

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.8309 chars
- **Distinct Values:** 7

### order_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,822

</details>

</details>

---

## postgres2_sentimentemotionanalyzer {#postgres2-sentimentemotionanalyzer}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_sentimentemotionanalyzer`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 3

### conv_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.9310344827586206 chars
- **Distinct Values:** 15

### cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0027745 to 0.0034244999999999996
- **Average:** 0.0030984827586206898
- **Distinct Values:** 29

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 29

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 29

### latency

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.287287 to 3.034108
- **Average:** 2.025382896551724
- **Distinct Values:** 29

### output

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 520.4827586206897 chars
- **Distinct Values:** 29

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres2_summarizer {#postgres2-summarizer}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_summarizer`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 291

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 56.0
- **Average:** 52.0258
- **Distinct Values:** 4

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 15.0 to 535.0
- **Average:** 59.52179999999999
- **Distinct Values:** 227

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 62,663,528.0 to 103,639,476.0
- **Average:** 101,444,378.98619999
- **Distinct Values:** 9,696

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### latency

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.3149709808640182 to 779.8253362600226
- **Average:** 1.2955289934036158
- **Distinct Values:** 9,997

### number_of_messages

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 408.0
- **Average:** 16.9792
- **Distinct Values:** 110

### prompt_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 161.0 to 6,743.0
- **Average:** 626.4462000000002
- **Distinct Values:** 1,255

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,777

### total_cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.000555 to 0.020341
- **Average:** 0.0021174258000000025
- **Distinct Values:** 3,982

### total_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 179.0 to 6,771.0
- **Average:** 685.968
- **Distinct Values:** 1,329

</details>

</details>

---

## postgres_account_users {#postgres-account-users}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_account_users`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,298

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,452.0
- **Average:** 17,273.2150106503
- **Distinct Values:** 1,631

### automation_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.5935346447813558
- **Distinct Values:** 2

### billable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9466634776369289
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,800

### crm_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9142964540784363
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 7,982

### inviter_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 53,772.0
- **Average:** 21,422.171641791047
- **Distinct Values:** 704
- **Null %:** 37.9%

### marketing_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.5957900012529758
- **Distinct Values:** 2

### role

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.6943991980954768
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,598

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,795.0
- **Average:** 30,706.33830347075
- **Distinct Values:** 4,802

</details>

</details>

---

## postgres_account_users_raw {#postgres-account-users-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_account_users_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 853

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,141.0
- **Average:** 14,448.6534
- **Distinct Values:** 1,315

### automation_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2085
- **Distinct Values:** 2

### billable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9466634776369289
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,554

### crm_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3635
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 6,428

### inviter_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 53,031.0
- **Average:** 19,494.76964729986
- **Distinct Values:** 650
- **Null %:** 31.7%

### marketing_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2089
- **Distinct Values:** 2

### role

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.7002
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,788

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,337.0
- **Average:** 29,544.3029
- **Distinct Values:** 4,174

</details>

</details>

---

## postgres_accounts {#postgres-accounts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_accounts`

<details>
<summary><strong>📊 Columns (49 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 527

### agent_analytic_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.000898069151324652
- **Distinct Values:** 2

### assignment_logic

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1974
- **Distinct Values:** 2

### auto_resolve_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** Yes
- **Range:** 1.0 to 10.0
- **Average:** 4.6
- **Distinct Values:** 3
- **Null %:** 99.8%

### billing_email

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2846879209699147 chars
- **Distinct Values:** 12

### concurrency_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.013920071845532105
- **Distinct Values:** 2

### concurrency_limit

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1,000.0
- **Average:** 5.475033738191634
- **Distinct Values:** 12
- **Null %:** 0.2%

### contact_masking

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0002
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,586

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.997530309833857 chars
- **Distinct Values:** 22

### customer_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 3
- **Null %:** 97.3%

### domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.039964077233947 chars
- **Distinct Values:** 1,270

### enforce_tagging

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.015267175572519083
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,586

### feature_flags

- **Type:** `Float`
- **Nullable:** No
- **Range:** 14.0 to 59,630.0
- **Average:** 3,398.487651549169
- **Distinct Values:** 52

### grace_added_on

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### grace_extension

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.026493039964077234
- **Distinct Values:** 2

### hide_all_tab

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.012348450830713965
- **Distinct Values:** 2

### hide_all_tab_for_supervisor

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### hide_bot_conversations

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0029187247418051188
- **Distinct Values:** 2

### hide_out_of_stock

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.006286484059272564
- **Distinct Values:** 2

### hide_queued_tab

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.005163897620116749
- **Distinct Values:** 2

### hide_queued_tab_for_supervisor

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### is_enterprise

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.05298607992815447
- **Distinct Values:** 2

### locale

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 23.0
- **Average:** 0.08419398293668612
- **Distinct Values:** 9

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.02132914234396 chars
- **Distinct Values:** 1,569

### on_grace_period

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.13403682083520432
- **Distinct Values:** 2

### on_shopify_custom_plan

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.012797485406376291
- **Distinct Values:** 2

### partner_billed

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### password

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 1,586

### payment_pending

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.08037718904355635
- **Distinct Values:** 2

### preferred_billing_currency

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6686124831612034
- **Distinct Values:** 2

### settings_flags

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shopify_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.956443646160754 chars
- **Distinct Values:** 425

### shopify_app_reinstalled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.012348450830713965
- **Distinct Values:** 2

### shopify_country_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.5226762460709474 chars
- **Distinct Values:** 45

### shopify_country_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.7903008531656937 chars
- **Distinct Values:** 42

### shopify_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.05927256398742703
- **Distinct Values:** 2

### shopify_store_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 7.320835204310732 chars
- **Distinct Values:** 392

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 1.7555006735518635 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### support_email

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0682532555006734 chars
- **Distinct Values:** 3

### template_last_synced_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 275
- **Null %:** 93.4%

### ums_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.09788953749438707
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,111

### username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 41.27727885047149 chars
- **Distinct Values:** 1,586

### website_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 1.1957790749887742 chars
- **Distinct Values:** 76

</details>

</details>

---

## postgres_agent_agent_analytics {#postgres-agent-agent-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_agent_agent_analytics`

<details>
<summary><strong>📊 Columns (26 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 63

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 23,996.0
- **Average:** 3,922.5685
- **Distinct Values:** 165

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 91,137.9
- **Average:** 68.9324158918005
- **Distinct Values:** 1,767
- **Null %:** 40.8%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 102,343.35
- **Average:** 459.8942991024288
- **Distinct Values:** 4,148
- **Null %:** 24.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26.0
- **Average:** 1.2586999999999997
- **Distinct Values:** 26

### assignee_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 45,169.0
- **Average:** 19,248.159
- **Distinct Values:** 475

### average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 172,818.12
- **Average:** 175.28261876584955
- **Distinct Values:** 2,600
- **Null %:** 40.8%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 9,921,112.0 to 62,575,427.0
- **Average:** 61,757,163.9039
- **Distinct Values:** 8,048

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,599

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,923
- **Null %:** 40.8%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6,622

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10.0 to 30,027.0
- **Average:** 7,130.9525
- **Distinct Values:** 312

### is_auto_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0867
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0007
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2527
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8042
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,058
- **Null %:** 40.8%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 3,936
- **Null %:** 42.7%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 6,472
- **Null %:** 24.2%

### self_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4531
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,005

</details>

</details>

---

## postgres_agent_analytics {#postgres-agent-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_agent_analytics`

<details>
<summary><strong>📊 Columns (26 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,783

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,047.0
- **Average:** 2,934.0706999999998
- **Distinct Values:** 276

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 538,887.14
- **Average:** 330.5876945442107
- **Distinct Values:** 2,157
- **Null %:** 41.5%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** -260.19 to 702,447.42
- **Average:** 568.2310476925055
- **Distinct Values:** 3,915
- **Null %:** 22.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 79.0
- **Average:** 1.2835
- **Distinct Values:** 28

### assignee_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 50,150.0
- **Average:** 12,236.8013
- **Distinct Values:** 1,637

### average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 734,825.17
- **Average:** 449.8389512711865
- **Distinct Values:** 2,886
- **Null %:** 43.4%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 9,809.0 to 76,260,479.0
- **Average:** 43,181,510.6101
- **Distinct Values:** 9,997

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,783
- **Null %:** 42.2%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,996

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 10.0 to 33,622.0
- **Average:** 5,375.366049963414
- **Distinct Values:** 612
- **Null %:** 4.3%

### is_auto_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0265
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0923
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2257
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8023
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,783
- **Null %:** 42.2%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,288
- **Null %:** 47.1%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 7,772
- **Null %:** 22.3%

### self_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1342
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,994

</details>

</details>

---

## postgres_attendances {#postgres-attendances}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_attendances`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 77

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,117.0
- **Average:** 6,620.4225
- **Distinct Values:** 1,208

### availability

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 0.9541
- **Distinct Values:** 5

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,073

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### reason

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,073

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 50,282.0
- **Average:** 22,403.296
- **Distinct Values:** 230

</details>

</details>

---

## postgres_automation_rule_analytic {#postgres-automation-rule-analytic}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rule_analytic`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,749

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,980.0
- **Average:** 20,572.8113
- **Distinct Values:** 53

### automation_rule_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 463.0 to 4,370.0
- **Average:** 3,707.6505
- **Distinct Values:** 91

### conversation_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,319

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 52,808,608.0 to 163,129,569.0
- **Average:** 108,212,191.1625
- **Distinct Values:** 3,338

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,234

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### rule_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.2636 chars
- **Distinct Values:** 69

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,234

</details>

</details>

---

## postgres_automation_rule_analytic_raw {#postgres-automation-rule-analytic-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rule_analytic_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 949

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,052.0
- **Average:** 22,022.1139
- **Distinct Values:** 61

### automation_rule_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 463.0 to 4,370.0
- **Average:** 3,665.0571
- **Distinct Values:** 121

### conversation_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,146

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 55,870,942.0 to 132,686,471.0
- **Average:** 116,586,861.3691
- **Distinct Values:** 4,163

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,360

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### rule_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.0336 chars
- **Distinct Values:** 101

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,360

</details>

</details>

---

## postgres_automation_rules {#postgres-automation-rules}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rules`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 171

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 27,586.0
- **Average:** 16,688.174019607843
- **Distinct Values:** 115

### actions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 182.0906862745098 chars
- **Distinct Values:** 257

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6642156862745098
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 308.50245098039215 chars
- **Distinct Values:** 329

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 328

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 8.034313725490197 chars
- **Distinct Values:** 70

### event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 17.32107843137255 chars
- **Distinct Values:** 8

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 330

### is_test

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 14.91421568627451 chars
- **Distinct Values:** 298

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### test_numbers

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.23529411764705882 chars
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 407

</details>

</details>

---

## postgres_billing_attendances {#postgres-billing-attendances}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_billing_attendances`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 449

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,763.0
- **Average:** 17,651.595760931836
- **Distinct Values:** 707

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### current_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7790719877792629
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,237

### previous_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.21348100057284705
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### toggled_by

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 55,131.0
- **Average:** 48,905.10743801653
- **Distinct Values:** 288
- **Null %:** 93.1%

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 55,131.0
- **Average:** 37,511.36719495895
- **Distinct Values:** 3,094

</details>

</details>

---

## postgres_billing_attendances_raw {#postgres-billing-attendances-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_billing_attendances_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 449

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,763.0
- **Average:** 17,651.595760931836
- **Distinct Values:** 707

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### current_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7790719877792629
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,237

### previous_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.21348100057284705
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### toggled_by

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 55,131.0
- **Average:** 48,905.10743801653
- **Distinct Values:** 288
- **Null %:** 93.1%

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 55,131.0
- **Average:** 37,511.36719495895
- **Distinct Values:** 3,094

</details>

</details>

---

## postgres_bot_cdc_bot_csat {#postgres-bot-cdc-bot-csat}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_bot_cdc_bot_csat`

<details>
<summary><strong>📊 Columns (20 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _ab_cdc_lsn

- **Type:** `Float`
- **Nullable:** No
- **Range:** 89,320,491,998,048.0 to 89,321,918,201,280.0
- **Average:** 89,321,601,473,766.9
- **Distinct Values:** 3

### _ab_cdc_updated_at

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 39.0 chars
- **Distinct Values:** 3

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 36

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 51.0 to 54.0
- **Average:** 53.6136
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,895

### csat_comment

- **Type:** `Text`
- **Semantic Type:** `Comment`
- **Nullable:** No
- **Avg Length:** 0.0397 chars
- **Distinct Values:** 14

### csat_reason

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.449 chars
- **Distinct Values:** 61

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 1.0 to 5.0
- **Average:** 3.28051948051948
- **Distinct Values:** 6
- **Null %:** 88.4%

### display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,608.0 to 5,324,628.0
- **Average:** 4,489,666.318900004
- **Distinct Values:** 8,000

### event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0101 chars
- **Distinct Values:** 7

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 115.0 to 33,743.0
- **Average:** 5,024.974397439744
- **Distinct Values:** 7
- **Null %:** 0.0%

### is_csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1749
- **Distinct Values:** 2

### is_reminder_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1943
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 509,540,021.0 to 738,668,456.0
- **Average:** 563,652,139.0222999
- **Distinct Values:** 9,997

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.8533 chars
- **Distinct Values:** 1,234

### sender_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.999 chars
- **Distinct Values:** 6,892

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres_bot_cdc_bot_csat_raw {#postgres-bot-cdc-bot-csat-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_bot_cdc_bot_csat_raw`

<details>
<summary><strong>📊 Columns (20 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _ab_cdc_lsn

- **Type:** `Float`
- **Nullable:** No
- **Range:** 122,089,095,213,168.0 to 122,089,095,213,168.0
- **Average:** 122,089,095,213,168.0
- **Distinct Values:** 1

### _ab_cdc_updated_at

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 39.0 chars
- **Distinct Values:** 1

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 18

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 39.0
- **Average:** 39.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,987

### csat_comment

- **Type:** `Text`
- **Semantic Type:** `Comment`
- **Nullable:** No
- **Avg Length:** 0.151 chars
- **Distinct Values:** 56

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6946 chars
- **Distinct Values:** 28

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 1.0 to 5.0
- **Average:** 3.913764510779436
- **Distinct Values:** 6
- **Null %:** 94.0%

### display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 622,427.0 to 2,749,238.0
- **Average:** 2,601,268.1216999986
- **Distinct Values:** 9,780

### event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.6695 chars
- **Distinct Values:** 5

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 894.0 to 894.0
- **Average:** 894.0
- **Distinct Values:** 1

### is_csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1255
- **Distinct Values:** 2

### is_reminder_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 775,425,654.0 to 822,907,778.0
- **Average:** 801,349,033.7265
- **Distinct Values:** 9,999

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9998 chars
- **Distinct Values:** 9,664

### sender_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.7673 chars
- **Distinct Values:** 9,667

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres_broadcasts {#postgres-broadcasts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_broadcasts`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 201

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,036.0
- **Average:** 5,818.9355
- **Distinct Values:** 148

### content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 328.999 chars
- **Distinct Values:** 1,885

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 10.3188 chars
- **Distinct Values:** 95

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### is_cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0042
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 7.9475 chars
- **Distinct Values:** 1,608

### scheduled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0821
- **Distinct Values:** 2

### scheduled_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 640
- **Null %:** 91.8%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### template_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 709.0 to 127,727.0
- **Average:** 79,128.0256
- **Distinct Values:** 2,074

### total

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 179,872.0
- **Average:** 1,919.2989
- **Distinct Values:** 1,897

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,975

</details>

</details>

---

## postgres_channel_facebook_pages {#postgres-channel-facebook-pages}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_facebook_pages`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 34

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,607.0
- **Average:** 12,185.130857648099
- **Distinct Values:** 368

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 932

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 430
- **Null %:** 51.1%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,113

### instagram_add_on

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.497789566755084
- **Distinct Values:** 2

### instagram_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.32183908045977 chars
- **Distinct Values:** 404

### page_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 129.4076038903625 chars
- **Distinct Values:** 1,079

### page_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 23.122900088417328 chars
- **Distinct Values:** 839

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 937

### user_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 125.06366047745358 chars
- **Distinct Values:** 1,021

</details>

</details>

---

## postgres_channel_gupshup_enterprises {#postgres-channel-gupshup-enterprises}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_gupshup_enterprises`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,537.0
- **Average:** 8,581.569711538461
- **Distinct Values:** 251

### catalog_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.6899038461538463 chars
- **Distinct Values:** 33

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 416

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 124
- **Null %:** 57.9%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 416

### pass

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.966346153846154 chars
- **Distinct Values:** 346

### pass_hsm

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.997596153846154 chars
- **Distinct Values:** 346

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.899038461538462 chars
- **Distinct Values:** 332

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 364

### user

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.838942307692308 chars
- **Distinct Values:** 338

### user_hsm

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.846153846153847 chars
- **Distinct Values:** 337

</details>

</details>

---

## postgres_channel_three_sixty_dialogs {#postgres-channel-three-sixty-dialogs}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_three_sixty_dialogs`

<details>
<summary><strong>📊 Columns (19 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 32

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 27,645.0
- **Average:** 22,312.822281167108
- **Distinct Values:** 280

### api_key

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.862068965517242 chars
- **Distinct Values:** 168

### catalog_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.5676392572944297 chars
- **Distinct Values:** 13

### channel_live

- **Type:** `Integer`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3050397877984085
- **Distinct Values:** 2

### channel_submitted

- **Type:** `Integer`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.06896551724137931
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 372

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 175
- **Null %:** 49.3%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 372

### on_cloud

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.38726790450928383
- **Distinct Values:** 2

### onboarding_started_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 2
- **Null %:** 99.7%

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.893899204244033 chars
- **Distinct Values:** 360

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### template_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.07161803713527852
- **Distinct Values:** 2

### three_sixty_channel_id

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 3.647214854111406 chars
- **Distinct Values:** 167

### three_sixty_client_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.570291777188329 chars
- **Distinct Values:** 146

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 360

### waba_account_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.6684350132625996 chars
- **Distinct Values:** 158

</details>

</details>

---

## postgres_channel_whatsapp_cloud_apis {#postgres-channel-whatsapp-cloud-apis}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_whatsapp_cloud_apis`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 28,435.0
- **Average:** 12,442.135338345865
- **Distinct Values:** 108

### auth_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 172.08270676691728 chars
- **Distinct Values:** 128

### catalog_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.5037593984962405 chars
- **Distinct Values:** 34

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 133

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 45
- **Null %:** 63.2%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 133

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.721804511278197 chars
- **Distinct Values:** 133

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 128

### wa_business_account_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.661654135338345 chars
- **Distinct Values:** 126

### wa_business_account_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.969924812030076 chars
- **Distinct Values:** 116

### wa_phone_number_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.503759398496241 chars
- **Distinct Values:** 126

</details>

</details>

---

## postgres_channel_whatsapp_cloud_apis_raw {#postgres-channel-whatsapp-cloud-apis-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_whatsapp_cloud_apis_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 28,435.0
- **Average:** 12,458.814814814816
- **Distinct Values:** 108

### auth_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 172.2 chars
- **Distinct Values:** 128

### catalog_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.674074074074074 chars
- **Distinct Values:** 34

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 133

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 45
- **Null %:** 63.7%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 133

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.651851851851852 chars
- **Distinct Values:** 135

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 130

### wa_business_account_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.666666666666666 chars
- **Distinct Values:** 126

### wa_business_account_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.985185185185186 chars
- **Distinct Values:** 116

### wa_phone_number_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.511111111111111 chars
- **Distinct Values:** 126

</details>

</details>

---

## postgres_contacts {#postgres-contacts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_contacts`

<details>
<summary><strong>📊 Columns (19 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,742

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,089.0
- **Average:** 3,078.055
- **Distinct Values:** 323

### additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 63.7635 chars
- **Distinct Values:** 906

### address

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### conversations_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### custom_attributes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3816 chars
- **Distinct Values:** 43

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.1175 chars
- **Distinct Values:** 1,761

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### external_uuid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### identifier

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.009 chars
- **Distinct Values:** 630

### instagram_username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.5572 chars
- **Distinct Values:** 415

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 9.5572 chars
- **Distinct Values:** 7,553

### opt_in

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9977
- **Distinct Values:** 2

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.7687 chars
- **Distinct Values:** 7,292

### pubsub_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 10,000

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,976

</details>

</details>

---

## postgres_conv_agent_analytics {#postgres-conv-agent-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_analytics`

<details>
<summary><strong>📊 Columns (26 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 729

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,518.0
- **Average:** 7,598.544300000001
- **Distinct Values:** 242

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 89,797.98
- **Average:** 136.7615272591486
- **Distinct Values:** 1,824
- **Null %:** 46.4%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** -44.06 to 115,257.89
- **Average:** 594.6920062606719
- **Distinct Values:** 4,165
- **Null %:** 29.7%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 25.0
- **Average:** 1.1091
- **Distinct Values:** 24

### assignee_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 51,601.0
- **Average:** 28,778.2854
- **Distinct Values:** 1,073

### average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 89,797.98
- **Average:** 173.89005414488423
- **Distinct Values:** 2,014
- **Null %:** 46.4%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 11,442,558.0 to 99,600,632.0
- **Average:** 72,022,586.14970003
- **Distinct Values:** 9,978

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,983

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,371
- **Null %:** 46.2%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,980

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10.0 to 34,283.0
- **Average:** 13,504.4864
- **Distinct Values:** 537

### is_auto_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1021
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0048
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1783
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7221
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,376
- **Null %:** 46.2%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,631
- **Null %:** 43.6%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 7,027
- **Null %:** 29.7%

### self_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3502
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,986

</details>

</details>

---

## postgres_conv_agent_analytics_raw {#postgres-conv-agent-analytics-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_analytics_raw`

<details>
<summary><strong>📊 Columns (26 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 53

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 23,996.0
- **Average:** 3,922.2389
- **Distinct Values:** 165

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 91,137.9
- **Average:** 68.96738159675238
- **Distinct Values:** 1,767
- **Null %:** 40.9%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 102,343.35
- **Average:** 459.8904197465683
- **Distinct Values:** 4,148
- **Null %:** 24.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26.0
- **Average:** 1.2581
- **Distinct Values:** 26

### assignee_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 48,931.0
- **Average:** 19,256.3994
- **Distinct Values:** 477

### average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 172,818.12
- **Average:** 175.37059539918812
- **Distinct Values:** 2,600
- **Null %:** 40.9%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 9,921,112.0 to 65,914,696.0
- **Average:** 61,757,860.22309998
- **Distinct Values:** 8,050

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,600

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,921
- **Null %:** 40.9%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6,623

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10.0 to 30,027.0
- **Average:** 7,133.9139
- **Distinct Values:** 312

### is_auto_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0867
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0011
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2528
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8042
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,056
- **Null %:** 40.9%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 3,936
- **Null %:** 42.7%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 6,473
- **Null %:** 24.2%

### self_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4533
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,007

</details>

</details>

---

## postgres_conv_agent_bot_inboxes {#postgres-conv-agent-bot-inboxes}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_bot_inboxes`

<details>
<summary><strong>📊 Columns (21 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,554.0
- **Average:** 11,006.223157894738
- **Distinct Values:** 409

### agent_bot_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6,113.0
- **Average:** 2,503.6431578947368
- **Distinct Values:** 408

### bot_percent

- **Type:** `Float`
- **Semantic Type:** `Share`
- **Nullable:** No
- **Range:** 0.0 to 100.0
- **Average:** 68.42105263157895
- **Distinct Values:** 2

### bot_percent_off

- **Type:** `Float`
- **Semantic Type:** `Share`
- **Nullable:** No
- **Range:** -5.0 to 101.0
- **Average:** 68.52947368421053
- **Distinct Values:** 8

### conv_marketing_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 21.57578947368421 chars
- **Distinct Values:** 11

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 949

### csat_with_bot

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7463157894736843
- **Distinct Values:** 2

### delivery_medium

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 950

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 6.0 to 34,266.0
- **Average:** 15,776.814736842109
- **Distinct Values:** 950

### international_number_allowed

- **Type:** `Integer`
- **Semantic Type:** `Quantity`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9978947368421053
- **Distinct Values:** 2

### is_test

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.028421052631578948
- **Distinct Values:** 2

### only_conv_marketing

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.007368421052631579
- **Distinct Values:** 2

### reply_to_comment

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.031578947368421054
- **Distinct Values:** 2

### reply_to_template

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.11052631578947368
- **Distinct Values:** 3

### test_numbers

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 20.352631578947367 chars
- **Distinct Values:** 221

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 886

</details>

</details>

---

## postgres_conv_agent_bots {#postgres-conv-agent-bots}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_bots`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 422

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.037914691943127965 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 422

### hide_input_for_bot_conversations

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 11.338862559241706 chars
- **Distinct Values:** 421

### outgoing_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 58.11374407582938 chars
- **Distinct Values:** 419

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 422

</details>

</details>

---

## postgres_conv_ar_internal_metadata {#postgres-conv-ar-internal-metadata}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_ar_internal_metadata`

<details>
<summary><strong>📊 Columns (7 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2

### key

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 11.0 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2

### value

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 25.0 chars
- **Distinct Values:** 2

</details>

</details>

---

## postgres_conv_billing_plans {#postgres-conv-billing-plans}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_billing_plans`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 73.0
- **Average:** 44.76923076923077
- **Distinct Values:** 13

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 13

### pricing

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 34.0 chars
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### total_convs

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 18,768.0
- **Average:** 2,532.923076923077
- **Distinct Values:** 8

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

### zoho_addon_code

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 22.0 chars
- **Distinct Values:** 1

### zoho_plan_code

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 21.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres_conv_canned_images {#postgres-conv-canned-images}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_canned_images`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### canned_response_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 363.0 to 365.0
- **Average:** 364.0
- **Distinct Values:** 3
- **Null %:** 99.1%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 230

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 230

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 21.408695652173915 chars
- **Distinct Values:** 26

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 230

</details>

</details>

---

## postgres_conv_channel_api {#postgres-conv-channel-api}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_api`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 72.0 to 27,401.0
- **Average:** 13,669.42857142857
- **Distinct Values:** 7

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7
- **Null %:** 14.3%

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 7

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7

### webhook_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 37.857142857142854 chars
- **Distinct Values:** 7

</details>

</details>

---

## postgres_conv_channel_knowlarities {#postgres-conv-channel-knowlarities}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_knowlarities`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 27,006.0
- **Average:** 6,049.846153846154
- **Distinct Values:** 9

### caller_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 13.038461538461538 chars
- **Distinct Values:** 11

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 26

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 18
- **Null %:** 34.6%

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 26

### sr_api_key

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 8

### sr_number

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 28.076923076923077 chars
- **Distinct Values:** 26

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 26

</details>

</details>

---

## postgres_conv_channel_value_firsts {#postgres-conv-channel-value-firsts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_value_firsts`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12.0 to 481.0
- **Average:** 454.94736842105266
- **Distinct Values:** 4

### auth_token

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 17.973684210526315 chars
- **Distinct Values:** 5

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 38

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 3
- **Null %:** 92.1%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 38

### pass

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 18.5 chars
- **Distinct Values:** 8

### phone_number

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 37

### user

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.5 chars
- **Distinct Values:** 6

</details>

</details>

---

## postgres_conv_channel_web_widgets {#postgres-conv-channel-web-widgets}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_web_widgets`

<details>
<summary><strong>📊 Columns (25 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,563.0
- **Average:** 11,983.858741258742
- **Distinct Values:** 523

### closewidgetpopupsetting

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.7874125874125875 chars
- **Distinct Values:** 4

### configsetting

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 175.52027972027972 chars
- **Distinct Values:** 130

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 715

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 191
- **Null %:** 57.8%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 715

### feature_flags

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 2.8965034965034966
- **Distinct Values:** 4

### firsttimepopupsetting

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.836363636363636 chars
- **Distinct Values:** 40

### hmac_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 715

### homepopupsetting

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9944055944055945 chars
- **Distinct Values:** 12

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7846153846153846 chars
- **Distinct Values:** 45

### pre_chat_form_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.043356643356643354
- **Distinct Values:** 2

### pre_chat_form_options

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 7.321678321678322 chars
- **Distinct Values:** 30

### reply_time

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.04055944055944056
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### unreadsetting

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.24055944055944056 chars
- **Distinct Values:** 4

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 603

### website_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 715

### website_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 53.31188811188811 chars
- **Distinct Values:** 650

### welcome_tagline

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.802797202797203 chars
- **Distinct Values:** 60

### welcome_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 1.8447552447552447 chars
- **Distinct Values:** 68

### widget_color

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 114

### widget_zindex

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 98.0 to 2,147,483,001.0
- **Average:** 2,104,976,684.3753502
- **Distinct Values:** 14
- **Null %:** 0.1%

</details>

</details>

---

## postgres_conv_channel_zokos {#postgres-conv-channel-zokos}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_zokos`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 58.0 to 20,465.0
- **Average:** 10,330.0
- **Distinct Values:** 3

### auth_token

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 3

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 3
- **Null %:** 50.0%

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 4

### phone_number

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 4

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4

</details>

</details>

---

## postgres_conv_contact_inboxes {#postgres-conv-contact-inboxes}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_contact_inboxes`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 245

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 9,774,981.0 to 81,341,599.0
- **Average:** 77,787,210.27320006
- **Distinct Values:** 9,991

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,833

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### hmac_verified

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 73.0 to 33,788.0
- **Average:** 17,414.077100000006
- **Distinct Values:** 446

### source_id

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 14.6043 chars
- **Distinct Values:** 10,000

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,833

</details>

</details>

---

## postgres_conv_contact_labels {#postgres-conv-contact-labels}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_contact_labels`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 31,253,478.0 to 94,357,834.0
- **Average:** 82,016,630.60190763
- **Distinct Values:** 1,973

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,986

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,992

### label_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 60,424.0 to 274,934.0
- **Average:** 263,718.3458835342
- **Distinct Values:** 32

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,986

</details>

</details>

---

## postgres_conv_conversation_analytics {#postgres-conv-conversation-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_conversation_analytics`

<details>
<summary><strong>📊 Columns (44 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 591

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 11.0 to 27,084.0
- **Average:** 8,592.1696
- **Distinct Values:** 237

### adjusted_company_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5,100.78
- **Average:** 281.836265060241
- **Distinct Values:** 600
- **Null %:** 90.9%

### adjusted_company_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 14,814.61
- **Average:** 92.14095195530727
- **Distinct Values:** 881
- **Null %:** 55.2%

### adjusted_open_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,175
- **Null %:** 71.5%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 22.0
- **Average:** 0.3357
- **Distinct Values:** 22

### average_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### bot_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1,440.12
- **Average:** 4.269714673913043
- **Distinct Values:** 47
- **Null %:** 77.9%

### bot_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 20.0
- **Average:** 0.4839
- **Distinct Values:** 18

### company_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5,108.45
- **Average:** 315.7605366922234
- **Distinct Values:** 638
- **Null %:** 90.9%

### company_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 14,814.61
- **Average:** 100.17237541899442
- **Distinct Values:** 911
- **Null %:** 55.2%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 30.0
- **Average:** 1.0303
- **Distinct Values:** 26

### conv_open_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,522
- **Null %:** 71.5%

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 65,984,845.0 to 74,425,472.0
- **Average:** 72,896,029.515
- **Distinct Values:** 10,000

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,498

### csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0023
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### first_agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 13,319.51
- **Average:** 250.06490690032857
- **Distinct Values:** 491
- **Null %:** 90.9%

### first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,847
- **Null %:** 35.7%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1,526
- **Null %:** 82.2%

### first_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 50,407.0
- **Average:** 29,679.23085585586
- **Distinct Values:** 400
- **Null %:** 82.2%

### first_bot_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,067
- **Null %:** 77.9%

### first_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,474
- **Null %:** 47.4%

### first_opened_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 33,610.0
- **Average:** 14,385.466000000006
- **Distinct Values:** 449

### is_handled_by_bot

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3102
- **Distinct Values:** 2

### is_handoff

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0911
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5987
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4323
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4475
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,677
- **Null %:** 35.7%

### last_bot_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,119
- **Null %:** 77.9%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,683
- **Null %:** 47.4%

### last_resolution_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 50,192.0
- **Average:** 30,381.87300574346
- **Distinct Values:** 374
- **Null %:** 84.3%

### last_resolution_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,150
- **Null %:** 55.2%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,272
- **Null %:** 55.2%

### manual_agent_handoff

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0059
- **Distinct Values:** 2

### manual_handoff_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 327.0 to 49,924.0
- **Average:** 23,356.28813559322
- **Distinct Values:** 15
- **Null %:** 99.4%

### outbound_status

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3.0
- **Average:** 0.7015182186234818
- **Distinct Values:** 4
- **Null %:** 1.2%

### overall_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 89,655.04
- **Average:** 365.46092960893856
- **Distinct Values:** 1,936
- **Null %:** 55.2%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 6.0
- **Average:** 3.9732
- **Distinct Values:** 7

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,048

</details>

</details>

---

## postgres_conv_conversations {#postgres-conv-conversations}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_conversations`

<details>
<summary><strong>📊 Columns (51 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 306

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 524.0
- **Average:** 66.68900000000001
- **Distinct Values:** 67

### additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 42.5171 chars
- **Distinct Values:** 621

### agent_last_seen_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1,193
- **Null %:** 87.9%

### alert

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0015
- **Distinct Values:** 2

### alert_dispatch_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 61.0
- **Average:** 0.8587
- **Distinct Values:** 22

### assigned_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### assigned_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0063 chars
- **Distinct Values:** 3

### assigned_by_resource_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,019.0 to 1,860.0
- **Average:** 1,350.6666666666667
- **Distinct Values:** 4
- **Null %:** 100.0%

### assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 3.0 to 4,644.0
- **Average:** 522.6980633802817
- **Distinct Values:** 143
- **Null %:** 88.6%

### assignee_version

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### close_dispatch_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 61.0
- **Average:** 0.8587
- **Distinct Values:** 22

### closed_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0086 chars
- **Distinct Values:** 3

### contact_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 303,478.0 to 78,197,325.0
- **Average:** 27,008,842.451800004
- **Distinct Values:** 9,090

### contact_inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 302,880.0 to 31,883,989.0
- **Average:** 27,095,821.66839999
- **Distinct Values:** 9,119

### contact_last_seen_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 285
- **Null %:** 97.1%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,089

### crm_ticket_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 4,522.0 to 10,767,176.0
- **Average:** 3,813,587.8193
- **Distinct Values:** 9,999

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### external_uuid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### facebook_post_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### frt_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### identifier

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0526 chars
- **Distinct Values:** 3

### in_reply_to_email

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8.0 to 727.0
- **Average:** 264.88740000000007
- **Distinct Values:** 115

### is_conv_marketing

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### is_primary

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### last_activity_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,750

### locked

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### messages_count

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### new_filter

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### nrt_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### opened_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 211
- **Null %:** 97.9%

### previous_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,019.0 to 1,860.0
- **Average:** 1,439.5
- **Distinct Values:** 3
- **Null %:** 100.0%

### previous_label_list

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 6.9011 chars
- **Distinct Values:** 259

### primary_conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### rasa_conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### resolution_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0095 chars
- **Distinct Values:** 3

### sla_policy_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### sla_tracking_started_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### starred

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0006
- **Distinct Values:** 2

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6.0
- **Average:** 3.009
- **Distinct Values:** 5

### status_changed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 3
- **Null %:** 100.0%

### team_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### unread

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8911
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,842

### uuid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 10,000

</details>

</details>

---

## postgres_conv_shopify_availed_trials {#postgres-conv-shopify-availed-trials}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_shopify_availed_trials`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 168

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 168

### shop_domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.398809523809524 chars
- **Distinct Values:** 168

### shop_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 26.154761904761905 chars
- **Distinct Values:** 168

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### trial_end

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 131

### trial_start

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 131

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 168

</details>

</details>

---

## postgres_conv_subscriptions {#postgres-conv-subscriptions}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_subscriptions`

<details>
<summary><strong>📊 Columns (22 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,510.0
- **Average:** 14,018.546772068512
- **Distinct Values:** 499

### admin_cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 759

### current_term_end

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 136
- **Null %:** 25.6%

### current_term_start

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 44
- **Null %:** 25.6%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 759

### invoice_close_date

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 288
- **Null %:** 58.6%

### invoice_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 2
- **Null %:** 35.0%

### plan_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 811.0
- **Average:** 316.26218708827406
- **Distinct Values:** 41

### platform

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6956521739130435
- **Distinct Values:** 2

### platform_subscription_id

- **Type:** `Text`
- **Semantic Type:** `Subscription`
- **Nullable:** No
- **Avg Length:** 9.9433465085639 chars
- **Distinct Values:** 570

### previous_billing_end

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 15
- **Null %:** 35.2%

### previous_billing_start

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 16
- **Null %:** 35.2%

### shopify_confirmation_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 12.395256916996047 chars
- **Distinct Values:** 42

### shopify_invoice_pending

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 7.0
- **Average:** 2.8194993412384717
- **Distinct Values:** 5

### trial_end

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 166
- **Null %:** 75.0%

### trial_start

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 134
- **Null %:** 75.0%

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 512

</details>

</details>

---

## postgres_conv_taggings {#postgres-conv-taggings}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_taggings`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No

### context

- **Type:** `Text`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No

### src

- **Type:** `Text`
- **Nullable:** No

### tag_id

- **Type:** `Float`
- **Nullable:** No

### taggable_id

- **Type:** `Float`
- **Nullable:** No

### taggable_type

- **Type:** `Text`
- **Nullable:** No

</details>

</details>

---

## postgres_conv_team_members {#postgres-conv-team-members}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_team_members`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 173

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 358

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### team_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 2,090.0
- **Average:** 1,725.9804469273743
- **Distinct Values:** 129

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 173

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 51,591.0
- **Average:** 36,598.874301675976
- **Distinct Values:** 310

</details>

</details>

---

## postgres_conv_webhook_watchers {#postgres-conv-webhook-watchers}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_webhook_watchers`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No

### account_id

- **Type:** `Float`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### event_name

- **Type:** `Text`
- **Nullable:** No

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No

### failure_reason

- **Type:** `Text`
- **Nullable:** No

### object_id

- **Type:** `Float`
- **Nullable:** No

### object_type

- **Type:** `Text`
- **Nullable:** No

### src

- **Type:** `Text`
- **Nullable:** No

### status

- **Type:** `Float`
- **Nullable:** No

### success_reason

- **Type:** `Text`
- **Nullable:** No

### updated_at

- **Type:** `DateTime`
- **Nullable:** No

### webhook_payload

- **Type:** `Text`
- **Nullable:** No

### webhook_url

- **Type:** `Text`
- **Nullable:** No

</details>

</details>

---

## postgres_conv_working_hour_slots {#postgres-conv-working-hour-slots}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_working_hour_slots`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No

### close_hour

- **Type:** `Float`
- **Nullable:** No

### close_minutes

- **Type:** `Float`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No

### open_hour

- **Type:** `Float`
- **Nullable:** No

### open_minutes

- **Type:** `Float`
- **Nullable:** No

### src

- **Type:** `Text`
- **Nullable:** No

### updated_at

- **Type:** `DateTime`
- **Nullable:** No

### working_hour_id

- **Type:** `Float`
- **Nullable:** No

</details>

</details>

---

## postgres_conversation_labels {#postgres-conversation-labels}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_labels`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,503

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 41,669.0 to 73,521,321.0
- **Average:** 40,218,843.0449
- **Distinct Values:** 9,995

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,983

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### label_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 7.0 to 201,372.0
- **Average:** 91,082.4561
- **Distinct Values:** 4,001

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,983

</details>

</details>

---

## postgres_conversation_labels_raw {#postgres-conversation-labels-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_labels_raw`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,287

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,454,268.0 to 133,947,240.0
- **Average:** 132,681,689.8166
- **Distinct Values:** 9,820

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,881

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### label_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 68.0 to 374,486.0
- **Average:** 204,603.94420000003
- **Distinct Values:** 2,873

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,881

</details>

</details>

---

## postgres_conversation_trackers {#postgres-conversation-trackers}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_trackers`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,285

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 135.0
- **Average:** 113.4611
- **Distinct Values:** 8

### change_performed_via

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.7488 chars
- **Distinct Values:** 2

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,611,272.0 to 101,663,003.0
- **Average:** 99,387,648.97439997
- **Distinct Values:** 6,932

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,107

### current_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 51,659.0
- **Average:** 24,581.208016235414
- **Distinct Values:** 33
- **Null %:** 80.3%

### current_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.2435 chars
- **Distinct Values:** 7

### duration_in_previous_event

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 78,338.0
- **Average:** 1,622.4434
- **Distinct Values:** 1,350

### event_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.1762 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### performer_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 989.0 to 50,258.0
- **Average:** 26,083.299363057326
- **Distinct Values:** 15
- **Null %:** 87.4%

### previous_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 51,270.0
- **Average:** 24,180.654285714285
- **Distinct Values:** 21
- **Null %:** 96.5%

### previous_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.9234 chars
- **Distinct Values:** 7

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,107

</details>

</details>

---

## postgres_csat_survey_responses {#postgres-csat-survey-responses}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_csat_survey_responses`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,700

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,116.0
- **Average:** 7,436.8793
- **Distinct Values:** 59

### agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4587 chars
- **Distinct Values:** 200

### assigned_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 216.0 to 50,746.0
- **Average:** 37,931.17832576249
- **Distinct Values:** 274
- **Null %:** 22.9%

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3,029,371.0 to 84,233,061.0
- **Average:** 77,832,363.01089995
- **Distinct Values:** 9,681

### contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.35 chars
- **Distinct Values:** 8,568

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6369 chars
- **Distinct Values:** 8,296

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10,013,014.0 to 84,937,377.0
- **Average:** 81,259,009.69500001
- **Distinct Values:** 10,000

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,848

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### feedback_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 22.5787 chars
- **Distinct Values:** 4,322

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 33,818.0
- **Average:** 13,194.6676
- **Distinct Values:** 87

### inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.8285 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1757
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 575,103,467.0 to 606,026,765.0
- **Average:** 590,376,098.4548
- **Distinct Values:** 9,999

### rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6101
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6406 chars
- **Distinct Values:** 3

### response_conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,950

</details>

</details>

---

## postgres_csat_survey_responses_raw {#postgres-csat-survey-responses-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_csat_survey_responses_raw`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 24,887.0
- **Average:** 1,649.2214999999999
- **Distinct Values:** 63

### agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.5282 chars
- **Distinct Values:** 203

### assigned_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 46,656.0
- **Average:** 26,439.395028067363
- **Distinct Values:** 207
- **Null %:** 37.6%

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3,029,608.0 to 68,022,360.0
- **Average:** 63,962,974.1846
- **Distinct Values:** 9,422

### contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.3095 chars
- **Distinct Values:** 8,531

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.7166 chars
- **Distinct Values:** 8,353

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 19,397,853.0 to 65,937,270.0
- **Average:** 63,137,946.1795
- **Distinct Values:** 9,984

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,892

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,845

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### feedback_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.4477 chars
- **Distinct Values:** 3,846

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 32,105.0
- **Average:** 4,186.2681
- **Distinct Values:** 80

### inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9501 chars
- **Distinct Values:** 55

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1701
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 426,412,144.0 to 640,816,234.0
- **Average:** 431,546,825.2416
- **Distinct Values:** 10,000

### rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6692
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6527 chars
- **Distinct Values:** 3

### response_conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,915

</details>

</details>

---

## postgres_ctwa_contact_trackings {#postgres-ctwa-contact-trackings}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_ctwa_contact_trackings`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 259.0 to 28,846.0
- **Average:** 22,046.1299
- **Distinct Values:** 18

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 49,786,171.0 to 172,700,220.0
- **Average:** 169,960,041.2342997
- **Distinct Values:** 9,242

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,829

### ctwa_click_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 134.8444 chars
- **Distinct Values:** 9,851

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9953 chars
- **Distinct Values:** 9,222

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,829

</details>

</details>

---

## postgres_ctwa_contact_trackings_raw {#postgres-ctwa-contact-trackings-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_ctwa_contact_trackings_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 259.0 to 28,846.0
- **Average:** 22,046.1299
- **Distinct Values:** 18

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 49,786,171.0 to 172,700,220.0
- **Average:** 169,960,041.2342997
- **Distinct Values:** 9,242

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,829

### ctwa_click_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 134.8444 chars
- **Distinct Values:** 9,851

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9953 chars
- **Distinct Values:** 9,222

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,829

</details>

</details>

---

## postgres_curated_views {#postgres-curated-views}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_curated_views`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 13

### filters

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 45.07692307692308 chars
- **Distinct Values:** 13

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 25.692307692307693 chars
- **Distinct Values:** 13

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 3

</details>

</details>

---

## postgres_curated_views_raw {#postgres-curated-views-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_curated_views_raw`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 13

### filters

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 45.07692307692308 chars
- **Distinct Values:** 13

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 25.692307692307693 chars
- **Distinct Values:** 13

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 3

</details>

</details>

---

## postgres_custom_field_inboxes {#postgres-custom-field-inboxes}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_inboxes`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 150

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 167.0
- **Average:** 85.74594594594595
- **Distinct Values:** 151

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 370

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 35,527.0
- **Average:** 30,835.618918918924
- **Distinct Values:** 159

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

</details>

</details>

---

## postgres_custom_field_inboxes_raw {#postgres-custom-field-inboxes-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_inboxes_raw`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 150

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 167.0
- **Average:** 85.74594594594595
- **Distinct Values:** 151

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 370

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 35,527.0
- **Average:** 30,835.618918918924
- **Distinct Values:** 159

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

</details>

</details>

---

## postgres_custom_field_options {#postgres-custom-field-options}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_options`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 66

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 91

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 4.0 to 163.0
- **Average:** 105.41333333333333
- **Distinct Values:** 60

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 900

### position

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 247.0
- **Average:** 43.923772609819125
- **Distinct Values:** 249
- **Null %:** 16.5%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 80

### value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 26.83888888888889 chars
- **Distinct Values:** 840

</details>

</details>

---

## postgres_custom_field_options_raw {#postgres-custom-field-options-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_options_raw`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 73

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 91

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 4.0 to 163.0
- **Average:** 102.88246628131022
- **Distinct Values:** 60

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 900

### position

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 247.0
- **Average:** 41.2070805043647
- **Distinct Values:** 249
- **Null %:** 51.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 89

### value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 26.577071290944122 chars
- **Distinct Values:** 840

</details>

</details>

---

## postgres_custom_field_values {#postgres-custom-field-values}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_values`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6,714

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 79,422,859.0 to 134,887,666.0
- **Average:** 127,751,391.40230003
- **Distinct Values:** 9,399

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,867

### custom_field_hash

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.0047 chars
- **Distinct Values:** 1,055

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 36.0
- **Average:** 31.255400000000005
- **Distinct Values:** 20

### custom_field_option_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 657.0
- **Average:** 81.19437563747633
- **Distinct Values:** 48
- **Null %:** 31.4%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,868

### value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.334 chars
- **Distinct Values:** 1,168

</details>

</details>

---

## postgres_custom_field_values_raw {#postgres-custom-field-values-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_values_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,005

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 79,422,859.0 to 119,701,527.0
- **Average:** 117,050,652.7498
- **Distinct Values:** 8,849

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,180

### custom_field_hash

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### custom_field_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 50.0
- **Average:** 40.062799999999996
- **Distinct Values:** 26

### custom_field_option_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 83.0
- **Average:** 53.257839721254356
- **Distinct Values:** 36
- **Null %:** 68.4%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,297

### value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.198 chars
- **Distinct Values:** 5,086

</details>

</details>

---

## postgres_custom_fields {#postgres-custom-fields}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_fields`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 22

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 54.0 to 28,397.0
- **Average:** 23,952.166666666668
- **Distinct Values:** 12

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 30

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 5.766666666666667 chars
- **Distinct Values:** 9

### enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7333333333333333
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 30

### field_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 7.0
- **Average:** 2.3
- **Distinct Values:** 5

### mandatory

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.6 chars
- **Distinct Values:** 28

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 28

</details>

</details>

---

## postgres_custom_fields_raw {#postgres-custom-fields-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_fields_raw`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 22

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 54.0 to 28,397.0
- **Average:** 23,952.166666666668
- **Distinct Values:** 12

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 30

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 5.766666666666667 chars
- **Distinct Values:** 9

### enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7333333333333333
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 30

### field_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 7.0
- **Average:** 2.3
- **Distinct Values:** 5

### mandatory

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.6 chars
- **Distinct Values:** 28

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 28

</details>

</details>

---

## postgres_custom_views {#postgres-custom-views}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_views`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 143

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 240

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 241

### filters

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 75.79253112033194 chars
- **Distinct Values:** 125

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.506224066390041 chars
- **Distinct Values:** 193

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 240

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,378.0
- **Average:** 47,794.041493775934
- **Distinct Values:** 86

</details>

</details>

---

## postgres_custom_views_raw {#postgres-custom-views-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_views_raw`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 147

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 240

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 241

### filters

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 76.052 chars
- **Distinct Values:** 131

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.336 chars
- **Distinct Values:** 194

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 249

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,378.0
- **Average:** 46,706.024
- **Distinct Values:** 86

</details>

</details>

---

## postgres_data_access_logs {#postgres-data-access-logs}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_data_access_logs`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,520

### accessed_data

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.245019920318725 chars
- **Distinct Values:** 3,077

### accessed_detail

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 3.6251358203549437
- **Distinct Values:** 4

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 56.0 to 28,155.0
- **Average:** 26,801.998551249548
- **Distinct Values:** 10

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,522

### ip_address

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.032959072799711 chars
- **Distinct Values:** 136

### resource_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 30,475,464.0 to 119,766,189.0
- **Average:** 109,886,964.65005437
- **Distinct Values:** 2,862
- **Null %:** 0.1%

### resource_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.994929373415429 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,150.0
- **Average:** 50,440.79626946758
- **Distinct Values:** 11

</details>

</details>

---

## postgres_data_access_logs_raw {#postgres-data-access-logs-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_data_access_logs_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,520

### accessed_data

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.245019920318725 chars
- **Distinct Values:** 3,077

### accessed_detail

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 3.6251358203549437
- **Distinct Values:** 4

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 56.0 to 28,155.0
- **Average:** 26,801.998551249548
- **Distinct Values:** 10

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 5,522

### ip_address

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.032959072799711 chars
- **Distinct Values:** 136

### resource_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 30,475,464.0 to 119,766,189.0
- **Average:** 109,886,964.65005437
- **Distinct Values:** 2,862
- **Null %:** 0.1%

### resource_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.994929373415429 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 53,150.0
- **Average:** 50,440.79626946758
- **Distinct Values:** 11

</details>

</details>

---

## postgres_fb_account_account {#postgres-fb-account-account}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_account`

<details>
<summary><strong>📊 Columns (22 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 38

### company

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 13.973387922210849 chars
- **Distinct Values:** 2,714

### company_logo

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 0.01160013647219379 chars
- **Distinct Values:** 3

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,849

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2,931

### google_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.057659501876492665 chars
- **Distinct Values:** 21

### grace_added_on

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 149
- **Null %:** 95.0%

### grace_extension

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.01501194131695667
- **Distinct Values:** 2

### hd_account_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 28,777.0
- **Average:** 20,084.551916376306
- **Distinct Values:** 2,870
- **Null %:** 2.1%

### is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6618901398839986
- **Distinct Values:** 2

### is_enterprise

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.016376663254861822
- **Distinct Values:** 2

### link_click_attribution_window

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 240.0
- **Average:** 24.720914363698398
- **Distinct Values:** 8

### messages_sent_window

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 168.0
- **Average:** 24.454793585806893
- **Distinct Values:** 7

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.365404298874104 chars
- **Distinct Values:** 2,747

### on_grace_period

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.05834186284544524
- **Distinct Values:** 2

### payment_pending

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03002388263391334
- **Distinct Values:** 2

### show_link_click_attribution

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### show_messages_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.007505970658478335
- **Distinct Values:** 2

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.2975093824633231 chars
- **Distinct Values:** 4

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### ui_mode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.9669054930058 chars
- **Distinct Values:** 3

</details>

</details>

---

## postgres_fb_account_account_raw {#postgres-fb-account-account-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_account_raw`

<details>
<summary><strong>📊 Columns (22 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 38

### company

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 13.973387922210849 chars
- **Distinct Values:** 2,714

### company_logo

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 0.01160013647219379 chars
- **Distinct Values:** 3

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,849

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2,931

### google_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.057659501876492665 chars
- **Distinct Values:** 21

### grace_added_on

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 149
- **Null %:** 95.0%

### grace_extension

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.01501194131695667
- **Distinct Values:** 2

### hd_account_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 28,777.0
- **Average:** 20,084.551916376306
- **Distinct Values:** 2,870
- **Null %:** 2.1%

### is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6618901398839986
- **Distinct Values:** 2

### is_enterprise

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.016376663254861822
- **Distinct Values:** 2

### link_click_attribution_window

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 240.0
- **Average:** 24.720914363698398
- **Distinct Values:** 8

### messages_sent_window

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 168.0
- **Average:** 24.454793585806893
- **Distinct Values:** 7

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.365404298874104 chars
- **Distinct Values:** 2,747

### on_grace_period

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.05834186284544524
- **Distinct Values:** 2

### payment_pending

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03002388263391334
- **Distinct Values:** 2

### show_link_click_attribution

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### show_messages_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.007505970658478335
- **Distinct Values:** 2

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.2975093824633231 chars
- **Distinct Values:** 4

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### ui_mode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.9669054930058 chars
- **Distinct Values:** 3

</details>

</details>

---

## postgres_fb_account_integration {#postgres-fb-account-integration}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_integration`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 10,964.0
- **Average:** 7,782.246895544193
- **Distinct Values:** 1,925

### config

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 105.18517165814463 chars
- **Distinct Values:** 2,419

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,246

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2,738

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 10.739956172388604 chars
- **Distinct Values:** 23

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### uid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.014974433893352 chars
- **Distinct Values:** 2,368

</details>

</details>

---

## postgres_fb_block_activities {#postgres-fb-block-activities}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_block_activities`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 21

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,237

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7.0
- **Average:** 2.6782
- **Distinct Values:** 6

### block_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.0552 chars
- **Distinct Values:** 506

### block_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 4.0
- **Average:** 1.5175
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,237

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### flow_execution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 9,817,587.0 to 15,269,884.0
- **Average:** 15,097,574.245199993
- **Distinct Values:** 4,006

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,476.0 to 13,933.0
- **Average:** 10,967.9656
- **Distinct Values:** 135

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,236

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 487,988.0 to 57,023,752.0
- **Average:** 52,369,927.45149999
- **Distinct Values:** 3,375

</details>

</details>

---

## postgres_fb_block_activities_dup {#postgres-fb-block-activities-dup}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_block_activities_dup`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 20

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,221

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.9377
- **Distinct Values:** 2

### block_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 73

### block_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.3442
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,221

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### flow_execution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,377.0 to 45,620.0
- **Average:** 13,839.3198
- **Distinct Values:** 7,603

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 529.0
- **Average:** 484.0787567893784
- **Distinct Values:** 13
- **Null %:** 0.6%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,220

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2,803,649.0 to 10,481,104.0
- **Average:** 7,516,723.535099998
- **Distinct Values:** 5,928

</details>

</details>

---

## postgres_fb_bot_builder_botcsat {#postgres-fb-bot-builder-botcsat}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_botcsat`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 11,555.0 to 11,555.0
- **Average:** 11,555.0
- **Distinct Values:** 1

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 37,338.0 to 37,380.0
- **Average:** 37,354.12903225807
- **Distinct Values:** 30

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.9032258064516129 chars
- **Distinct Values:** 4

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 3.0 to 5.0
- **Average:** 4.857142857142857
- **Distinct Values:** 3
- **Null %:** 54.8%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 31

### flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 388.0 to 435.0
- **Average:** 394.06451612903226
- **Distinct Values:** 2

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12,239.0 to 36,303.0
- **Average:** 32,421.709677419356
- **Distinct Values:** 2

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.6129032258064516
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,376,195,950.0 to 1,391,460,105.0
- **Average:** 1,378,215,128.516129
- **Distinct Values:** 30

### node_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 177,540.0 to 195,339.0
- **Average:** 179,891.2258064516
- **Distinct Values:** 6

### sender_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 146,138,923.0 to 147,158,342.0
- **Average:** 146,273,354.83870968
- **Distinct Values:** 30

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

</details>

</details>

---

## postgres_fb_bot_builder_botcsat_raw {#postgres-fb-bot-builder-botcsat-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_botcsat_raw`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 11,555.0 to 11,555.0
- **Average:** 11,555.0
- **Distinct Values:** 1

### conv_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 37,338.0 to 37,380.0
- **Average:** 37,354.12903225807
- **Distinct Values:** 30

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.9032258064516129 chars
- **Distinct Values:** 4

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 3.0 to 5.0
- **Average:** 4.857142857142857
- **Distinct Values:** 3
- **Null %:** 54.8%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 31

### flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 388.0 to 435.0
- **Average:** 394.06451612903226
- **Distinct Values:** 2

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12,239.0 to 36,303.0
- **Average:** 32,421.709677419356
- **Distinct Values:** 2

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.6129032258064516
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1,376,195,950.0 to 1,391,460,105.0
- **Average:** 1,378,215,128.516129
- **Distinct Values:** 30

### node_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 177,540.0 to 195,339.0
- **Average:** 179,891.2258064516
- **Distinct Values:** 6

### sender_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 146,138,923.0 to 147,158,342.0
- **Average:** 146,273,354.83870968
- **Distinct Values:** 30

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

</details>

</details>

---

## postgres_fb_bot_builder_flow {#postgres-fb-bot-builder-flow}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_flow`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,008.0
- **Average:** 7,683.3615107913665
- **Distinct Values:** 34

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 545

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 556

### has_changes

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.45863309352517984
- **Distinct Values:** 2

### is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.420863309352518
- **Distinct Values:** 2

### is_published

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5557553956834532
- **Distinct Values:** 2

### production_flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 48,167.0 to 62,302.0
- **Average:** 53,890.56654676259
- **Distinct Values:** 548

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### staging_flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 48,168.0 to 62,222.0
- **Average:** 53,348.15647482014
- **Distinct Values:** 556

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 552

</details>

</details>

---

## postgres_fb_bot_builder_flow_raw {#postgres-fb-bot-builder-flow-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_flow_raw`

<details>
<summary><strong>📊 Columns (12 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,008.0
- **Average:** 7,683.3615107913665
- **Distinct Values:** 34

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 545

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 556

### has_changes

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.45863309352517984
- **Distinct Values:** 2

### is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.420863309352518
- **Distinct Values:** 2

### is_published

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5557553956834532
- **Distinct Values:** 2

### production_flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 48,167.0 to 62,302.0
- **Average:** 53,890.56654676259
- **Distinct Values:** 548

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### staging_flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 48,168.0 to 62,222.0
- **Average:** 53,348.15647482014
- **Distinct Values:** 556

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 552

</details>

</details>

---

## postgres_fb_builder_user {#postgres-fb-builder-user}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_builder_user`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 636

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,954

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,996

### identity

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.9948 chars
- **Distinct Values:** 9,880

### ig_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0143 chars
- **Distinct Values:** 12

### ig_username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.1542 chars
- **Distinct Values:** 1,601

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 764.0 to 927.0
- **Average:** 910.6
- **Distinct Values:** 4
- **Null %:** 99.8%

### phone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.006 chars
- **Distinct Values:** 6

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.4302 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,498

### wa_optin_status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_fb_builder_user_raw {#postgres-fb-builder-user-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_builder_user_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 635

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,954

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,996

### identity

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.9948 chars
- **Distinct Values:** 9,880

### ig_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0143 chars
- **Distinct Values:** 12

### ig_username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.1542 chars
- **Distinct Values:** 1,601

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 764.0 to 927.0
- **Average:** 910.6
- **Distinct Values:** 4
- **Null %:** 99.8%

### phone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.006 chars
- **Distinct Values:** 6

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.4302 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,498

### wa_optin_status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_fb_central_orders {#postgres-fb-central-orders}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_central_orders`

<details>
<summary><strong>📊 Columns (35 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 13.0 to 747.0
- **Average:** 56.4406
- **Distinct Values:** 54

### amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 203,190.0
- **Average:** 977.2809080000005
- **Distinct Values:** 1,987

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0037
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,586

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 1

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.4412 chars
- **Distinct Values:** 7,751

### discount_amount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** Yes
- **Range:** 0.0 to 8,398.4
- **Average:** 8.08854
- **Distinct Values:** 99

### discount_codes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 36.1764 chars
- **Distinct Values:** 1,796

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.8052 chars
- **Distinct Values:** 7,381

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.5339 chars
- **Distinct Values:** 5,260

### fulfillment

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 23.5194 chars
- **Distinct Values:** 625

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.5227 chars
- **Distinct Values:** 4

### gateway

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.5369 chars
- **Distinct Values:** 29

### integration_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 21.0 to 4,971.0
- **Average:** 976.3246951219512
- **Distinct Values:** 24
- **Null %:** 93.4%

### items

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 605.1322 chars
- **Distinct Values:** 9,999

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.7719 chars
- **Distinct Values:** 4,579

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 10,000

### order_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.83 chars
- **Distinct Values:** 9,999

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.5642 chars
- **Distinct Values:** 305

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 124.7358 chars
- **Distinct Values:** 10,000

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.2992 chars
- **Distinct Values:** 7

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.4698 chars
- **Distinct Values:** 9,351

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 1

### shipping_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 800.0
- **Average:** 9.742
- **Distinct Values:** 26

### source_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0016 chars
- **Distinct Values:** 3

### store_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 203,190.0
- **Average:** 967.7015040000002
- **Distinct Values:** 1,884

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 19.2745 chars
- **Distinct Values:** 527

### tracking_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 119.7761 chars
- **Distinct Values:** 9,942

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,586

</details>

</details>

---

## postgres_fb_conv_flow_messages {#postgres-fb-conv-flow-messages}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_messages`

<details>
<summary><strong>📊 Columns (17 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 74

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3.0 to 10,842.0
- **Average:** 7,535.8744
- **Distinct Values:** 61

### conv_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 992.0 to 13,839.0
- **Average:** 10,496.365000000005
- **Distinct Values:** 169

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,674

### entity_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,123.0 to 4,143.0
- **Average:** 3,796.1117021276596
- **Distinct Values:** 11
- **Null %:** 94.4%

### entity_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.282 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### execution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,299,997.0 to 14,889,164.0
- **Average:** 14,814,117.763777025
- **Distinct Values:** 8,506
- **Null %:** 5.6%

### message_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6.0
- **Average:** 4.8362
- **Distinct Values:** 5

### meta

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 77.2582 chars
- **Distinct Values:** 9,004

### node_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,322.0 to 26,783.0
- **Average:** 18,901.6239
- **Distinct Values:** 347

### ref_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.8916 chars
- **Distinct Values:** 8,997

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 1.8923
- **Distinct Values:** 3

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,682

### user_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 489,017.0 to 56,528,714.0
- **Average:** 52,113,776.31980001
- **Distinct Values:** 7,945

</details>

</details>

---

## postgres_fb_conv_flow_nodes {#postgres-fb-conv-flow-nodes}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_nodes`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 112

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,500

### data

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 418.2512 chars
- **Distinct Values:** 6,706

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 67.0 to 55,043.0
- **Average:** 35,292.968400000005
- **Distinct Values:** 5,978

### node_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.1967 chars
- **Distinct Values:** 88

### oid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 9,982

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.71 chars
- **Distinct Values:** 19

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

</details>

</details>

---

## postgres_fb_conv_flow_nodes_raw {#postgres-fb-conv-flow-nodes-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_nodes_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,273

### data

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 426.9296 chars
- **Distinct Values:** 7,297

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### flow_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 67.0 to 52,877.0
- **Average:** 30,991.5558
- **Distinct Values:** 6,707

### node_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.1528 chars
- **Distinct Values:** 71

### oid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 9,973

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.8237 chars
- **Distinct Values:** 19

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,045

</details>

</details>

---

## postgres_fb_conversational_broadcasts {#postgres-fb-conversational-broadcasts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_broadcasts`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,001

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2,133.0
- **Average:** 638.1781
- **Distinct Values:** 41

### cohort_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0168 chars
- **Distinct Values:** 4

### cohort_ids

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.5384 chars
- **Distinct Values:** 129

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,761

### draft_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 8.0 to 40,350.0
- **Average:** 18,775.611840641
- **Distinct Values:** 8,985
- **Null %:** 10.1%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### is_triggered

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8127
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 19.8266 chars
- **Distinct Values:** 8,479

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.3479 chars
- **Distinct Values:** 4

### retries_attempted

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.0209
- **Distinct Values:** 4

### retry_settings

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.1668 chars
- **Distinct Values:** 3,506

### schedule_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 8,175
- **Null %:** 18.0%

### schedule_time_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,826

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2944 chars
- **Distinct Values:** 7

### topic_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 3,499.0
- **Average:** 1,201.967741935484
- **Distinct Values:** 17
- **Null %:** 99.7%

### total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 199,920.0
- **Average:** 7,818.170900000003
- **Distinct Values:** 4,071

### trigger_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 4.0 to 50,484.0
- **Average:** 27,257.68994574627
- **Distinct Values:** 8,540
- **Null %:** 13.4%

### ums_broadcast_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.3512 chars
- **Distinct Values:** 8,064

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,567

### users_csv_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 123.5242 chars
- **Distinct Values:** 8,380

</details>

</details>

---

## postgres_fb_conversational_broadcasts_raw {#postgres-fb-conversational-broadcasts-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_broadcasts_raw`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 5,960.0
- **Average:** 1,530.867
- **Distinct Values:** 68

### cohort_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.5328 chars
- **Distinct Values:** 150

### cohort_ids

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.2338 chars
- **Distinct Values:** 214

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,786

### draft_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 8.0 to 23,481.0
- **Average:** 10,555.32745504841
- **Distinct Values:** 8,677
- **Null %:** 13.2%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### is_triggered

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8211
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 18.9918 chars
- **Distinct Values:** 8,436

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.4149 chars
- **Distinct Values:** 4

### retries_attempted

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.0223
- **Distinct Values:** 4

### retry_settings

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.8804 chars
- **Distinct Values:** 2,189

### schedule_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 8,236
- **Null %:** 17.3%

### schedule_time_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,872

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.3238 chars
- **Distinct Values:** 7

### topic_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 3,499.0
- **Average:** 1,320.2285714285715
- **Distinct Values:** 21
- **Null %:** 99.7%

### total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 171,562.0
- **Average:** 7,344.133799999997
- **Distinct Values:** 3,807

### trigger_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 4.0 to 33,701.0
- **Average:** 19,787.257548032936
- **Distinct Values:** 8,624
- **Null %:** 12.6%

### ums_broadcast_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.5432 chars
- **Distinct Values:** 8,143

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,404

### users_csv_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 111.9164 chars
- **Distinct Values:** 8,510

</details>

</details>

---

## postgres_fb_conversational_flow_executions {#postgres-fb-conversational-flow-executions}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flow_executions`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,437

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### execution_source_ref_id

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 4.0879 chars
- **Distinct Values:** 3,605

### execution_source_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 13.9012 chars
- **Distinct Values:** 2

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 529.0
- **Average:** 473.2887033497636
- **Distinct Values:** 21
- **Null %:** 0.6%

### last_executed_node_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.9964 chars
- **Distinct Values:** 69

### next_node_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2919 chars
- **Distinct Values:** 25

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tracker_metadata

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,583

### user_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,803,649.0 to 10,477,426.0
- **Average:** 7,197,557.564912978
- **Distinct Values:** 7,674
- **Null %:** 0.0%

</details>

</details>

---

## postgres_fb_conversational_flow_executions_raw {#postgres-fb-conversational-flow-executions-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flow_executions_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,437

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### execution_source_ref_id

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 4.0879 chars
- **Distinct Values:** 3,605

### execution_source_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 13.9012 chars
- **Distinct Values:** 2

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 529.0
- **Average:** 473.2887033497636
- **Distinct Values:** 21
- **Null %:** 0.6%

### last_executed_node_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.9964 chars
- **Distinct Values:** 69

### next_node_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2919 chars
- **Distinct Values:** 25

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tracker_metadata

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,583

### user_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,803,649.0 to 10,477,426.0
- **Average:** 7,197,557.564912978
- **Distinct Values:** 7,674
- **Null %:** 0.0%

</details>

</details>

---

## postgres_fb_conversational_flows {#postgres-fb-conversational-flows}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows`

<details>
<summary><strong>📊 Columns (25 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,253

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 10,900.0
- **Average:** 4,872.199029799028
- **Distinct Values:** 184

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,029

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 12
- **Null %:** 99.8%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### dnd_duration

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.00997920997920998 chars
- **Distinct Values:** 6

### dnd_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0009702009702009702
- **Distinct Values:** 2

### dnd_start_time

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.018711018711018712 chars
- **Distinct Values:** 5

### draft_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3,409.0
- **Average:** 1,634.521020311762
- **Distinct Values:** 1,293
- **Null %:** 70.7%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 7,088

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 52.0 to 5,578.0
- **Average:** 4,323.0582483587095
- **Distinct Values:** 250
- **Null %:** 0.8%

### is_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0015246015246015245
- **Distinct Values:** 2

### is_draft

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.09133749133749133
- **Distinct Values:** 2

### is_two_way_broadcast

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.15384615384615385
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 19.666528066528066 chars
- **Distinct Values:** 5,789

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.157726957726958 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### test_mode

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.023007623007623008
- **Distinct Values:** 2

### test_mode_numbers

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 3.6334026334026333 chars
- **Distinct Values:** 171

### trigger_event_type_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,156.0 to 2,192.0
- **Average:** 1,338.132726089786
- **Distinct Values:** 97
- **Null %:** 78.7%

### triggers

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 146.34428274428274 chars
- **Distinct Values:** 6,986

### type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.091614691614692 chars
- **Distinct Values:** 5

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,120

### use_cases

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres_fb_conversational_flows_freetextreplies {#postgres-fb-conversational-flows-freetextreplies}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows_freetextreplies`

<details>
<summary><strong>📊 Columns (7 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,717

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 6,728

### execution_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 129,924,842.0 to 194,173,711.0
- **Average:** 168,690,422.4910064
- **Distinct Values:** 6,477

### node_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 49,939.0 to 120,386.0
- **Average:** 80,721.43288241416
- **Distinct Values:** 62

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.67087854913037 chars
- **Distinct Values:** 6,056

</details>

</details>

---

## postgres_fb_conversational_flows_freetextreplies_raw {#postgres-fb-conversational-flows-freetextreplies-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows_freetextreplies_raw`

<details>
<summary><strong>📊 Columns (7 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,717

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 6,728

### execution_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 129,924,842.0 to 194,173,711.0
- **Average:** 168,690,422.49100634
- **Distinct Values:** 6,477

### node_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 49,939.0 to 120,386.0
- **Average:** 80,721.43288241416
- **Distinct Values:** 62

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### text

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.67087854913037 chars
- **Distinct Values:** 6,056

</details>

</details>

---

## postgres_fb_igrn_broadcasts {#postgres-fb-igrn-broadcasts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_broadcasts`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 606.6849865951742 chars
- **Distinct Values:** 720

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 744
- **Null %:** 0.4%

### custom_ref_prefix

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 746

### is_triggered

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9477211796246648
- **Distinct Values:** 2

### max_users_to_receive

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 68,550.0
- **Average:** 9,998.743243243243
- **Distinct Values:** 374
- **Null %:** 10.7%

### ref

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.08847184986595 chars
- **Distinct Values:** 727

### schedule_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 746

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### topic_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 4,147.0
- **Average:** 1,920.9490616621983
- **Distinct Values:** 89

### total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 68,550.0
- **Average:** 8,381.739946380698
- **Distinct Values:** 404

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 740

</details>

</details>

---

## postgres_fb_igrn_broadcasts_raw {#postgres-fb-igrn-broadcasts-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_broadcasts_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 605.8728246318608 chars
- **Distinct Values:** 720

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 744
- **Null %:** 0.5%

### custom_ref_prefix

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 746

### is_triggered

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9464524765729585
- **Distinct Values:** 2

### max_users_to_receive

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 68,550.0
- **Average:** 10,086.490254872564
- **Distinct Values:** 374
- **Null %:** 10.7%

### ref

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.089692101740294 chars
- **Distinct Values:** 727

### schedule_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 746

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### topic_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 4,147.0
- **Average:** 1,918.6439089692099
- **Distinct Values:** 89

### total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 68,550.0
- **Average:** 8,370.519410977242
- **Distinct Values:** 404

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 741

</details>

</details>

---

## postgres_fb_igrn_optins {#postgres-fb-igrn-optins}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_optins`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,788

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 36.0 to 8,496.0
- **Average:** 4,630.1697
- **Distinct Values:** 21

### conv_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 13,827.0
- **Average:** 7,433.08463008463
- **Distinct Values:** 28
- **Null %:** 26.7%

### conv_flow_message_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,111.0 to 3,941,160.0
- **Average:** 2,650,566.1553200157
- **Distinct Values:** 7,360
- **Null %:** 26.4%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,982

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### notification_messages_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.8832 chars
- **Distinct Values:** 9,998

### notification_sent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 13,119,498.0 to 70,296,551.0
- **Average:** 63,440,548.21895911
- **Distinct Values:** 2,691
- **Null %:** 73.1%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 2

### status_changed_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,982

### topic_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 199.0 to 4,147.0
- **Average:** 2,786.5388
- **Distinct Values:** 29

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,982

### user_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,895,060.0 to 57,931,360.0
- **Average:** 48,069,458.95950001
- **Distinct Values:** 9,991

</details>

</details>

---

## postgres_hd_csat_survey_responses {#postgres-hd-csat-survey-responses}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_csat_survey_responses`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 28

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 22,742.0
- **Average:** 1,569.9344
- **Distinct Values:** 60

### agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4918 chars
- **Distinct Values:** 200

### assigned_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 46,126.0
- **Average:** 25,796.42780835222
- **Distinct Values:** 201
- **Null %:** 38.2%

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3,029,608.0 to 66,555,112.0
- **Average:** 63,966,601.7949
- **Distinct Values:** 9,430

### contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4112 chars
- **Distinct Values:** 8,604

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6815 chars
- **Distinct Values:** 8,328

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 62,554,920.0 to 63,639,156.0
- **Average:** 63,078,821.1584
- **Distinct Values:** 9,984

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,889

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 9,893

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### feedback_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.4746 chars
- **Distinct Values:** 3,834

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 30,159.0
- **Average:** 4,107.601
- **Distinct Values:** 78

### inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9045 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1758
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 426,394,302.0 to 434,909,475.0
- **Average:** 430,813,082.4345
- **Distinct Values:** 10,000

### rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6771
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6581 chars
- **Distinct Values:** 3

### response_conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,291

</details>

</details>

---

## postgres_hd_csat_survey_responses_raw {#postgres-hd-csat-survey-responses-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_csat_survey_responses_raw`

<details>
<summary><strong>📊 Columns (23 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 28

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 22,742.0
- **Average:** 1,569.9344
- **Distinct Values:** 60

### agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4918 chars
- **Distinct Values:** 200

### assigned_agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 46,126.0
- **Average:** 25,796.42780835222
- **Distinct Values:** 201
- **Null %:** 38.2%

### contact_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3,029,608.0 to 66,555,112.0
- **Average:** 63,966,601.7949
- **Distinct Values:** 9,430

### contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4112 chars
- **Distinct Values:** 8,604

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6815 chars
- **Distinct Values:** 8,328

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 62,554,920.0 to 63,639,156.0
- **Average:** 63,078,821.1584
- **Distinct Values:** 9,984

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,889

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 9,893

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### feedback_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.4746 chars
- **Distinct Values:** 3,834

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 115.0 to 30,159.0
- **Average:** 4,107.601
- **Distinct Values:** 78

### inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9045 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1758
- **Distinct Values:** 2

### message_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 426,394,302.0 to 434,909,475.0
- **Average:** 430,813,082.4345
- **Distinct Values:** 10,000

### rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6771
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6581 chars
- **Distinct Values:** 3

### response_conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,291

</details>

</details>

---

## postgres_hd_messages {#postgres-hd-messages}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_messages`

<details>
<summary><strong>📊 Columns (30 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,460

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 51.0 to 27,452.0
- **Average:** 11,399.7912
- **Distinct Values:** 58

### broadcast_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 4,773,979.0 to 4,775,281.0
- **Average:** 4,774,990.367561875
- **Distinct Values:** 62
- **Null %:** 62.0%

### client_echo_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 437.8122 chars
- **Distinct Values:** 4,628

### content_attributes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 496.4759 chars
- **Distinct Values:** 9,407

### content_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5.0
- **Average:** 0.012033572656487006
- **Distinct Values:** 4
- **Null %:** 1.1%

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 62,626,201.0 to 96,407,062.0
- **Average:** 89,880,775.86720002
- **Distinct Values:** 5,717

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,716

### echo_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 4.0
- **Average:** 3.9920844327176783
- **Distinct Values:** 3
- **Null %:** 96.2%

### email_draft

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### external_source_ids

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 18.0776 chars
- **Distinct Values:** 1,756

### identifier

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.033 chars
- **Distinct Values:** 10

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 695.0 to 34,116.0
- **Average:** 30,702.3972
- **Distinct Values:** 67

### is_echo

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0379
- **Distinct Values:** 2

### message_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 11.0
- **Average:** 3.7189
- **Distinct Values:** 6

### parent_message_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### private

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### sender_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 92,103,150.0
- **Average:** 412,739.54302581545
- **Distinct Values:** 114
- **Null %:** 0.1%

### sender_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0289 chars
- **Distinct Values:** 4

### source_id

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 4.5468 chars
- **Distinct Values:** 653

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2.0
- **Average:** 1.9711
- **Distinct Values:** 3

### template_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 98.4129 chars
- **Distinct Values:** 4,537

### template_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 21,706.0 to 114,674.0
- **Average:** 110,457.8180982535
- **Distinct Values:** 279
- **Null %:** 2.1%

### ums_message_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.4267 chars
- **Distinct Values:** 9,726

### ums_message_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 7.476 chars
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,104

</details>

</details>

---

## postgres_in_app_feedbacks {#postgres-in-app-feedbacks}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_in_app_feedbacks`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,489

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### feature_likability

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6523
- **Distinct Values:** 2

### feature_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### source_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10,863,224.0 to 103,662,327.0
- **Average:** 89,567,788.80470002
- **Distinct Values:** 4,930

### source_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,489

</details>

</details>

---

## postgres_inbox_members {#postgres-inbox-members}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_inbox_members`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,512

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,818

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 5.0 to 33,936.0
- **Average:** 10,361.078699999998
- **Distinct Values:** 1,328

### inbox_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.08588521598053134
- **Distinct Values:** 3
- **Null %:** 1.4%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,817

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 50,815.0
- **Average:** 32,722.1544
- **Distinct Values:** 1,743

</details>

</details>

---

## postgres_inboxes {#postgres-inboxes}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_inboxes`

<details>
<summary><strong>📊 Columns (50 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 455

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,296.0
- **Average:** 11,350.678076609618
- **Distinct Values:** 711

### allow_offline_assignment

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1813
- **Distinct Values:** 2

### auto_alert_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 9,360.0
- **Average:** 718.516707416463
- **Distinct Values:** 36

### auto_close_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 43,200.0
- **Average:** 828.8956805215973
- **Distinct Values:** 56

### auto_resolve_bot_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 10,800.0
- **Average:** 780.5218690573214
- **Distinct Values:** 43

### auto_resolve_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 525,600.0
- **Average:** 2,862.946481934257
- **Distinct Values:** 48

### auto_resolve_voice_duration

- **Type:** `Float`
- **Nullable:** Yes

### away_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.3697364846509101 chars
- **Distinct Values:** 5

### bot_handoff_away

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.997826677533279
- **Distinct Values:** 2

### channel_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 11,528.0
- **Average:** 4,160.423526215703
- **Distinct Values:** 2,520

### channel_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 20.662048356424883 chars
- **Distinct Values:** 17

### conversation_tracking_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,929

### csat_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 106.31676174952459 chars
- **Distinct Values:** 53

### csat_question

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 34.028796522684054 chars
- **Distinct Values:** 5

### csat_survey_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.10730779679434936
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 963
- **Null %:** 73.6%

### email_collect_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0005433306166802499
- **Distinct Values:** 2

### enable_agent_offline

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.004618310241782124
- **Distinct Values:** 2

### enable_auto_assignment

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 1.0844879108937788
- **Distinct Values:** 3

### end_time

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0488997555012225 chars
- **Distinct Values:** 12

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 3,090

### greeting_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.024178212442271124
- **Distinct Values:** 2

### greeting_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.252377071447976 chars
- **Distinct Values:** 16

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.373811464276013 chars
- **Distinct Values:** 2,728

### opt_in_key

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.233903830480847 chars
- **Distinct Values:** 11

### opt_in_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.7851 chars
- **Distinct Values:** 5

### opt_out_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1752241238793806
- **Distinct Values:** 2

### opt_out_key

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.236348818255909 chars
- **Distinct Values:** 18

### opt_out_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 42.5281173594132 chars
- **Distinct Values:** 28

### out_of_office_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 45.09372453137734 chars
- **Distinct Values:** 349

### send_csat_for_auto_resolved_conversation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.17370721048798252
- **Distinct Values:** 2

### send_csat_for_ooo

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.17370721048798252
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### start_time

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0467264330345015 chars
- **Distinct Values:** 10

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.0035316490084216
- **Distinct Values:** 2

### timezone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.255637055148058 chars
- **Distinct Values:** 13

### tracking_reminder_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### ums_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.05517115804806992
- **Distinct Values:** 2

### ums_incoming_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.06030969845150774
- **Distinct Values:** 2

### ums_outgoing_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.004618310241782124
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,413

### wa_csat_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.00873998543335761
- **Distinct Values:** 2

### wa_widget_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.871267297887837 chars
- **Distinct Values:** 193

### wait_time_enabled

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.04699809834284162
- **Distinct Values:** 2

### wait_time_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 88.09915783754414 chars
- **Distinct Values:** 67

### widget_bot_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0331431676174954 chars
- **Distinct Values:** 26

### working_hours_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.24123879380603097
- **Distinct Values:** 2

</details>

</details>

---

## postgres_labels {#postgres-labels}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_labels`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,234

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,287.0
- **Average:** 10,494.8853
- **Distinct Values:** 303

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### color

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,582

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.1348 chars
- **Distinct Values:** 41

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### internal

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### label_level

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.0811
- **Distinct Values:** 3

### label_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 2

### resource_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### show_on_sidebar

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 17.5563 chars
- **Distinct Values:** 8,842

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,568

</details>

</details>

---

## postgres_labels_raw {#postgres-labels-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_labels_raw`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 476.0
- **Average:** 138.6545
- **Distinct Values:** 124

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### color

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,969

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 1.3446 chars
- **Distinct Values:** 215

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### internal

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.001
- **Distinct Values:** 2

### label_level

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.0157
- **Distinct Values:** 3

### label_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 2

### resource_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### show_on_sidebar

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 21.6029 chars
- **Distinct Values:** 1,283

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,109

</details>

</details>

---

## postgres_lc_contacts_contacts {#postgres-lc-contacts-contacts}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lc_contacts_contacts`

<details>
<summary><strong>📊 Columns (18 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 710

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 225.0
- **Average:** 116.4091
- **Distinct Values:** 25

### additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 13.499 chars
- **Distinct Values:** 2,312

### address

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0243 chars
- **Distinct Values:** 2

### conversations_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 219.0
- **Average:** 2.849
- **Distinct Values:** 35

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,967

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1.9994 chars
- **Distinct Values:** 2

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.2747 chars
- **Distinct Values:** 8,328

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,913

### identifier

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### instagram_username

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 11.4404 chars
- **Distinct Values:** 9,700

### opt_in

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7718
- **Distinct Values:** 2

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.938 chars
- **Distinct Values:** 9,854

### pubsub_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 9,914

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,611

</details>

</details>

---

## postgres_lk2_shopify_app_event {#postgres-lk2-shopify-app-event}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_event`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 56.0 to 27,909.0
- **Average:** 11,807.592592592593
- **Distinct Values:** 13

### agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 52,230.0
- **Average:** 40,964.4
- **Distinct Values:** 8
- **Null %:** 81.5%

### conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,644.0 to 1,380,088.0
- **Average:** 558,762.8
- **Distinct Values:** 9
- **Null %:** 81.5%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 54

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 1

### order_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,940,734.0 to 28,347,984.0
- **Average:** 24,895,329.111111112
- **Distinct Values:** 36

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

</details>

</details>

---

## postgres_lk2_shopify_app_event_raw {#postgres-lk2-shopify-app-event-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_event_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 56.0 to 27,909.0
- **Average:** 11,807.592592592593
- **Distinct Values:** 13

### agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 52,230.0
- **Average:** 40,964.4
- **Distinct Values:** 8
- **Null %:** 81.5%

### conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,644.0 to 1,380,088.0
- **Average:** 558,762.8
- **Distinct Values:** 9
- **Null %:** 81.5%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 54

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 1

### order_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,940,734.0 to 28,347,984.0
- **Average:** 24,895,329.111111112
- **Distinct Values:** 36

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

</details>

</details>

---

## postgres_lk2_shopify_app_orderrefund {#postgres-lk2-shopify-app-orderrefund}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_orderrefund`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 174

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,566

### is_created_on_shopify

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9974457215836526
- **Distinct Values:** 2

### last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.573435504469984 chars
- **Distinct Values:** 2

### order_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,214,523.0 to 28,348,009.0
- **Average:** 8,821,745.161373947
- **Distinct Values:** 1,538
- **Null %:** 1.5%

### processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 305
- **Null %:** 80.6%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3301404853128993 chars
- **Distinct Values:** 305

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 50.0 to 261,167.0
- **Average:** 841.4521200510856
- **Distinct Values:** 211

</details>

</details>

---

## postgres_lk2_shopify_app_orderrefund_raw {#postgres-lk2-shopify-app-orderrefund-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_orderrefund_raw`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 174

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,566

### is_created_on_shopify

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9974457215836526
- **Distinct Values:** 2

### last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.573435504469984 chars
- **Distinct Values:** 2

### order_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,214,523.0 to 28,348,009.0
- **Average:** 8,821,745.161373947
- **Distinct Values:** 1,538
- **Null %:** 1.5%

### processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 305
- **Null %:** 80.6%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3301404853128993 chars
- **Distinct Values:** 305

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 50.0 to 261,167.0
- **Average:** 841.4521200510854
- **Distinct Values:** 211

</details>

</details>

---

## postgres_lk2_shopify_app_shopifyorder {#postgres-lk2-shopify-app-shopifyorder}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyorder`

<details>
<summary><strong>📊 Columns (54 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 104

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 673.8161759999998
- **Distinct Values:** 1,475

### applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 76,377.0
- **Average:** 44.77312400000003
- **Distinct Values:** 736

### cancel_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6022 chars
- **Distinct Values:** 3

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,211,275.0 to 186,789,533.0
- **Average:** 79,351,993.2806
- **Distinct Values:** 10,000

### conversation_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### create_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,991

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4882 chars
- **Distinct Values:** 2

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9989 chars
- **Distinct Values:** 7,918

### edit_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.457 chars
- **Distinct Values:** 7,627

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.4831 chars
- **Distinct Values:** 3,929

### fixed_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 572.2139000000001
- **Distinct Values:** 1,360

### is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4344
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.677 chars
- **Distinct Values:** 3,576

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.9985 chars
- **Distinct Values:** 10,000

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 9,999

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.3041 chars
- **Distinct Values:** 44

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 116.2159 chars
- **Distinct Values:** 9,999

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.3776 chars
- **Distinct Values:** 849

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4882 chars
- **Distinct Values:** 2

### refund_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40.0
- **Average:** 10.146
- **Distinct Values:** 3

### shopify_billing_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 208,846.0 to 32,349,309.0
- **Average:** 20,234,272.84181256
- **Distinct Values:** 9,061
- **Null %:** 2.9%

### shopify_customer_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 348,683.0 to 43,008,768.0
- **Average:** 27,388,399.1049
- **Distinct Values:** 7,922

### shopify_financial_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 5.0 to 11.0
- **Average:** 6.8798
- **Distinct Values:** 4

### shopify_fulfillment_status_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 12.0 to 15.0
- **Average:** 12.0391
- **Distinct Values:** 3

### shopify_order_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.1618
- **Distinct Values:** 2

### shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 57.0 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 555,317.0 to 32,349,310.0
- **Average:** 21,658,779.531373657
- **Distinct Values:** 5,095
- **Null %:** 46.9%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 663.6701759999999
- **Distinct Values:** 1,216

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### total_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 19,500.0
- **Average:** 622.811323
- **Distinct Values:** 1,417

### total_tax

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 730.68
- **Average:** 15.953373999999998
- **Distinct Values:** 435

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,927

### user_owe_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk2_shopify_app_shopifyorder_raw {#postgres-lk2-shopify-app-shopifyorder-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyorder_raw`

<details>
<summary><strong>📊 Columns (54 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 103

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 673.826176
- **Distinct Values:** 1,475

### applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 76,377.0
- **Average:** 44.77312400000003
- **Distinct Values:** 736

### cancel_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6022 chars
- **Distinct Values:** 3

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,211,275.0 to 119,066,912.0
- **Average:** 79,342,889.7938
- **Distinct Values:** 10,000

### conversation_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### create_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,991

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4882 chars
- **Distinct Values:** 2

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9989 chars
- **Distinct Values:** 7,919

### edit_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.4576 chars
- **Distinct Values:** 7,628

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.4837 chars
- **Distinct Values:** 3,930

### fixed_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 572.2239
- **Distinct Values:** 1,360

### is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4344
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.677 chars
- **Distinct Values:** 3,577

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.9986 chars
- **Distinct Values:** 10,000

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 9,999

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.3041 chars
- **Distinct Values:** 44

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 116.2159 chars
- **Distinct Values:** 9,999

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.3776 chars
- **Distinct Values:** 849

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4882 chars
- **Distinct Values:** 2

### refund_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40.0
- **Average:** 10.146
- **Distinct Values:** 3

### shopify_billing_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 208,846.0 to 32,349,309.0
- **Average:** 20,234,455.360968046
- **Distinct Values:** 9,061
- **Null %:** 2.9%

### shopify_customer_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 348,683.0 to 43,008,768.0
- **Average:** 27,388,529.157000005
- **Distinct Values:** 7,923

### shopify_financial_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 5.0 to 11.0
- **Average:** 6.8798
- **Distinct Values:** 4

### shopify_fulfillment_status_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 12.0 to 15.0
- **Average:** 12.0391
- **Distinct Values:** 3

### shopify_order_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.1618
- **Distinct Values:** 2

### shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 57.0 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 555,317.0 to 32,349,310.0
- **Average:** 21,659,423.65957046
- **Distinct Values:** 5,096
- **Null %:** 46.9%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40,333.0
- **Average:** 663.6801759999998
- **Distinct Values:** 1,216

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### total_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 19,500.0
- **Average:** 622.8213230000001
- **Distinct Values:** 1,417

### total_tax

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 730.68
- **Average:** 15.962815999999997
- **Distinct Values:** 435

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,927

### user_owe_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk2_shopify_app_shopifyproduct {#postgres-lk2-shopify-app-shopifyproduct}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyproduct`

<details>
<summary><strong>📊 Columns (18 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 64

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 9,872.0
- **Average:** 9,126.289
- **Distinct Values:** 9

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,390

### default_variant_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 5,470,942.0
- **Average:** 42,058.52842156624
- **Distinct Values:** 8,199
- **Null %:** 18.0%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5825 chars
- **Distinct Values:** 4,687

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### fetched_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5825 chars
- **Distinct Values:** 4,687

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 47.021 chars
- **Distinct Values:** 4,651

### popularity

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 152,000.0
- **Average:** 2,330.878592370482
- **Distinct Values:** 854
- **Null %:** 40.0%

### product_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 10,000

### product_link

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.5119 chars
- **Distinct Values:** 2,462

### purchasable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### sale_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 140,000.0
- **Average:** 1,649.59369480361
- **Distinct Values:** 1,046
- **Null %:** 18.0%

### sku

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.7072 chars
- **Distinct Values:** 3,759

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,211

</details>

</details>

---

## postgres_lk2_shopify_app_shopifyproduct_raw {#postgres-lk2-shopify-app-shopifyproduct-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyproduct_raw`

<details>
<summary><strong>📊 Columns (18 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 55

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 9,872.0
- **Average:** 9,126.289
- **Distinct Values:** 9

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,390

### default_variant_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 5,470,942.0
- **Average:** 42,058.522932422544
- **Distinct Values:** 8,199
- **Null %:** 18.0%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5827 chars
- **Distinct Values:** 4,685

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### fetched_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5827 chars
- **Distinct Values:** 4,685

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 47.0141 chars
- **Distinct Values:** 4,651

### popularity

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 152,000.0
- **Average:** 2,330.5765767116445
- **Distinct Values:** 851
- **Null %:** 40.0%

### product_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 10,000

### product_link

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.5119 chars
- **Distinct Values:** 2,462

### purchasable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### sale_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 140,000.0
- **Average:** 1,649.6864003415462
- **Distinct Values:** 1,042
- **Null %:** 18.0%

### sku

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.7071 chars
- **Distinct Values:** 3,759

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,211

</details>

</details>

---

## postgres_lk2_store_ordermodel {#postgres-lk2-store-ordermodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_ordermodel`

<details>
<summary><strong>📊 Columns (33 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 81

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,607.0
- **Average:** 7,886.9239
- **Distinct Values:** 158

### amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 101,800.0
- **Average:** 1,376.4268030000046
- **Distinct Values:** 2,796

### attribution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 68,327.0 to 68,478.0
- **Average:** 68,402.5
- **Distinct Values:** 3
- **Null %:** 100.0%

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.037
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.008 chars
- **Distinct Values:** 4,361

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,431

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 5

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9926 chars
- **Distinct Values:** 9,767

### delivery_date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.6323 chars
- **Distinct Values:** 9,475

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,905

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.3815 chars
- **Distinct Values:** 5,515

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.0602 chars
- **Distinct Values:** 5

### item_names

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 98.6283 chars
- **Distinct Values:** 5,770

### items

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1,217.9743 chars
- **Distinct Values:** 9,906

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.3284 chars
- **Distinct Values:** 4,841

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 9.4534 chars
- **Distinct Values:** 9,906

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9979 chars
- **Distinct Values:** 9,908

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3306 chars
- **Distinct Values:** 274

### payment_method

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0018 chars
- **Distinct Values:** 3

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.3024 chars
- **Distinct Values:** 8

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.712 chars
- **Distinct Values:** 9,577

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9991 chars
- **Distinct Values:** 16

### refund_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 10,941.0
- **Average:** 25.779347
- **Distinct Values:** 69

### shopify_store_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 12,974.0
- **Average:** 3,820.2992897869367
- **Distinct Values:** 158
- **Null %:** 0.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 101,800.0
- **Average:** 1,350.106913073927
- **Distinct Values:** 2,427
- **Null %:** 0.0%

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 46.925 chars
- **Distinct Values:** 4,073

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,002

</details>

</details>

---

## postgres_lk2_store_ordermodel_raw {#postgres-lk2-store-ordermodel-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_ordermodel_raw`

<details>
<summary><strong>📊 Columns (33 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 65

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 19,409.0
- **Average:** 15,876.487
- **Distinct Values:** 11

### amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 862,808.0
- **Average:** 6,339.9953709999945
- **Distinct Values:** 2,402

### attribution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0992
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.4112 chars
- **Distinct Values:** 7,937

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4492 chars
- **Distinct Values:** 2

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.4345 chars
- **Distinct Values:** 6,233

### delivery_date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.8776 chars
- **Distinct Values:** 5,056

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.337 chars
- **Distinct Values:** 4,234

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.1268 chars
- **Distinct Values:** 4

### item_names

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 79.6488 chars
- **Distinct Values:** 6,228

### items

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1,219.1025 chars
- **Distinct Values:** 10,001

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.305 chars
- **Distinct Values:** 4,020

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.786 chars
- **Distinct Values:** 9,615

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.7007 chars
- **Distinct Values:** 10,000

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.783 chars
- **Distinct Values:** 1,628

### payment_method

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.664 chars
- **Distinct Values:** 6

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.0538 chars
- **Distinct Values:** 5,912

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4492 chars
- **Distinct Values:** 2

### refund_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26,930.0
- **Average:** 261.51525100000015
- **Distinct Values:** 373

### shopify_store_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 9.0 to 10,328.0
- **Average:** 8,862.69052579973
- **Distinct Values:** 8
- **Null %:** 18.4%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 862,808.0
- **Average:** 6,079.040119999997
- **Distinct Values:** 1,667

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 53.2 chars
- **Distinct Values:** 5,534

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,126

</details>

</details>

---

## postgres_lk2_store_productcollectionmodel {#postgres-lk2-store-productcollectionmodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_productcollectionmodel`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 77

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,512.0
- **Average:** 918.7357000000002
- **Distinct Values:** 99

### collection_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.8821 chars
- **Distinct Values:** 9,753

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 793

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.0437 chars
- **Distinct Values:** 8,530

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9958 chars
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,703

</details>

</details>

---

## postgres_lk2_store_productcollectionmodel_raw {#postgres-lk2-store-productcollectionmodel-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_productcollectionmodel_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 26

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,512.0
- **Average:** 918.7357000000002
- **Distinct Values:** 99

### collection_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.8821 chars
- **Distinct Values:** 9,753

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 793

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.0234 chars
- **Distinct Values:** 8,518

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9958 chars
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,466

</details>

</details>

---

## postgres_lk_account_accountmodel {#postgres-lk-account-accountmodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountmodel`

<details>
<summary><strong>📊 Columns (19 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 112

### bobble_ai_account_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 100.0%

### checkout_provider_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 34.0 to 103.0
- **Average:** 84.5
- **Distinct Values:** 7
- **Null %:** 99.7%

### crm_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 4,456.0
- **Average:** 2,758.4705882352937
- **Distinct Values:** 596
- **Null %:** 70.3%

### dashboard_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 23.964071856287426 chars
- **Distinct Values:** 647

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2,004

### facebook_page_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### gitlab_private_token

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.17964071856287425 chars
- **Distinct Values:** 2

### gitlab_project_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0718562874251497 chars
- **Distinct Values:** 19

### is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2994011976047904
- **Distinct Values:** 2

### logistics_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 5,117.0
- **Average:** 3,624.8310139165
- **Distinct Values:** 504
- **Null %:** 74.9%

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.328842315369261 chars
- **Distinct Values:** 2,004

### payment_channels_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 1,139.0
- **Average:** 738.4347826086956
- **Distinct Values:** 46
- **Null %:** 97.7%

### shortio_authorization

- **Type:** `Text`
- **Semantic Type:** `Author`
- **Nullable:** No
- **Avg Length:** 1.0778443113772456 chars
- **Distinct Values:** 3

### shortio_domain

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.5484031936127745 chars
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 13,674.0
- **Average:** 7,146.391666666666
- **Distinct Values:** 717
- **Null %:** 64.1%

### user_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 27,659.0
- **Average:** 15,449.579789894948
- **Distinct Values:** 2,000
- **Null %:** 0.2%

</details>

</details>

---

## postgres_lk_account_accountproperties {#postgres-lk-account-accountproperties}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountproperties`

<details>
<summary><strong>📊 Columns (24 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,703.0
- **Average:** 22,422.32342007435
- **Distinct Values:** 259

### broadcasts

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### cost_per_bot

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.9417472118959106
- **Distinct Values:** 22

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### crm

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### deal_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.45353159851301 chars
- **Distinct Values:** 269

### deal_owner

- **Type:** `Text`
- **Semantic Type:** `Owner`
- **Nullable:** No
- **Avg Length:** 12.58736059479554 chars
- **Distinct Values:** 15

### deal_stage

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.431226765799256 chars
- **Distinct Values:** 4

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 269

### flows

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### free_active_contacts

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### free_agents

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 60.0
- **Average:** 4.144981412639405
- **Distinct Values:** 20

### free_bot_sessions

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 150,000.0
- **Average:** 2,473.977695167286
- **Distinct Values:** 14

### ig

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.12267657992565056
- **Distinct Values:** 2

### ndr

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### nps

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### outbound_cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.02758364312267658
- **Distinct Values:** 11

### per_agent_fee

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3,000.0
- **Average:** 1,104.2081784386617
- **Distinct Values:** 28

### pipeline

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### type_of_bot

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.79182156133829 chars
- **Distinct Values:** 6

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk_account_accountproperties_raw {#postgres-lk-account-accountproperties-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountproperties_raw`

<details>
<summary><strong>📊 Columns (24 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,703.0
- **Average:** 22,422.32342007435
- **Distinct Values:** 259

### broadcasts

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### cost_per_bot

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.9417472118959106
- **Distinct Values:** 22

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### crm

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### deal_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.45353159851301 chars
- **Distinct Values:** 269

### deal_owner

- **Type:** `Text`
- **Semantic Type:** `Owner`
- **Nullable:** No
- **Avg Length:** 12.58736059479554 chars
- **Distinct Values:** 15

### deal_stage

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.431226765799256 chars
- **Distinct Values:** 4

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 269

### flows

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### free_active_contacts

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### free_agents

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 60.0
- **Average:** 4.144981412639405
- **Distinct Values:** 20

### free_bot_sessions

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 150,000.0
- **Average:** 2,473.977695167286
- **Distinct Values:** 14

### ig

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.12267657992565056
- **Distinct Values:** 2

### ndr

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### nps

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### outbound_cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.02758364312267658
- **Distinct Values:** 11

### per_agent_fee

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3,000.0
- **Average:** 1,104.2081784386617
- **Distinct Values:** 28

### pipeline

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### type_of_bot

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.79182156133829 chars
- **Distinct Values:** 6

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk_bifrostbridge_leadsqauredconvomapping {#postgres-lk-bifrostbridge-leadsqauredconvomapping}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_bifrostbridge_leadsqauredconvomapping`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 777

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 20,465.0 to 20,465.0
- **Average:** 20,465.0
- **Distinct Values:** 1

### convo_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 35,552.0 to 225,534.0
- **Average:** 111,482.1682
- **Distinct Values:** 8,637

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,882

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### integration_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 21.0 to 21.0
- **Average:** 21.0
- **Distinct Values:** 1

### lead_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 8,256

### opportunity_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 9,981

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,883

</details>

</details>

---

## postgres_lk_bifrostbridge_leadsquaredusers {#postgres-lk-bifrostbridge-leadsquaredusers}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_bifrostbridge_leadsquaredusers`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 20,465.0 to 20,465.0
- **Average:** 20,465.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 11

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 198

### integration_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 21.0 to 21.0
- **Average:** 21.0
- **Distinct Values:** 1

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 16

### user_email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 33.7020202020202 chars
- **Distinct Values:** 198

### user_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 196

</details>

</details>

---

## postgres_lk_influenced_sales {#postgres-lk-influenced-sales}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_influenced_sales`

<details>
<summary><strong>📊 Columns (21 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 27,269.0
- **Average:** 10,571.4201
- **Distinct Values:** 130

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 865,000.0
- **Average:** 1,426.0220320000008
- **Distinct Values:** 2,760

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,895

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 6

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### identifier

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.423 chars
- **Distinct Values:** 218

### interaction_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### last_interaction

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 9,859

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 0.8548 chars
- **Distinct Values:** 215

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 9,999

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.9966 chars
- **Distinct Values:** 9,805

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 4.8984 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,869

### utm_campaign

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0077 chars
- **Distinct Values:** 5

### utm_content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0013 chars
- **Distinct Values:** 2

### utm_medium

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0054 chars
- **Distinct Values:** 6

### utm_source

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0058 chars
- **Distinct Values:** 5

### utm_term

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk_influenced_sales_raw {#postgres-lk-influenced-sales-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_influenced_sales_raw`

<details>
<summary><strong>📊 Columns (21 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 438

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 51.0 to 28,101.0
- **Average:** 13,808.2165
- **Distinct Values:** 82

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 991,000.0
- **Average:** 3,463.7873379999833
- **Distinct Values:** 3,799

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,580

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 6

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### identifier

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.155 chars
- **Distinct Values:** 281

### interaction_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.7006 chars
- **Distinct Values:** 3

### last_interaction

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,860
- **Null %:** 0.2%

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.2038 chars
- **Distinct Values:** 139

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.6293 chars
- **Distinct Values:** 10,001

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.1976 chars
- **Distinct Values:** 5,641

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 7.7391 chars
- **Distinct Values:** 7

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,577

### utm_campaign

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.3857 chars
- **Distinct Values:** 38

### utm_content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.1168 chars
- **Distinct Values:** 9

### utm_medium

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0563 chars
- **Distinct Values:** 17

### utm_source

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.1029 chars
- **Distinct Values:** 20

### utm_term

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0447 chars
- **Distinct Values:** 8

</details>

</details>

---

## postgres_lk_shopify_app_event {#postgres-lk-shopify-app-event}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_event`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 249.0 to 27,116.0
- **Average:** 18,405.0
- **Distinct Values:** 4

### agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 50,274.0
- **Average:** 38,102.6
- **Distinct Values:** 4
- **Null %:** 28.6%

### conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,261.0 to 66,278.0
- **Average:** 16,070.6
- **Distinct Values:** 4
- **Null %:** 28.6%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 7

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 1

### order_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,940,734.0 to 12,895,987.0
- **Average:** 10,944,091.142857144
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7

</details>

</details>

---

## postgres_lk_shopify_app_event_raw {#postgres-lk-shopify-app-event-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_event_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 249.0 to 27,116.0
- **Average:** 12,791.307692307691
- **Distinct Values:** 5

### agent_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 51,882.0
- **Average:** 39,712.666666666664
- **Distinct Values:** 7
- **Null %:** 30.8%

### conversation_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,261.0 to 1,380,088.0
- **Average:** 620,664.8888888889
- **Distinct Values:** 8
- **Null %:** 30.8%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 13

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.0 chars
- **Distinct Values:** 1

### order_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 8,940,734.0 to 21,306,349.0
- **Average:** 15,474,764.538461538
- **Distinct Values:** 11

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

</details>

</details>

---

## postgres_lk_shopify_app_orderrefund {#postgres-lk-shopify-app-orderrefund}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_orderrefund`

<details>
<summary><strong>📊 Columns (15 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 138

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,344

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,349

### is_created_on_shopify

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9970348406226834
- **Distinct Values:** 2

### last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,344

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.25352112676056 chars
- **Distinct Values:** 2

### order_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1,214,523.0 to 19,522,599.0
- **Average:** 5,976,871.01055807
- **Distinct Values:** 1,321
- **Null %:** 1.7%

### processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 264
- **Null %:** 80.5%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3395107487027427 chars
- **Distinct Values:** 264

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 50.0 to 30,814.0
- **Average:** 584.4046627131207
- **Distinct Values:** 125

</details>

</details>

---

## postgres_lk_shopify_app_shopifyorder {#postgres-lk-shopify-app-shopifyorder}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_shopifyorder`

<details>
<summary><strong>📊 Columns (51 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,291

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,314.0
- **Average:** 11,051.385000000002
- **Distinct Values:** 192

### agent_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 218,250.0
- **Average:** 1,360.6435190000007
- **Distinct Values:** 3,855

### applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 61,626.42
- **Average:** 209.629479
- **Distinct Values:** 1,930

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### cart_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 89,297.0 to 88,804,557.0
- **Average:** 39,222,920.8871
- **Distinct Values:** 10,001

### conversation_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### create_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 10,001

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9952 chars
- **Distinct Values:** 9,990

### edit_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.661 chars
- **Distinct Values:** 8,899

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.1957 chars
- **Distinct Values:** 5,661

### fixed_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 218,250.0
- **Average:** 1,318.9819960000002
- **Distinct Values:** 3,740

### is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3166
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.7637 chars
- **Distinct Values:** 5,510

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.1311 chars
- **Distinct Values:** 9,994

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9971 chars
- **Distinct Values:** 10,000

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.6181 chars
- **Distinct Values:** 683

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 126.237 chars
- **Distinct Values:** 10,001

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.0914 chars
- **Distinct Values:** 3,420

### refund_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 8,000.0
- **Average:** 23.644699
- **Distinct Values:** 161

### shopify_billing_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 37,614.0 to 22,608,912.0
- **Average:** 12,813,616.233312732
- **Distinct Values:** 6,459
- **Null %:** 35.3%

### shopify_customer_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 27,499.0 to 34,679,774.0
- **Average:** 14,565,611.7394
- **Distinct Values:** 9,990

### shopify_financial_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 5.0 to 11.0
- **Average:** 7.1879
- **Distinct Values:** 7

### shopify_fulfillment_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12.0 to 15.0
- **Average:** 12.1618
- **Distinct Values:** 4

### shopify_order_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.6351
- **Distinct Values:** 3

### shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 63.4768 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 37,614.0 to 22,608,912.0
- **Average:** 12,611,120.24722906
- **Distinct Values:** 6,495
- **Null %:** 35.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 218,250.0
- **Average:** 1,336.2823520000002
- **Distinct Values:** 3,355

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### total_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 218,250.0
- **Average:** 1,285.4034080000008
- **Distinct Values:** 3,737

### total_tax

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 22,419.64
- **Average:** 80.27825100000003
- **Distinct Values:** 2,546

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,987

### user_owe_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk_shopify_app_shopifyorder_raw {#postgres-lk-shopify-app-shopifyorder-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_shopifyorder_raw`

<details>
<summary><strong>📊 Columns (51 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 13

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 41.0
- **Average:** 40.143
- **Distinct Values:** 3

### agent_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 23,324.0
- **Average:** 774.1839309999999
- **Distinct Values:** 665

### applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 2,455.0
- **Average:** 5.905039
- **Distinct Values:** 86

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 93,002.0 to 2,366,411.0
- **Average:** 273,336.46059999993
- **Distinct Values:** 9,999

### conversation_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### create_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,373

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9998 chars
- **Distinct Values:** 8,712

### edit_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 23.1392 chars
- **Distinct Values:** 8,692

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.1665 chars
- **Distinct Values:** 4,389

### fixed_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 8,847.0
- **Average:** 2.43129
- **Distinct Values:** 12

### is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0083
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.767 chars
- **Distinct Values:** 4,521

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.0795 chars
- **Distinct Values:** 10,001

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.0 chars
- **Distinct Values:** 10,001

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0451 chars
- **Distinct Values:** 33

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 128.7491 chars
- **Distinct Values:** 10,001

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4648 chars
- **Distinct Values:** 8,334

### refund_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### refunded_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 50.0
- **Average:** 0.27
- **Distinct Values:** 4

### shopify_billing_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 33,174.0 to 1,181,302.0
- **Average:** 765,133.4975124379
- **Distinct Values:** 186
- **Null %:** 98.0%

### shopify_customer_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 27,261.0 to 1,463,024.0
- **Average:** 89,921.7998
- **Distinct Values:** 8,713

### shopify_financial_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 5.0 to 11.0
- **Average:** 7.980099999999998
- **Distinct Values:** 4

### shopify_fulfillment_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12.0 to 15.0
- **Average:** 12.0021
- **Distinct Values:** 3

### shopify_order_status_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 2.9575
- **Distinct Values:** 3

### shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 64.8321 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 33,174.0 to 1,181,302.0
- **Average:** 742,236.4867256638
- **Distinct Values:** 104
- **Null %:** 98.9%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 23,324.0
- **Average:** 773.9139309999998
- **Distinct Values:** 664

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### total_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 23,324.0
- **Average:** 773.7136079999999
- **Distinct Values:** 661

### total_tax

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1,349.54
- **Average:** 0.8330079999999999
- **Distinct Values:** 38

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,106

### user_owe_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### user_refund_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

</details>

</details>

---

## postgres_lk_store_customermodel {#postgres-lk-store-customermodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_customermodel`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 628

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 272.0
- **Average:** 65.0524
- **Distinct Values:** 4

### address

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 344.218 chars
- **Distinct Values:** 8,779

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,268

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.0 chars
- **Distinct Values:** 9,996

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.2257 chars
- **Distinct Values:** 9,743

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.1337 chars
- **Distinct Values:** 5,310

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.4367 chars
- **Distinct Values:** 4,503

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.7975 chars
- **Distinct Values:** 1,496

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tags

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,168

</details>

</details>

---

## postgres_lk_store_igmedia {#postgres-lk-store-igmedia}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_igmedia`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 36

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 54.0 to 27,489.0
- **Average:** 14,109.5298
- **Distinct Values:** 29

### caption

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 392.5199 chars
- **Distinct Values:** 9,192

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,956

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,998

### ig_user_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.0 chars
- **Distinct Values:** 37

### media_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.0 chars
- **Distinct Values:** 10,000

### media_product_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.4321 chars
- **Distinct Values:** 2

### media_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.4147 chars
- **Distinct Values:** 3

### media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 127.1902 chars
- **Distinct Values:** 9,881

### post_link

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 41.3095 chars
- **Distinct Values:** 10,001

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### thumbnail_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 136.5052 chars
- **Distinct Values:** 4,615

### variant_ids

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 25.994 chars
- **Distinct Values:** 1,986

</details>

</details>

---

## postgres_lk_store_ordermodel {#postgres-lk-store-ordermodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_ordermodel`

<details>
<summary><strong>📊 Columns (35 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,315

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,220.0
- **Average:** 5,775.7167
- **Distinct Values:** 284

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 98,671.0
- **Average:** 1,290.0230010000005
- **Distinct Values:** 3,686

### attribution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 59,568.0 to 63,992.0
- **Average:** 61,780.0
- **Distinct Values:** 3
- **Null %:** 100.0%

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0536
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.884 chars
- **Distinct Values:** 5,277

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,994

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.7045 chars
- **Distinct Values:** 8

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9943 chars
- **Distinct Values:** 9,854

### delivery_date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### discount_codes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 27.1293 chars
- **Distinct Values:** 2,443

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 21.1784 chars
- **Distinct Values:** 9,069

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.4216 chars
- **Distinct Values:** 5,834

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.3862 chars
- **Distinct Values:** 7

### item_names

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 89.627 chars
- **Distinct Values:** 7,048

### items

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1,198.7084 chars
- **Distinct Values:** 9,921

### landing_site_ref

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.025 chars
- **Distinct Values:** 12

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.6795 chars
- **Distinct Values:** 5,135

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.8993 chars
- **Distinct Values:** 9,993

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9872 chars
- **Distinct Values:** 10,000

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.5664 chars
- **Distinct Values:** 613

### order_status_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 14.764 chars
- **Distinct Values:** 1,180

### payment_method

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0174 chars
- **Distinct Values:** 7

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.3105 chars
- **Distinct Values:** 13

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.726 chars
- **Distinct Values:** 9,862

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.694 chars
- **Distinct Values:** 19

### shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2,600.0
- **Average:** 19.927707
- **Distinct Values:** 116

### shopify_store_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 4.0 to 12,913.0
- **Average:** 3,140.2258769407704
- **Distinct Values:** 265
- **Null %:** 13.1%

### sold_by_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0013
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### subtotal_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 98,671.0
- **Average:** 1,270.0422805784299
- **Distinct Values:** 3,293
- **Null %:** 0.4%

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 33.3393 chars
- **Distinct Values:** 3,653

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,018

</details>

</details>

---

## postgres_lk_store_productcollectionmodel {#postgres-lk-store-productcollectionmodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productcollectionmodel`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 89

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,512.0
- **Average:** 620.2106
- **Distinct Values:** 25

### collection_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.9533 chars
- **Distinct Values:** 1,445

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 94

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 1,445

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 17.6531 chars
- **Distinct Values:** 1,348

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,939

</details>

</details>

---

## postgres_lk_store_productcollectionmodel_raw {#postgres-lk-store-productcollectionmodel-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productcollectionmodel_raw`

<details>
<summary><strong>📊 Columns (10 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 12,512.0
- **Average:** 918.7357000000002
- **Distinct Values:** 99

### collection_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 36.8821 chars
- **Distinct Values:** 9,753

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 793

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 16.0193 chars
- **Distinct Values:** 8,516

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9958 chars
- **Distinct Values:** 2

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,572

</details>

</details>

---

## postgres_lk_store_productmodel {#postgres-lk-store-productmodel}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productmodel`

<details>
<summary><strong>📊 Columns (36 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 26,075.0 to 27,314.0
- **Average:** 26,772.1457
- **Distinct Values:** 3

### attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 193.3399 chars
- **Distinct Values:** 4,598

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,063

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 33.5814 chars
- **Distinct Values:** 2,258

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### faqs

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### fetched_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 262.0439 chars
- **Distinct Values:** 5,451

### image

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 106.0924 chars
- **Distinct Values:** 6,582

### inventory

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** -52.0 to 7,989.0
- **Average:** 6.848500000000001
- **Distinct Values:** 152

### inventory_management

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Avg Length:** 7.0008 chars
- **Distinct Values:** 2

### inventory_policy

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0244 chars
- **Distinct Values:** 2

### metafields

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 32.383 chars
- **Distinct Values:** 5,047

### name_synonyms

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### options

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 25.8537 chars
- **Distinct Values:** 447

### popularity

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 475,525.0
- **Average:** 154,609.2268
- **Distinct Values:** 9,861

### price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 100,320.0
- **Average:** 3,110.368362
- **Distinct Values:** 913

### product_created_on_store_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 6,765
- **Null %:** 0.4%

### product_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 34.998 chars
- **Distinct Values:** 6,503

### product_link

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 64.7706 chars
- **Distinct Values:** 6,492

### product_updated_on_store_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7,981
- **Null %:** 0.4%

### purchasable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### reorder_time_intervals

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### sale_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 100,320.0
- **Average:** 2,500.416150000001
- **Distinct Values:** 1,400

### shopify_store_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 12,242.0 to 12,933.0
- **Average:** 12,662.1896
- **Distinct Values:** 3

### sku

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.8054 chars
- **Distinct Values:** 9,595

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,764

### upsell_time_intervals

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### usage_time_intervals

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### variant_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 42.9986 chars
- **Distinct Values:** 10,000

### vendor

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 8.8974 chars
- **Distinct Values:** 291

</details>

</details>

---

## postgres_lk_store_store {#postgres-lk-store-store}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_store`

<details>
<summary><strong>📊 Columns (30 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 52

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,775.0
- **Average:** 18,439.755888650965
- **Distinct Values:** 933

### ayuvya_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### bebodywise_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### bigcommerce_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 36.0
- **Average:** 15.0
- **Distinct Values:** 5
- **Null %:** 99.5%

### biocule_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### damensch_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.32441113490364 chars
- **Distinct Values:** 516

### dukaan_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 34.0 to 36.0
- **Average:** 35.0
- **Distinct Values:** 3
- **Null %:** 99.8%

### emotorad_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 934

### farzicom_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 3.0
- **Average:** 2.75
- **Distinct Values:** 3
- **Null %:** 99.6%

### fb_catalog_gsheet

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.29764453961456105 chars
- **Distinct Values:** 4

### has_catalog_integration

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03854389721627409
- **Distinct Values:** 2

### hkvitals_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### kindlife_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### littlejoy_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### manmatters_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### pilgrim_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### powerlook_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### s3_csv

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4207708779443253 chars
- **Distinct Values:** 37

### shopg_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### shopify_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 13,216.0
- **Average:** 8,417.814269535675
- **Distinct Values:** 856
- **Null %:** 5.5%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### thedermaco_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 2.0
- **Average:** 1.5
- **Distinct Values:** 3
- **Null %:** 99.8%

### webhook_secret

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.033190578158458245 chars
- **Distinct Values:** 2

### wforwomen_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 67.0
- **Average:** 34.0
- **Distinct Values:** 4
- **Null %:** 99.7%

### woocommerce_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 472.0
- **Average:** 237.5
- **Distinct Values:** 13
- **Null %:** 98.7%

### wowskinscience_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

</details>

</details>

---

## postgres_lk_store_store_raw {#postgres-lk-store-store-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_store_raw`

<details>
<summary><strong>📊 Columns (30 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 52

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 28,775.0
- **Average:** 18,439.755888650965
- **Distinct Values:** 933

### ayuvya_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### bebodywise_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### bigcommerce_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 36.0
- **Average:** 15.0
- **Distinct Values:** 5
- **Null %:** 99.5%

### biocule_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### damensch_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.32441113490364 chars
- **Distinct Values:** 516

### dukaan_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 34.0 to 36.0
- **Average:** 35.0
- **Distinct Values:** 3
- **Null %:** 99.8%

### emotorad_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 934

### farzicom_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 3.0
- **Average:** 2.75
- **Distinct Values:** 3
- **Null %:** 99.6%

### fb_catalog_gsheet

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.29764453961456105 chars
- **Distinct Values:** 4

### has_catalog_integration

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03854389721627409
- **Distinct Values:** 2

### hkvitals_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### kindlife_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### littlejoy_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### manmatters_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### pilgrim_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### powerlook_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### s3_csv

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4207708779443253 chars
- **Distinct Values:** 37

### shopg_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

### shopify_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 13,216.0
- **Average:** 8,417.814269535675
- **Distinct Values:** 856
- **Null %:** 5.5%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### thedermaco_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 2.0
- **Average:** 1.5
- **Distinct Values:** 3
- **Null %:** 99.8%

### webhook_secret

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.033190578158458245 chars
- **Distinct Values:** 2

### wforwomen_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 67.0
- **Average:** 34.0
- **Distinct Values:** 4
- **Null %:** 99.7%

### woocommerce_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 472.0
- **Average:** 237.5
- **Distinct Values:** 13
- **Null %:** 98.7%

### wowskinscience_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 2
- **Null %:** 99.9%

</details>

</details>

---

## postgres_lk_test_lk_table_raw {#postgres-lk-test-lk-table-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_test_lk_table_raw`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7

### age

- **Type:** `Float`
- **Nullable:** No
- **Range:** 20.0 to 30.0
- **Average:** 23.555555555555557
- **Distinct Values:** 5

### another_col

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.3333333333333333 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 7.333333333333333 chars
- **Distinct Values:** 6

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.2222222222222223 chars
- **Distinct Values:** 4

</details>

</details>

---

## postgres_messages_message_tags {#postgres-messages-message-tags}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_messages_message_tags`

<details>
<summary><strong>📊 Columns (8 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,472

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,376

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.0028 chars
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 36.2169 chars
- **Distinct Values:** 9,992

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,376

</details>

</details>

---

## postgres_messages_taggables {#postgres-messages-taggables}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_messages_taggables`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 41

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 305

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tag_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### taggable_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 715,185,857.0 to 717,121,899.0
- **Average:** 716,868,665.7154
- **Distinct Values:** 9,999

### taggable_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 305

</details>

</details>

---

## postgres_sla_policies {#postgres-sla-policies}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_policies`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 56

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 28,397.0
- **Average:** 20,132.537313432837
- **Distinct Values:** 39

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.582089552238806
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 38.47761194029851 chars
- **Distinct Values:** 63

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 67

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7
- **Null %:** 91.0%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 10.432835820895523 chars
- **Distinct Values:** 26

### escalations

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 198.61194029850745 chars
- **Distinct Values:** 44

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 67

### metrics

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 159.83582089552237 chars
- **Distinct Values:** 46

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.014925373134329 chars
- **Distinct Values:** 55

### order

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7.0
- **Average:** 1.8656716417910448
- **Distinct Values:** 7

### reminders

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 114.55223880597015 chars
- **Distinct Values:** 25

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 66

</details>

</details>

---

## postgres_sla_policies_raw {#postgres-sla-policies-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_policies_raw`

<details>
<summary><strong>📊 Columns (16 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 78

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 28,397.0
- **Average:** 20,251.09900990099
- **Distinct Values:** 39

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6633663366336634
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 36.32673267326733 chars
- **Distinct Values:** 64

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 67

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7
- **Null %:** 94.1%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 9.148514851485148 chars
- **Distinct Values:** 28

### escalations

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 238.44554455445544 chars
- **Distinct Values:** 51

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 67

### metrics

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 169.05940594059405 chars
- **Distinct Values:** 60

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.237623762376238 chars
- **Distinct Values:** 55

### order

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7.0
- **Average:** 1.9801980198019802
- **Distinct Values:** 7

### reminders

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 123.21782178217822 chars
- **Distinct Values:** 27

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 100

</details>

</details>

---

## postgres_sla_trackers {#postgres-sla-trackers}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_trackers`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 286

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 20,465.0 to 20,465.0
- **Average:** 20,465.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 81,913,410.0 to 114,010,972.0
- **Average:** 112,908,764.1641
- **Distinct Values:** 2,479

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

### current_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 52,258.0
- **Average:** 51,095.29031230083
- **Distinct Values:** 40
- **Null %:** 37.2%

### escalation_level

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### event

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 6.0
- **Average:** 1.5933
- **Distinct Values:** 5

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### related_message_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 805,619,397.0 to 819,542,314.0
- **Average:** 810,761,389.0503597
- **Distinct Values:** 140
- **Null %:** 97.2%

### sla_policy_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 2.2243
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

</details>

</details>

---

## postgres_sla_trackers_raw {#postgres-sla-trackers-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_trackers_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 286

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 20,465.0 to 20,465.0
- **Average:** 20,465.0
- **Distinct Values:** 1

### conversation_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 81,913,410.0 to 114,010,972.0
- **Average:** 112,908,764.1641
- **Distinct Values:** 2,479

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

### current_assignee_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 52,258.0
- **Average:** 51,095.29031230083
- **Distinct Values:** 40
- **Null %:** 37.2%

### escalation_level

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### event

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 6.0
- **Average:** 1.5933
- **Distinct Values:** 5

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### related_message_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 805,619,397.0 to 819,542,314.0
- **Average:** 810,761,389.0503597
- **Distinct Values:** 140
- **Null %:** 97.2%

### sla_policy_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 2.2243
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

</details>

</details>

---

## postgres_taggables {#postgres-taggables}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_taggables`

<details>
<summary><strong>📊 Columns (9 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,881

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,913

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### tag_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 77,029.0
- **Average:** 17,089.450199999996
- **Distinct Values:** 771

### taggable_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 672,152,308.0 to 689,780,258.0
- **Average:** 680,969,426.2856
- **Distinct Values:** 9,992

### taggable_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,913

</details>

</details>

---

## postgres_teams {#postgres-teams}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_teams`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 105

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 28,431.0
- **Average:** 21,062.88529411765
- **Distinct Values:** 155

### allow_auto_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8411764705882353
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 340

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 36
- **Null %:** 89.7%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 9.76764705882353 chars
- **Distinct Values:** 116

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 340

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 12.55 chars
- **Distinct Values:** 264

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 340

</details>

</details>

---

## postgres_teams_raw {#postgres-teams-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_teams_raw`

<details>
<summary><strong>📊 Columns (11 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 121

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 24.0 to 28,431.0
- **Average:** 21,322.09560723514
- **Distinct Values:** 155

### allow_auto_assign

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.8087855297157622
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 340

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 36
- **Null %:** 91.0%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 10.253229974160206 chars
- **Distinct Values:** 118

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 340

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.219638242894057 chars
- **Distinct Values:** 268

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 387

</details>

</details>

---

## postgres_templates {#postgres-templates}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_templates`

<details>
<summary><strong>📊 Columns (28 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,838

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 27,578.0
- **Average:** 14,750.440499999997
- **Distinct Values:** 172

### allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.023
- **Distinct Values:** 2

### body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 316.7722 chars
- **Distinct Values:** 7,836

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.1344 chars
- **Distinct Values:** 6

### complex_template_config

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4928 chars
- **Distinct Values:** 18

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,926

### created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3229
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7,279.0
- **Average:** 787.1876000000001
- **Distinct Values:** 2,605

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,997

### footer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.58 chars
- **Distinct Values:** 381

### header

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.2183 chars
- **Distinct Values:** 307

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 107.0 to 34,375.0
- **Average:** 24,573.486299999982
- **Distinct Values:** 255

### is_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.5741 chars
- **Distinct Values:** 11

### media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 1.3575 chars
- **Distinct Values:** 10

### namespace

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.7856 chars
- **Distinct Values:** 78

### rejection_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### short_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.6464 chars
- **Distinct Values:** 8,412

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.9738 chars
- **Distinct Values:** 6

### template_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 131.5973 chars
- **Distinct Values:** 3,710

### template_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.5931 chars
- **Distinct Values:** 8,630

### template_custom_parameters

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### template_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.7428
- **Distinct Values:** 4

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,840

</details>

</details>

---

## postgres_templates_raw {#postgres-templates-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_templates_raw`

<details>
<summary><strong>📊 Columns (28 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 14

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 71.0
- **Average:** 50.4214
- **Distinct Values:** 21

### allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 311.9602 chars
- **Distinct Values:** 6,724

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.4648 chars
- **Distinct Values:** 4

### complex_template_config

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,882

### created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1549
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### display_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 10,142.0
- **Average:** 1,582.9088
- **Distinct Values:** 3,766

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,001

### footer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4843 chars
- **Distinct Values:** 346

### header

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3689 chars
- **Distinct Values:** 617

### inbox_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 10.0 to 34,219.0
- **Average:** 11,598.3447
- **Distinct Values:** 69

### is_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.4445 chars
- **Distinct Values:** 9

### media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 1.2218 chars
- **Distinct Values:** 24

### namespace

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.2384 chars
- **Distinct Values:** 7

### rejection_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### short_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.3657 chars
- **Distinct Values:** 7,318

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.9985 chars
- **Distinct Values:** 4

### template_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 119.2652 chars
- **Distinct Values:** 2,892

### template_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.2048 chars
- **Distinct Values:** 7,498

### template_custom_parameters

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.4028 chars
- **Distinct Values:** 156

### template_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.5401
- **Distinct Values:** 4

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 575

</details>

</details>

---

## postgres_users {#postgres-users}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_users`

<details>
<summary><strong>📊 Columns (43 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,671

### address

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3914 chars
- **Distinct Values:** 35

### availability

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 0.9098
- **Distinct Values:** 5

### calling_enabled

- **Type:** `Integer`
- **Nullable:** Yes

### concurrency_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2925
- **Distinct Values:** 2

### concurrency_limit

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 555,555.0
- **Average:** 95.31504655120632
- **Distinct Values:** 50
- **Null %:** 0.1%

### configs

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### confirmation_sent_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,702
- **Null %:** 24.9%

### confirmation_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.116 chars
- **Distinct Values:** 2,191

### confirmed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,066
- **Null %:** 15.4%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,479

### current_sign_in_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,198
- **Null %:** 32.0%

### current_sign_in_ip

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.8198 chars
- **Distinct Values:** 1,783

### default_view_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### default_view_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### display_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4407 chars
- **Distinct Values:** 339

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 23.4187 chars
- **Distinct Values:** 6,510

### encrypted_password

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 45.066 chars
- **Distinct Values:** 5,796

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 6,478

### helpdesk_admin

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0003
- **Distinct Values:** 2

### last_sign_in_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 7,865
- **Null %:** 20.3%

### last_sign_in_ip

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.8078 chars
- **Distinct Values:** 1,864

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 10.3066 chars
- **Distinct Values:** 5,498

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4656 chars
- **Distinct Values:** 1,472

### provider

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0 chars
- **Distinct Values:** 1

### pubsub_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 6,479

### reset_password_sent_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 937
- **Null %:** 87.8%

### reset_password_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.808 chars
- **Distinct Values:** 938

### shopify_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0114
- **Distinct Values:** 2

### sign_in_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26,944.0
- **Average:** 57.53750000000002
- **Distinct Values:** 459

### signature

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.5176 chars
- **Distinct Values:** 230

### signature_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.4096 chars
- **Distinct Values:** 3

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.385 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 1.61 chars
- **Distinct Values:** 459

### timezone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.0058 chars
- **Distinct Values:** 9

### tokens

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 225.3582 chars
- **Distinct Values:** 5,466

### ui_settings

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 5.7313 chars
- **Distinct Values:** 3

### uid

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.6602 chars
- **Distinct Values:** 7,501

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,627

### user_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0018
- **Distinct Values:** 2

### web_rtc_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

</details>

</details>

---

## postgresfb2_central_orders {#postgresfb2-central-orders}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb2_central_orders`

<details>
<summary><strong>📊 Columns (29 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 10

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12.0 to 11,563.0
- **Average:** 4,138.084100000002
- **Distinct Values:** 180

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,423.8074610000015
- **Distinct Values:** 2,773

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0068
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,523

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 8

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.6747 chars
- **Distinct Values:** 8,833

### discount_amount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 37,000.0
- **Average:** 272.7844269999999
- **Distinct Values:** 1,534

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.3969 chars
- **Distinct Values:** 9,345

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.4209 chars
- **Distinct Values:** 5,074

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.351 chars
- **Distinct Values:** 5

### integration_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 13,589.0
- **Average:** 5,796.0756
- **Distinct Values:** 180

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.4974 chars
- **Distinct Values:** 4,607

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.4479 chars
- **Distinct Values:** 9,973

### order_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.7155 chars
- **Distinct Values:** 9,051

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.3097 chars
- **Distinct Values:** 2,904

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.5774 chars
- **Distinct Values:** 10

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.2054 chars
- **Distinct Values:** 9,760

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 12

### shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3,170.0
- **Average:** 27.890595999999995
- **Distinct Values:** 56

### source_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 30,658.0 to 30,679.0
- **Average:** 30,668.5
- **Distinct Values:** 3
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.0243 chars
- **Distinct Values:** 5

### store_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 4.0
- **Average:** 1.0953
- **Distinct Values:** 3

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,396.5135260000004
- **Distinct Values:** 2,527

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 26.9285 chars
- **Distinct Values:** 2,528

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,522

</details>

</details>

---

## postgresfb2_central_orders_raw {#postgresfb2-central-orders-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb2_central_orders_raw`

<details>
<summary><strong>📊 Columns (29 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 10

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 12.0 to 11,563.0
- **Average:** 4,138.084100000002
- **Distinct Values:** 180

### amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,423.8074610000015
- **Distinct Values:** 2,773

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0068
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,523

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 8

### customer_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.6747 chars
- **Distinct Values:** 8,833

### discount_amount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 37,000.0
- **Average:** 272.7844269999999
- **Distinct Values:** 1,534

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.3969 chars
- **Distinct Values:** 9,345

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### first_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.4209 chars
- **Distinct Values:** 5,074

### fulfillment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.351 chars
- **Distinct Values:** 5

### integration_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 39.0 to 13,589.0
- **Average:** 5,796.0756
- **Distinct Values:** 180

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.4974 chars
- **Distinct Values:** 4,607

### order_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.4479 chars
- **Distinct Values:** 9,973

### order_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.7155 chars
- **Distinct Values:** 9,051

### order_notes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.3097 chars
- **Distinct Values:** 2,904

### payment_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.5774 chars
- **Distinct Values:** 10

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.2054 chars
- **Distinct Values:** 9,760

### presentment_currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 12

### shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3,170.0
- **Average:** 27.890595999999995
- **Distinct Values:** 56

### source_flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 30,658.0 to 30,679.0
- **Average:** 30,668.5
- **Distinct Values:** 3
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.0243 chars
- **Distinct Values:** 5

### store_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 4.0
- **Average:** 1.0953
- **Distinct Values:** 3

### subtotal_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,396.5135260000004
- **Distinct Values:** 2,527

### tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 26.9285 chars
- **Distinct Values:** 2,528

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,522

</details>

</details>

---

## postgresfb_block_activities {#postgresfb-block-activities}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 11

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,161

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.7915
- **Distinct Values:** 2

### block_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 49

### block_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.0036
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,161

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### flow_execution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,377.0 to 61,123.0
- **Average:** 29,305.7382
- **Distinct Values:** 5,796

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 529.0
- **Average:** 434.176
- **Distinct Values:** 11

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,163

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2,803,649.0 to 11,791,569.0
- **Average:** 9,751,403.218799992
- **Distinct Values:** 4,554

</details>

</details>

---

## postgresfb_block_activities_raw {#postgresfb-block-activities-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 11

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,161

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.7915
- **Distinct Values:** 2

### block_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 49

### block_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 3.0
- **Average:** 1.0036
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,161

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 10,000

### flow_execution_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 2,377.0 to 61,123.0
- **Average:** 29,305.7382
- **Distinct Values:** 5,796

### flow_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 166.0 to 529.0
- **Average:** 434.176
- **Distinct Values:** 11

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,163

### user_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2,803,649.0 to 11,791,569.0
- **Average:** 9,751,403.218799992
- **Distinct Values:** 4,554

</details>

</details>

---

## postgresfb_block_activities_raw_2 {#postgresfb-block-activities-raw-2}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities_raw_2`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No

### activity_time

- **Type:** `DateTime`
- **Nullable:** No

### activity_type

- **Type:** `Float`
- **Nullable:** No

### block_id

- **Type:** `Text`
- **Nullable:** No

### block_type

- **Type:** `Float`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No

### flow_execution_id

- **Type:** `Float`
- **Nullable:** Yes

### flow_id

- **Type:** `Float`
- **Nullable:** Yes

### src

- **Type:** `Text`
- **Nullable:** No

### updated_at

- **Type:** `DateTime`
- **Nullable:** No

### user_id

- **Type:** `Float`
- **Nullable:** No

</details>

</details>

---

## postgresfb_builder_user {#postgresfb-builder-user}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_builder_user`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,228

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 10,000

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### identity

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.9445 chars
- **Distinct Values:** 9,931

### ig_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0026 chars
- **Distinct Values:** 2

### ig_username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.8616 chars
- **Distinct Values:** 2,071

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5,891.0 to 5,892.0
- **Average:** 5,891.1
- **Distinct Values:** 3
- **Null %:** 99.9%

### phone

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.1897 chars
- **Distinct Values:** 5,207

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.4774 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,998

### wa_optin_status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 1

</details>

</details>

---

## postgresfb_builder_user_raw {#postgresfb-builder-user-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_builder_user_raw`

<details>
<summary><strong>📊 Columns (14 total)</strong></summary>

### id

- **Type:** `Float`
- **Semantic Type:** `PK`
- **Nullable:** No

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,289

### account_id

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,999

### eventn_ctx_event_id

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 9,999

### identity

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.5716 chars
- **Distinct Values:** 9,903

### ig_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### ig_username

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.9455 chars
- **Distinct Values:** 4,329

### inbox_id

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 925.0 to 927.0
- **Average:** 926.0
- **Distinct Values:** 3
- **Null %:** 100.0%

### phone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0182 chars
- **Distinct Values:** 10

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.9966 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 10,000

### wa_optin_status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 2.0 to 2.0
- **Average:** 2.0
- **Distinct Values:** 1

</details>

</details>

---

## postres2_bot_analytics {#postres2-bot-analytics}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `postres2_bot_analytics`

<details>
<summary><strong>📊 Columns (18 total)</strong></summary>

### account_id

- **Type:** `Integer`
- **Nullable:** No

### channel

- **Type:** `Text`
- **Nullable:** No

### conv_id

- **Type:** `Integer`
- **Nullable:** No

### conversation_id

- **Type:** `BigInteger`
- **Nullable:** No

### created_at

- **Type:** `Date`
- **Nullable:** No

### date

- **Type:** `Date`
- **Nullable:** No

### distinct_id

- **Type:** `Text`
- **Nullable:** No

### event_id

- **Type:** `BigInteger`
- **Nullable:** No

### event_name

- **Type:** `Text`
- **Nullable:** No

### event_type

- **Type:** `Integer`
- **Nullable:** No

### inbox_id

- **Type:** `Integer`
- **Nullable:** No

### inserted_at

- **Type:** `DateTime`
- **Nullable:** No

### is_outbound

- **Type:** `Integer`
- **Nullable:** No

### is_outside_working_hours

- **Type:** `Integer`
- **Nullable:** No

### products

- **Type:** `Text`
- **Nullable:** No

### properties

- **Type:** `Text`
- **Nullable:** No

### text

- **Type:** `Text`
- **Nullable:** No

### timestamp

- **Type:** `BigInteger`
- **Nullable:** No

</details>

</details>

---

## subscriptions {#subscriptions}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `subscriptions`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### __v_aibyte_transform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.3 chars
- **Distinct Values:** 2

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 20

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### apiuserid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 18.0 chars
- **Distinct Values:** 9

### channelname

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 8.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 20

### eventname

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 11.35 chars
- **Distinct Values:** 3

### inboxid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 27,881.0 to 35,028.0
- **Average:** 33,642.2
- **Distinct Values:** 11
- **Null %:** 25.0%

### islcsubscriber

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.25
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 14.6 chars
- **Distinct Values:** 6

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### umsenabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 52.8 chars
- **Distinct Values:** 6

</details>

</details>

---

## subscriptions_raw {#subscriptions-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `subscriptions_raw`

<details>
<summary><strong>📊 Columns (13 total)</strong></summary>

### __v_aibyte_transform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.3 chars
- **Distinct Values:** 2

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 20

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### apiuserid

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 18.0 chars
- **Distinct Values:** 9

### channelname

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 8.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 20

### eventname

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 11.35 chars
- **Distinct Values:** 3

### inboxid

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 27,881.0 to 35,028.0
- **Average:** 33,642.2
- **Distinct Values:** 11
- **Null %:** 25.0%

### islcsubscriber

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.25
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 14.6 chars
- **Distinct Values:** 6

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### umsenabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 52.8 chars
- **Distinct Values:** 6

</details>

</details>

---

## templates {#templates}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `templates`

<details>
<summary><strong>📊 Columns (19 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 2

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### allowcategorychange

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### bodycontent

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 35.0 chars
- **Distinct Values:** 2

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0 chars
- **Distinct Values:** 1

### createdat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

### displayid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3.0 to 4.0
- **Average:** 3.5
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2

### footer

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 189.0
- **Average:** 189.0
- **Distinct Values:** 1

### header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### inboxid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 716.0 to 716.0
- **Average:** 716.0
- **Distinct Values:** 1

### language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0 chars
- **Distinct Values:** 1

### shortcode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.5 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### templatecode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 2

### templatetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

</details>

</details>

---

## templates_raw {#templates-raw}

<details>
<summary><strong>📋 Table Details</strong></summary>

- **Schema:** `datawarehouse`
- **Raw Name:** `templates_raw`

<details>
<summary><strong>📊 Columns (19 total)</strong></summary>

### __v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 2

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### allowcategorychange

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### bodycontent

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 35.0 chars
- **Distinct Values:** 2

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0 chars
- **Distinct Values:** 1

### createdat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

### displayid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 3.0 to 4.0
- **Average:** 3.5
- **Distinct Values:** 2

### eventn_ctx_event_id

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 32.0 chars
- **Distinct Values:** 2

### footer

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### hdaccountid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 189.0 to 189.0
- **Average:** 189.0
- **Distinct Values:** 1

### header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### inboxid

- **Type:** `Float`
- **Nullable:** No
- **Range:** 716.0 to 716.0
- **Average:** 716.0
- **Distinct Values:** 1

### language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0 chars
- **Distinct Values:** 1

### shortcode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.5 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### templatecode

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 2

### templatetype

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0 chars
- **Distinct Values:** 1

### updatedat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

</details>

</details>

---
