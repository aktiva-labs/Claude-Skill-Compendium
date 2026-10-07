# Claude-Skill-Compendium

Repositorio de skills de terceros, versionadas aquí para usarlas en sesiones de Claude en la nube (sin depender de instalar plugins en cada sesión).

Cada carpeta de primer nivel es **una fuente upstream**, reducida a lo que usa el agente: las skills (`SKILL.md` + sus archivos de apoyo) y la `LICENSE`. Sin READMEs, tests, CI ni manifiestos de plugin. Las skills viven en `skills/*/SKILL.md` (o en `SKILL.md` en la raíz si la fuente es una sola skill).

## Estructura por categoría

### Eficiencia
| Carpeta | Skills | Para qué |
|---|---|---|
| [`ponytail/`](ponytail) | `ponytail`, `-audit`, `-review`, `-debt`, `-gain`, `-help` | Solución más corta que funciona; auditar sobre-ingeniería. |

### Código y desarrollo
| Carpeta | Skills | Para qué |
|---|---|---|
| [`addyosmani-agent-skills/`](addyosmani-agent-skills) | 25 skills de ciclo de vida: `spec-driven-development`, `planning-and-task-breakdown`, `incremental-implementation`, `test-driven-development`, `debugging-and-error-recovery`, `code-review-and-quality`, `code-simplification`, `api-and-interface-design`, `git-workflow-and-versioning`, `ci-cd-and-automation`, `shipping-and-launch`, `documentation-and-adrs`, `deprecation-and-migration`, `performance-optimization`, `observability-and-instrumentation`, `context-engineering`, `idea-refine`, `interview-me`, `doubt-driven-development`, `constraint-driven-development`, `source-driven-development`, `using-agent-skills`, … | Flujo de ingeniería de punta a punta. |
| [`fastapi/`](fastapi) | `fastapi` | Convenciones de FastAPI/Pydantic (solo la skill del repo oficial, no el framework). |
| [`supabase-postgres-best-practices/`](supabase-postgres-best-practices) | `supabase-postgres-best-practices` | Buenas prácticas de Postgres (solo esa skill del repo de Supabase). |

### Auditoría y seguridad
| Carpeta | Skills | Para qué |
|---|---|---|
| [`security-audit-skill/`](security-audit-skill) | `security-audit` | Revisión de vulnerabilidades y pen-test de código (Cloudflare). |
| `addyosmani-agent-skills/` | `security-and-hardening`, `code-review-and-quality` | Hardening OWASP y revisión previa al merge. |

### Frontend y diseño
| Carpeta | Skills | Para qué |
|---|---|---|
| [`emilkowalski-skills/`](emilkowalski-skills) | `emil-design-eng`, `animate`, `animate-expo`, `review-animations`, `improve-animations`, `find-animation-opportunities`, `animation-vocabulary`, `apple-design`, `break-ui`, `mobile-native`, `pick-ui-library`, `prototype`, `ask-sonner`, `write-swift` | Pulido de UI, animación, móvil nativo. |
| `addyosmani-agent-skills/` | `frontend-ui-engineering` | UI accesible y responsive. |

### Pruebas y navegador
| Carpeta | Skills | Para qué |
|---|---|---|
| [`playwright-cli/`](playwright-cli) | `playwright-cli` | Automatizar navegador y pruebas con Playwright. |
| `addyosmani-agent-skills/` | `browser-testing-with-devtools` | Pruebas en navegador real vía Chrome DevTools MCP. |

## Fuentes

| Carpeta | Origen |
|---|---|
| `ponytail` | https://github.com/dietrichgebert/ponytail |
| `security-audit-skill` | https://github.com/cloudflare/security-audit-skill |
| `playwright-cli` | https://github.com/microsoft/playwright-cli |
| `emilkowalski-skills` | https://github.com/emilkowalski/skills |
| `supabase-postgres-best-practices` | https://github.com/supabase/agent-skills (`skills/supabase-postgres-best-practices`) |
| `addyosmani-agent-skills` | https://github.com/addyosmani/agent-skills |
| `fastapi` | https://github.com/fastapi/fastapi (`fastapi/.agents/skills/fastapi`) |

## Actualizar

Volver a clonar la fuente (`git clone --depth 1`) y reemplazar la carpeta correspondiente, dejando solo las skills y la licencia (en `addyosmani-agent-skills/` también `references/`, que las skills enlazan). Cada carpeta conserva la licencia de su origen.
