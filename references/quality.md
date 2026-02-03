# Quality Gates, Testing, Docker

## Quality gates (minimum)
- Lint/format (language‑appropriate)
- Unit tests (critical paths)
- Review checklist before merge

## Testing
- Define smoke tests
- Add integration tests where possible
- Record test commands in `docs/` or `reports/`

## Docker (if possible)
- Provide Dockerfile + docker-compose
- Include env template and run instructions
- Add a minimal healthcheck endpoint or command
