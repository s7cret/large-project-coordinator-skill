# Roles & Models

## Default role map (preferred)
- **Coordinator**: current session (main)
- **Architect**: xiaomi/mimo-v2-flash (fallback: deepseek-chat)
- **Coder**: qwen-portal/coder-model (fallback: deepseek-coder)
- **Reviewer/Refactor**: deepseek-coder (fallback: qwen-portal/coder-model)
- **Docs**: gpt-5-mini (fallback: qwen)
- **Research**: deepseek-chat (fallback: qwen)
- **Vision**: qwen-portal/vision-model (only when images are involved)

## Model availability check
1) Check available models (e.g., config or model status).
2) Propose role assignments + fallbacks.
3) Ask for explicit user approval before proceeding.

## User confirmation (mandatory)
Always summarize the final role map in 3–6 lines and ask for confirmation:
- "Подтверждаешь состав ролей?"
