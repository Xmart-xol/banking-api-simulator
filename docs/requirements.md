# Functional Requirements

## Authentication

- Users must be able to register.
- Users must be able to log in.
- JWT tokens must be issued upon successful authentication.
- Passwords must be securely hashed and stored.
- Only authenticated users can access protected endpoints.

## Accounts

- Users can view all accounts associated with their profile.
- Users can view account balances.
- Each account must have a unique account number.
- An account must belong to a single customer.

## Transfers

- Users can transfer funds between accounts.
- Transfers cannot exceed the available balance.
- Transfers cannot be negative.
- Transfers cannot be made to the same account.
- Successful transfers must update both account balances.
- Every transfer must generate a transaction record.

## Transactions

- Users can view transaction history.
- Transaction history must include:
  - Date
  - Amount
  - Source Account
  - Destination Account
  - Transaction Type

## Audit Logging

- All transfers must be audited.
- Login attempts must be recorded.
- Failed authentication attempts must be recorded.
- Audit logs must include:
  - User
  - Action
  - Timestamp

# Non-Functional Requirements

## Security

- Passwords must be hashed.
- JWT authentication must be implemented.
- Sensitive endpoints must require authorization.

## Performance

- API responses should complete within reasonable response times.
- Database queries should be optimized.

## Reliability

- Transfers must be processed atomically.
- Partial transfers must not occur.

## Maintainability

- The solution must follow Clean Architecture principles.
- Business logic must be separated from infrastructure concerns.

## Observability

- Application events and errors must be logged.