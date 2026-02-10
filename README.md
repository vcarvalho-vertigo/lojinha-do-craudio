# lojinha-do-craudio

Marketplace de plugins para o [Claude Code](https://claude.ai/code). Projeto de estudo para explorar o sistema de plugins.

## Plugins disponíveis

| Plugin | Skill | Descrição |
|--------|-------|-----------|
| `craudio` | `/craudio:review-code` | Code review: bugs, segurança, performance e legibilidade |

## Como usar

```bash
# Adicionar o marketplace (de dentro do Claude Code)
/plugin marketplace add <caminho-ou-repo>

# Instalar um plugin
/plugin install craudio@lojinha-do-craudio

# Usar a skill de review
/craudio:review-code
```

## Teste local

```bash
# Validar a estrutura
claude plugin validate .

# Adicionar o marketplace localmente
/plugin marketplace add ./
```
