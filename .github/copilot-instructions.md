# Copilot Instructions for This Repository

These instructions apply to this workshop repository and are optimized for Terraform (`*.tf`) work.

Treat these as default preferences. If the user gives a direct request that conflicts with a preference, follow the user's request.

## Scope
- Apply these rules for Terraform files in this repo.
- Keep changes small and workshop-friendly unless explicitly asked for production hardening.

## Terraform Style
- Preserve the current file style: section comments above each resource and readable spacing between blocks.
- Keep resource names and Azure object names consistent with the existing `var.prefix` naming pattern.
- Prefer variable-driven values over hardcoded values when adding configurable settings.

## Azure/Terraform Conventions
- Keep Azure resource location sourced from `var.location` or the resource group location.
- Keep provider compatibility with the existing repo baseline (`azurerm` 2.x) unless the user explicitly requests an upgrade.
- For new resources, follow existing dependency patterns by referencing other resource attributes directly.

## Security and Secrets
- Never hardcode secrets or credentials in Terraform files.
- If a secret is needed, add it as an input variable and mark it as sensitive when appropriate.

## Assistant Output Expectations
- When generating or modifying Terraform, include a short rationale in plain language.
- Keep suggestions practical for a learning workshop and avoid introducing unrelated architectural changes.
- If a proposed change is potentially breaking, call it out explicitly and offer a safer alternative.
