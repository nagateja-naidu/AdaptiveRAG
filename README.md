
## 1. Problem Statement

The challenge is to identify the **15 gateways that should be visited by an engineer each week**.

We are given historical telemetry data from a set of gateways. The telemetry contains information such as:

- `gateway_id` - unique identifier of each gateway
- `ts_utc` - timestamp of the observation
- `offline_duration_sec` - how long the gateway was offline
- `disconnection_cnt` - number of disconnections
- `reboot_cnt` - number of reboots

The goal is not simply to find gateways with the highest number of failures. The goal is to **prioritize the gateways that are most likely to need an engineering visit**, using only information that would have been available before making the prediction.

For every week, the system must produce exactly **15 gateways**, ordered from rank 1 to rank 15.

The required output contains:

```text
week_start
rank
gateway_id
score
reason# AdaptiveRAG
