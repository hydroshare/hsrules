# hsrules

## iRODS Python rulesbase for Hydroshare

### Installation

1. For iRODS < 4.3, configure `"maximum_number_of_concurrent_rule_engine_server_processes": 1` in the `advanced_settings` stanza of `/etc/irods/server_config.json`.
1. For iRODS >= 4.3, configure `"number_of_concurrent_delay_rule_executors": 1` in `/etc/irods/server_config.json`.
1. Ensure that the `irods_rule_engine_plugin-cpp_default_policy-instance` instance is the last rule engine configured in `/etc/irods/server_congfig.json` if present.
1. Install the iRODS Python Rule Engine plug-in (PRE) to the iCAT server.
1. Configure the PRE in `/etc/irods/server_config.json` as the first rule engine.
1. Clone this repo to `/etc/irods` on the iCAT server.
1. Copy `core.py.hydroshare` to `/etc/irods/core.py` from either python2 (iRODS < 4.3) or python3 (iRODS >= 4.3) as appropriate.
1. Edit `/etc/irods/core.py` to provide real world values for `hsRestUser`, `hsRestPwd`, and `hsRestURL`.
