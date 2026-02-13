# Hello from Agent IAM!

This file was created by an AI agent that never had access to your GitHub credentials.

The vault decrypted credentials, executed code, and created this PR - all without exposing secrets to the agent.

## How It Works

1. **Agent submits code** - JavaScript as a string
2. **Vault decrypts token** - HKDF per-user key derivation
3. **Worker Loader loads code** - Dynamic module loading
4. **Code executes isolated** - Credentials in env, never returned
5. **Results returned** - Only GitHub API responses
6. **Credentials destroyed** - No persistence outside vault

## Security Model

- ✅ Envelope encryption (Root KEK → HKDF → AES-GCM)
- ✅ Per-user isolation (1 Durable Object per user)
- ✅ Dynamic code execution (Worker Loaders)
- ✅ Credentials never leave vault
- ✅ Full audit trail
- ✅ RBAC enforcement

This is the correct implementation of centralized IAM for AI agents.