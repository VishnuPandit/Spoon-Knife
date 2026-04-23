API Gateway required:
External to internal API traffic must route through bank-approved API gateway using supported auth (TUG 800-05-004). No direct core access from external clients.
Outbound B2B partner integrations that require stable network routes with central egress.
Authentication brokering between clients and services when client cannot meet auth requirements of service. (e.g. A client cannot meet service’s mTLS auth requirement. Client instead calls API gateway using OAuth and gateway routes request to service using mTLS)
API gateway recommended:
Internal to external calls when multiple internal clients need standard access to external service.
External to external calls when payload inspection and metric gathering needed. (e.g. vendor A calling vendor B’s API)
Internal to internal calls when central policy enforcement and consistent TLS/mTLS termination needed. (e.g. Tibco BW applications outbound API calls route through API Gateway)
API gateway not needed:
Internal to external API traffic that meets existing security policies and does not need shared access controls. Typically, single consumer integrations.
Native vendor SDK/connectors that handle client connections to vendor.
High throughput streaming services (e.g. Kafka, large file transfers). Should use other approved channels, not API gateways.
