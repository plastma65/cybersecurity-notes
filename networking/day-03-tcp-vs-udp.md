# Day 03 — TCP vs UDP

## Kết luận nhanh

```text
TCP
→ Có cơ chế thiết lập kết nối trước khi truyền dữ liệu.
→ Có cơ chế reliability, ordering và retransmission.

UDP
→ Connectionless.
→ Không dùng TCP-style 3-way handshake.
→ Không tự đảm bảo delivery hay đúng thứ tự.

Khi Nmap quét UDP:

Valid UDP response
→ strong evidence: open

ICMP Port Unreachable
→ strong evidence: closed

Nothing / no response
→ KHÔNG đồng nghĩa closed.
→ Có thể service không phản hồi probe.
→ Có thể packet bị firewall/filter drop.
→ Có thể packet loss hoặc rate limiting.

open|filtered
→ Nmap chưa đủ evidence để phân biệt:
   open hay filtered.

Ghi nhớ:
UDP scan khó chủ yếu vì sự im lặng có nhiều cách giải thích.
```
