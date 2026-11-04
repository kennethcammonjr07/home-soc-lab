# Tuning Log

## 2026-11-04 — Suppressed Suricata SID 2210064 for Quad9
- **Alert:** SURICATA STREAM 3way handshake SYN/ACK ignored TFO data (priority 3)
- **Source:** 149.112.112.112 / 9.9.9.9 (Quad9, Pi-hole's upstream DNS)
- **Investigation:** Fired repeatedly on normal Pi-hole → Quad9 DNS over TCP. Quad9 uses TCP Fast Open; Suricata flags early data in the handshake. Correlated with a Pi-hole CONNECTION_ERROR from the same IP. Benign.
- **Action:** Suppressed for Quad9 IPs only (threshold.config). Rule remains active for all other sources.
- **Result:** Removes the top source of noise from the Suricata Alerts panel.

## 2026-11-04 — Honeypot brute-force alert threshold set to 10
- **Reason:** Dashboard showed bursts up to ~11 attempts per 5 min; 10 catches real bursts without alerting on single probes. Will adjust if too noisy or too quiet.
