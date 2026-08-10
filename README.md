# PAQathon-skills

Agent skills ([`SKILL.md`](https://agentskills.io) open format) para Claude Code, Codex e qualquer agente que suporte o padrão.

## Skills

| Skill | O que faz |
|---|---|
| [`me-grelha`](.claude/skills/me-grelha/SKILL.md) | Transforma uma ideia vaga em spec através de rodadas de perguntas. |

## Instalar

```bash
npx skills@1.5.10 add blockful/PAQathon-skills -s '*' -a claude-code -a codex -g -y
```

Instala tudo globalmente para Claude Code + Codex. Outro agente? Adicione (ex.: `-a cursor`), ou tire `-a`/`-y` para escolher interativamente.

> ⚠️ Não use `--all`: ele mira todos os agentes do registro (60+).

### Variações

```bash
npx skills@1.5.10 add blockful/PAQathon-skills             # escolhe interativamente
npx skills@1.5.10 add blockful/PAQathon-skills@me-grelha   # instala uma só
npx skills@1.5.10 add blockful/PAQathon-skills --list      # lista disponíveis
npx skills@1.5.10 list -g                                  # lista instaladas
```

Como marketplace de plugin do Claude Code:

```
/plugin marketplace add blockful/PAQathon-skills
```

## Atualizar

```bash
npx skills@1.5.10 update
```

## Adicionar uma skill

1. Crie `.claude/skills/<skill-name>/SKILL.md`. O nome da pasta **deve ser igual** ao `name` do frontmatter.
2. Frontmatter exige `name` e `description`. **Sempre aspas na description** — um `: ` solto quebra o YAML e a skill é ignorada silenciosamente.
3. Coloque as palavras-gatilho no começo da description (é o que faz o agente ativar a skill). Máx. 1024 chars.
4. Valide — o próprio instalador é o validador:
   ```bash
   npx skills@1.5.10 add ./.claude/skills/<skill-name> --list
   ```
   Precisa listar sua skill. `No valid skills found` = frontmatter quebrado.
5. Registre em `.claude-plugin/marketplace.json` (lista `skills`) e crie o symlink Codex:
   ```bash
   ln -s ../../.claude/skills/<skill-name> .agents/skills/<skill-name>
   ```
6. Abra um PR.

Material extra (templates, refs, exemplos) vai em subpastas ao lado do `SKILL.md` (`references/`, `assets/`, `scripts/`) — os agentes carregam sob demanda.

## Layout

- `.claude/skills/` — fonte da verdade de cada skill.
- `.claude-plugin/marketplace.json` — marketplace do Claude Code.
- `.agents/skills/` — symlinks no formato aberto, lido nativamente pelo Codex.
