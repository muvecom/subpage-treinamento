# Subpages Treinamento

Repositório com páginas HTML estáticas de treinamento da Muvecom.
Cada unidade/tema fica em sua própria pasta, com um `index.html` independente.

Repositório remoto: [github.com/muvecom/subpage-treinamento](https://github.com/muvecom/subpage-treinamento)

## Estrutura atual

| Pasta | Conteúdo |
|-------|----------|
| `Alpha/` | Página de treinamento Alpha |
| `BAS Auto/` | Página de treinamento BAS Auto |
| `Bailon Itanhaem/` | Página de treinamento Bailon Itanhaém |
| `Bailon Praia Grande/` | Página de treinamento Bailon Praia Grande |
| `Hannover/` | Página de treinamento Hannover |
| `JAC/` | Página de treinamento JAC |
| `MED Prevent/` | Página de treinamento MED Prevent |
| `Zeekr/` | Página de treinamento Zeekr |

## Como visualizar localmente

### Opção 1: abrir direto no navegador

Abra o arquivo `index.html` da pasta desejada.

### Opção 2: subir servidor local (recomendado)

Na raiz do projeto:

```bash
python3 -m http.server 8000
```

Depois acesse no navegador:

- `http://localhost:8000/Alpha/`
- `http://localhost:8000/BAS%20Auto/`
- `http://localhost:8000/Zeekr/`

## Fluxo básico de atualização

```bash
git add -A
git commit -m "Atualiza página de treinamento X"
git push origin main
```

Se a política do repositório exigir, use branch/PR conforme as regras da organização.

## GitHub e autenticação (PAT/SSH)

### Clone via HTTPS

```bash
git clone https://github.com/muvecom/subpage-treinamento.git
cd subpage-treinamento
```

### Uso correto do Personal Access Token (PAT)

**Nunca** coloque token em arquivos do repositório (`README`, scripts, `.env` versionado ou URL remota com token embutido).

Use o token somente quando o Git solicitar credenciais em operações HTTPS (`git pull`/`git push`):

1. **Usuário:** seu usuário GitHub
2. **Senha:** cole o **PAT** (não a senha da conta)

### Armazenar credenciais localmente (opcional)

Persistente em arquivo local da máquina:

```bash
git config --global credential.helper store
```

Temporário em memória (8h):

```bash
git config --global credential.helper "cache --timeout=28800"
```

### Alternativa com SSH

Configure uma [chave SSH no GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) e troque o remote:

```bash
git remote set-url origin git@github.com:muvecom/subpage-treinamento.git
```

## Licença / uso

Uso interno Muvecom, salvo acordo em contrário.
