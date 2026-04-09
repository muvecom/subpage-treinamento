# Subpages Treinamento

Páginas HTML estáticas de treinamento da Muvecom. Cada unidade ou tema fica em uma pasta própria, com um `index.html` independente.

Repositório remoto: [github.com/muvecom/subpage-treinamento](https://github.com/muvecom/subpage-treinamento)

## Estrutura

| Pasta | Conteúdo |
|-------|----------|
| `Alpha/` | Página de treinamento Alpha |
| `BAS Auto/` | Página de treinamento BAS Auto |
| `Bailon Itanhaem/` | Página de treinamento Bailon Itanhaém |
| `Bailon Praia Grande/` | Página de treinamento Bailon Praia Grande |
| `Hannover/` | Página de treinamento Hannover |
| `JAC/` | Página de treinamento JAC |
| `MED Prevent/` | Página de treinamento MED Prevent |

Para visualizar localmente, abra o arquivo `index.html` desejado no navegador ou sirva a pasta com um servidor HTTP simples (por exemplo `python3 -m http.server` na raiz do projeto).

## Git e GitHub

Clone e remote HTTPS padrão:

```bash
git clone https://github.com/muvecom/subpage-treinamento.git
cd subpage-treinamento
```

### Onde usar o Personal Access Token (PAT)

**Não coloque o token em arquivo dentro deste repositório** (nem em `README`, `.env` commitado, scripts versionados ou URL do remote salva no Git com o token embutido). Isso expõe o segredo no histórico do Git e no GitHub.

Use o PAT apenas quando o Git **pedir senha** ao fazer `git push` ou `git pull` via HTTPS:

1. **Usuário:** seu nome de usuário do GitHub  
2. **Senha:** cole o **token** (não use a senha da conta)

Assim o token não fica no projeto; só trafega na autenticação.

### Salvar credenciais no computador (opcional)

Para não digitar o token a cada push, você pode usar o armazenamento de credenciais do Git **na sua máquina** (fora do repositório):

```bash
git config --global credential.helper store
```

Na próxima vez que o Git pedir usuário e senha, ele gravará em `~/.git-credentials` (permissões restritas). Revogue tokens antigos em [GitHub → Settings → Developer settings → Tokens](https://github.com/settings/tokens) se suspeitar de vazamento.

Outra opção é o cache temporário (memória, expira em minutos):

```bash
git config --global credential.helper 'cache --timeout=28800'
```

### Alternativa: SSH

Se preferir não usar PAT com HTTPS, configure uma [chave SSH no GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) e altere o remote:

```bash
git remote set-url origin git@github.com:muvecom/subpage-treinamento.git
```

## Publicar alterações

```bash
git add -A
git commit -m "Sua mensagem"
git push origin main
```

Se a política do repositório exigir, use merge request ou branch conforme as regras da organização.

## Licença / uso

Uso interno Muvecom, salvo acordo em contrário.
