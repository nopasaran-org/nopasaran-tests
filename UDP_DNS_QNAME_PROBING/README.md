## Overview

This state machine governs a test that establishes a control channel between a client and a server, then either sends a TCP-based DNS query from the client or processes it on the server.

## Test Variables Structure

The test relies on a `variables.json` file to configure both the control channel and the communication protocol between the client and the server.

```json
{
  "role": "TO_DO",
  "client": "client",
  "server": "server",
  "controller_conf_filename": "controller_configuration.json",
  "destination_port": "TO_DO",
  "ip": "TO_DO",
  "qname": "TO_DO",
  "qtype": "TO_DO",
  "response_spec": "TO_DO"
}
```

### Explanation of Variables

- **role**: Specifies the role of the current instance, either `"client"` or `"server"`. Determines whether the system will send a DNS query or host a DNS server to respond.

- **client**: Identifier for the client that will send a TCP DNS query.

- **server**: Identifier for the DNS server that will listen for and respond to queries.

- **controller_conf_filename**: Path to the controller configuration file (default: `"controller_configuration.json"`), which orchestrates coordination and shared state between client and server.

- **destination_port**: Server port number used for the TCP DNS communication.

- **ip**: IP address of the DNS server to which the query is directed (used by the client).

- **qname**: DNS query name that the client will use in the request (e.g., `"example.com"`).

- **qtype**: Type of DNS record to request (e.g., `"A"`, `"AAAA"`, `"MX"`).

- **response_spec**: A specification for how the server should respond to the query (e.g., predefined IP, TTL, record type).
