# EOSIO-notes

---

Current Latest Versions

eos: 1.8.4 (available via homebrew)

eosio.cdt: 1.6.3 (available via homebrew)

eosio.contracts: 1.7.0 (unit tests do not build!)

---

### Endpoint Query

```bash
curl --request POST --url https://eos.greymass.com:443/v1/node/get_supported_apis | jq
```


### Activate Chain Features (not sure if this works?)
```bash
curl -X POST https://mynode.io:8888/v1/producer/schedule_protocol_feature_activations -d '{"protocol_features_to_activate": ["0ec7e080177b2c02b278d5088611686b49d739925a92d9bfcacd7fc6b74053bd"]}' | jq



#full steps



curl -X POST https://mynode.io:8888/v1/producer/schedule_protocol_feature_activations -d '{"protocol_features_to_activate": ["0ec7e080177b2c02b278d5088611686b49d739925a92d9bfcacd7fc6b74053bd"]}' | jq



cleos -u https://mynode.io:8888 set contract eosio /var/dapps/eosio.bios -p eosio



cleos -u https://mynode.io:8888 push action eosio activate '["f0af56d2c5a48d60a4a5b5c903edfb7db3a736a94ed589d0b797df33ff9d3e1d"]' -p eosio # GET_SENDER

cleos -u https://mynode.io:8888 push action eosio activate '["2652f5f96006294109b3dd0bbde63693f55324af452b799ee137a81a905eed25"]' -p eosio # FORWARD_SETCODE

cleos -u https://mynode.io:8888 push action eosio activate '["8ba52fe7a3956c5cd3a656a3174b931d3bb2abb45578befc59f283ecd816a405"]' -p eosio # ONLY_BILL_FIRST_AUTHORIZER

cleos -u https://mynode.io:8888 push action eosio activate '["68dcaa34c0517d19666e6b33add67351d8c5f69e999ca1e37931bc410a297428"]' -p eosio # DISALLOW_EMPTY_PRODUCER_SCHEDULE

cleos -u https://mynode.io:8888 push action eosio activate '["e0fb64b1085cc5538970158d05a009c24e276fb94e1a0bf6a528b48fbc4ff526"]' -p eosio # FIX_LINKAUTH_RESTRICTION

cleos -u https://mynode.io:8888 push action eosio activate '["ef43112c6543b88db2283a2e077278c315ae2c84719a8b25f25cc88565fbea99"]' -p eosio # REPLACE_DEFERRED

cleos -u https://mynode.io:8888 push action eosio activate '["4a90c00d55454dc5b059055ca213579c6ea856967712a56017487886a4d4cc0f"]' -p eosio # NO_DUPLICATE_DEFERRED_ID



cleos -u https://mynode.io:8888 push action eosio activate '["ad9e3d8f650687709fd68f4b90b41f7d825a365b02c23a636cef88ac2ac00c43"]' -p eosio # RESTRICT_ACTION_TO_SELF

cleos -u https://mynode.io:8888 push action eosio activate '["1a99a59d87e06e09ec5b028a9cbb7749b4a5ad8819004365d02dc4379a8b7241"]' -p eosio # ONLY_LINK_TO_EXISTING_PERMISSION

cleos -u https://mynode.io:8888 push action eosio activate '["4e7bf348da00a945489b2a681749eb56f5de00b900014e137ddae39f48f69d67"]' -p eosio # RAM_RESTRICTIONS
```