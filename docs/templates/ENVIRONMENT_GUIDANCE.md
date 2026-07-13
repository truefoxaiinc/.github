# Environment-variable guidance

Commit `.env.example`, never `.env`.

Use safe placeholders and document each variable's purpose, whether it is required, its expected format and where production values are managed. Do not include passwords, tokens, private keys, database credentials, customer identifiers or real service endpoints.

Applications should fail closed when production secrets are missing and should validate configuration at startup.
