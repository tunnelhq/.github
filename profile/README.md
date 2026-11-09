<p align="center">
  <img src="./logo.svg" width="80" height="80" alt="TunnelHQ logo">
</p>

<h1 align="center">TunnelHQ</h1>

<p align="center">
  <b>Know the moment a VPN server goes down.</b><br>
  We run the real protocol handshake, not a ping — across 11 VPN protocols.
</p>

<p align="center">
  <a href="https://tunnelhq.com">Website</a> ·
  <a href="https://app.tunnelhq.com/register">Start free trial</a> ·
  <a href="https://tunnelhq.com/test/">Test a config free</a> ·
  <a href="https://docs.tunnelhq.com">Docs</a>
</p>

---

A port ping calls a VPN server healthy when nobody can actually connect. **TunnelHQ checks at the protocol layer** — completing the real handshake on every check, so wrong keys, expired preshared secrets, SNI blocks, REALITY misconfig and UDP shaping are caught, and a dead peer behind an open firewall port still fails and alerts you.

### 11 protocols, real handshakes

WireGuard · AmneziaWG · OpenVPN · OpenConnect · IKEv2 · VLESS · VMess · Trojan · Shadowsocks · Hysteria2 · TUIC — including V2Ray/Xray share links and subscription URLs, with REALITY, XTLS-Vision, WebSocket+TLS, gRPC and uTLS transports.

### What it does

- **Instant alerts** across 20 channels (Slack, PagerDuty, Telegram, Discord, email…) plus HMAC-signed webhooks, with incident logs and confirm-before-paging.
- **Uptime checks** for websites, APIs, hosts, TCP/DNS and cron heartbeats — same projects, same alert channels.
- **Team workspaces** with roles; credentials encrypted at rest with AES-256-GCM and hidden from viewers.

### Build on it

| | |
|---|---|
| **REST API** — 34 endpoints, OpenAPI spec | https://docs.tunnelhq.com/api/ |
| **`thq` CLI** — test a config/link from your terminal or CI | https://docs.tunnelhq.com/cli/ |
| **MCP server** — connect Claude, ChatGPT, Cursor, VS Code | https://docs.tunnelhq.com/mcp/ |
| **Webhooks** — signed down/degraded/up & incident events | https://docs.tunnelhq.com/webhooks/ |
| **Alert channels** | https://docs.tunnelhq.com/alert-channels/ |
| **Protocol docs** | https://docs.tunnelhq.com/protocols/ |

### Quick check via API

```bash
curl https://app.tunnelhq.com/api/v1/check \
  -H "X-API-Key: thk_••••••••" \
  -d '{"protocol": "wireguard", "config": "[Interface]…"}'
```

```json
{ "status": "healthy", "protocol": "wireguard", "connect_ms": 142, "latency_ms": 24, "exit_ip": "176.61.144.46" }
```

---

<p align="center"><sub>A <a href="https://digitald.tech">DigitalD.tech</a> project · <a href="https://docs.tunnelhq.com">docs.tunnelhq.com</a></sub></p>
