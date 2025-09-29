# Lab 03 – UML Thiết kế (Use Case & Sequence)

## Use Case: Withdraw Cash
Mô tả quy trình khách hàng rút tiền từ ATM.

```mermaid
%% UC Diagram
%% Mermaid chưa hỗ trợ Use Case chính thức, nhưng có thể biểu diễn bằng graph
graph TD
    Customer((Customer)) -->|Insert Card| UC1[Insert Card]
    Customer -->|Enter PIN| UC2[Enter PIN]
    Customer -->|Withdraw Cash| UC3[Withdraw Cash]

    UC3 --> UC4[Validate PIN]
    UC3 --> UC5[Dispense Cash]
    UC3 --> UC6[Print Receipt]

    UC2 --> UC4
    UC1 --> UC2

    UC3 --> Bank[(Bank Server)]
```

## Sequence: Withdraw Cash
Mô tả chi tiết luồng thông điệp giữa Customer, ATM và Bank Server.


```mermaid
sequenceDiagram
    participant C as Customer
    participant ATM as ATM Machine
    participant B as Bank Server

    C->>ATM: Insert Card
    ATM->>C: Request PIN
    C->>ATM: Enter PIN
    ATM->>B: Validate PIN
    B-->>ATM: PIN Valid/Invalid

    C->>ATM: Select Withdraw
    ATM->>C: Request Amount
    C->>ATM: Enter Amount
    ATM->>B: Withdraw Request(amount)
    B-->>ATM: Approve / Reject
    ATM->>C: Dispense Cash
    ATM->>C: Print Receipt
```

## Giải thích
- Customer: người thao tác trực tiếp.
- ATM: trung gian nhận yêu cầu và giao tiếp với hệ thống ngân hàng.
- Bank Server: xác thực và xử lý giao dịch.