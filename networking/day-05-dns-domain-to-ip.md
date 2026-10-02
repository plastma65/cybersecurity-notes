# Day 05 — DNS: Domain → IP

## Kết luận nhanh

```text
DNS
→ giúp phân giải domain/hostname thành thông tin
  cần thiết, thường là IP address.

A
→ IPv4

AAAA
→ IPv6

CNAME
→ alias sang hostname khác

MX
→ mail server cho domain

DNS thường:
→ UDP/53

nhưng DNS cũng có thể:
→ TCP/53

DNS cache
→ tránh lookup lại không cần thiết.

TTL
→ kiểm soát thời gian cache của record.

Trong Offensive Security:
DNS information
→ giúp hiểu infrastructure
→ tìm subdomain/host
→ xây dựng attack surface

Nhưng:
discovered asset ≠ authorized target
```

## Mental model

```text
Domain
  ↓
DNS resolution
  ↓
IP address
  ↓
TCP connection
  ↓
TLS (HTTPS)
  ↓
HTTP
```

## CNAME example

```text
shop.example.com
    ↓ CNAME
store.example.net
    ↓ A
203.0.113.50

→ Client ultimately gets an IP address to connect to.
```

## Pentest mindset

```text
Interesting hostname
      ↓
Do NOT assume what it is from the name alone.
      ↓
First question:
Is this asset actually authorized by the scope?
      ↓
Then gather permitted evidence:
DNS records / service behavior / HTTP response / headers / content
      ↓
Evidence → interpretation → conclusion
```

> A hostname that looks old, dev, admin, staging, or internal is only a clue — not proof.
