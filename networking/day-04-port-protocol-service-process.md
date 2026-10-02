# Day 04 — Port → Protocol → Service → Process

## Kết luận nhanh

```text
IP
→ xác định host/interface trên mạng.

Port
→ giúp hệ điều hành phân biệt endpoint
  của network communication.

Protocol
→ bộ quy tắc hai bên dùng để giao tiếp.

Service
→ chức năng mạng được hệ thống cung cấp.

Process
→ một chương trình đang thực thi.

Ví dụ:
22/tcp open
→ biết TCP port 22 đang open.

Chưa thể kết luận chắc chắn:
→ service gì?
→ software nào?
→ version nào?

-sV
→ giúp Nmap thực hiện service/version detection
  bằng probe và fingerprint response.

Ghi nhớ:
Port number ≠ chắc chắn service
open ≠ vulnerable
Tool output = evidence
Evidence → interpretation → conclusion
```

## Pentest mindset

```text
445/tcp open
      ↓
Service là gì?
      ↓
Nếu là SMB:
Authentication?
Guest/anonymous access?
Shares?
Read/Write permissions?
Sensitive information?
Misconfiguration?
Actual impact?
```

Authentication
→ "Tôi là ai?"

Authorization / Permissions
→ "Tôi được phép làm gì?"
