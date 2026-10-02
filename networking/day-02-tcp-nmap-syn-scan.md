# Day 02 — TCP Handshake & Nmap SYN Scan

## Kết luận nhanh

```text
TCP 3-way handshake:
SYN → SYN/ACK → ACK

Với TCP SYN scan (-sS), đơn giản hóa:

SYN/ACK
→ strong evidence: open

RST / RST-ACK
→ strong evidence: closed

No useful response / filtering behavior
→ có thể được Nmap đánh giá là filtered tùy scan và evidence.

SYN scan thường là half-open:
SYN → SYN/ACK → RST

Ghi nhớ:
open ≠ vulnerable
Port number ≠ chắc chắn service
Tool output = evidence
```
