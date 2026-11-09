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

WireGuard · AmneziaWG · OpenVPN · OpenConnect · IKEv2 · VLESS · VMess · Trojan · Shadowsocks · Hysteria2 · TUIC — including V2Ray/Xray share links and subscription URLs, with REALITY, XTLS-Vision, WebSocket+TLS, gRPC and uTLS transports. Paste a link or config and the protocol, host, port and keys are detected for you. → [Protocol docs](https://docs.tunnelhq.com/protocols/)

### Alerts & incidents

- **20 alert channels** — Slack, PagerDuty, Telegram, Discord, email, Opsgenie, Teams, Signal, Matrix and more, plus HMAC-signed webhooks. Turn one on per project, per tunnel or per check. → [Alert channels](https://docs.tunnelhq.com/alert-channels/)
- **Confirm before paging** — the first failed check opens an incident; a second confirms it down before the alert goes out, then another when it recovers.
- **Every incident keeps its log** — when it went down, how long it lasted, who acknowledged it, when it recovered. → [Incidents](https://docs.tunnelhq.com/concepts/incidents/)

### Uptime monitoring

Watch websites, APIs, hosts and cron jobs in the same projects and alert channels as your tunnels — **free during beta**, and they don't count toward your tunnel limit.

- **Five check types** — Website, keyword, ping, TCP port and DNS, from every 20 seconds to every 30 minutes.
- **Response times & availability** charted for the last 24h, 7d, 30d and 90d.
- **SSL & domain expiry** — warns up to two months before a certificate or domain lapses.
- **Heartbeats for cron jobs** — the job pings a heartbeat URL each run; a missed call or reported failure alerts. → [Uptime docs](https://docs.tunnelhq.com/uptime/) · [Heartbeats](https://docs.tunnelhq.com/uptime/heartbeat/)

### AI assistants (MCP)

- **Built-in MCP server** — connect Claude, ChatGPT, Cursor and VS Code just by signing in; you choose the project and whether it's read-only or read-write. → [MCP docs](https://docs.tunnelhq.com/mcp/)
- **Set up by your assistant** — one prompt finds the sites, APIs and jobs in your project, asks before adding them, and tests each one. → [tunnelhq.com/ai](https://tunnelhq.com/ai/)

### Team workspaces & security

- Invite teammates as Admins, Managers or Viewers; **Viewers never see a tunnel's VPN credentials.**
- **Groups** sort tunnels by provider, location or customer — each group shows its worst status.
- Keys and passwords are **encrypted with AES-256-GCM** before they touch the database; the free tester keeps nothing. → [Team docs](https://docs.tunnelhq.com/team/)

### Migrate in minutes

Bulk import: paste share links and configs, or upload `.ovpn` / `.conf` files — each server becomes a tunnel. A V2Ray or Xray **subscription URL brings in a whole fleet and keeps it in sync**. Or create tunnels through the REST API.

### Build on it

| | |
|---|---|
| **REST API** — 34 endpoints, OpenAPI spec | https://docs.tunnelhq.com/api/ |
| **`thq` CLI** — test a config/link from your terminal or CI (exits 1 on failure) | https://docs.tunnelhq.com/cli/ |
| **MCP server** — Claude, ChatGPT, Cursor, VS Code | https://docs.tunnelhq.com/mcp/ |
| **Signed webhooks** — down/degraded/up & incident events | https://docs.tunnelhq.com/webhooks/ |

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
