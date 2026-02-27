# cursor-configs

Repositório centralizado de **Cursor Rules** para importação em projetos via GitHub (Remote).

## Como importar no Cursor

1. Abra **Cursor Settings** (`Cmd+Shift+J` no Mac, `Ctrl+Shift+J` no Windows/Linux)
2. Vá em **Rules** → **Project Rules**
3. Clique em **+ Add Rule** → **Remote Rule (Github)**
4. Cole a URL do repositório: `https://github.com/SEU_USUARIO/cursor-configs`
5. As rules serão sincronizadas automaticamente com o repositório remoto

> As rules importadas permanecem sincronizadas com o repositório de origem. Atualizações no remote são refletidas automaticamente no seu projeto.

## Rules disponíveis

| Rule | Descrição | Aplicação |
|------|-----------|-----------|
| **backend-architecture** | Clean code e estrutura de diretórios para backend | Sempre |
| **frontend-architecture** | Arquitetura, estrutura e implementação para frontend | Sempre |
| **coding-standards** | Padrões globais de código (frontend e backend) | Sempre |
| **pre-commit-checks** | Verificações obrigatórias antes de commit/push | Sempre |
| **commits** | Formato Conventional Commits para mensagens | Inteligente |

## Estrutura do repositório

```
cursor-configs/
├── .cursor/
│   └── rules/
│       ├── backend-architecture/
│       │   └── RULE.mdc
│       ├── frontend-architecture/
│       │   └── RULE.mdc
│       ├── coding-standards/
│       │   └── RULE.mdc
│       ├── pre-commit-checks/
│       │   └── RULE.mdc
│       └── commits/
│           └── RULE.mdc
└── README.md
```

## Formato das rules

Cada rule usa o formato Cursor com frontmatter YAML:

```markdown
---
description: "Descrição da rule"
alwaysApply: true | false
globs: ["**/*.ts"]  # opcional, para rules file-specific
---

# Conteúdo da rule...
```

## Adicionando Skills (opcional)

Para adicionar **Agent Skills** neste repositório, crie a estrutura:

```
.cursor/skills/
└── meu-skill/
    └── SKILL.md
```

Ou use `.agents/skills/` para compatibilidade com o padrão Agent Skills.

## Referências

- [Cursor Rules Documentation](https://cursor.com/docs/context/rules)
- [Agent Skills Documentation](https://cursor.com/docs/context/skills)
