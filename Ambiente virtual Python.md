# Gerenciando Projetos Python com UV no VS Code

## Passo 1: Instalação

Abra o terminal do VS Code (`Ctrl + J`) e utilize o PowerShell para colar o comando de instalação do UV para Windows:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

> Após a instalação, feche e abra novamente o VS Code para que o terminal reconheça o novo comando.

---

## Passo 2: Inicializar o Projeto

Com a pasta do seu projeto aberta no VS Code, execute no terminal:

```powershell
uv init
```

Isso criará automaticamente arquivos essenciais como:
- `pyproject.toml` — ficha técnica do projeto
- `.python-version` — versão do Python utilizada
- `main.py` — arquivo de exemplo

---

## Passo 3: Criar o Ambiente Virtual (venv)

```powershell
uv venv
```

Isso criará uma pasta isolada chamada `.venv` contendo todas as dependências específicas desse projeto.

---

## Passo 4: Ativar o Ambiente Virtual

```powershell
.\.venv\Scripts\activate
```

> **Nota:** Se for a primeira vez e ocorrer um erro de permissão, altere a política de execução de scripts do Windows:
> ```powershell
> Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
> ```
> Em seguida, execute o comando de ativação novamente.

Você saberá que deu certo quando o nome do projeto aparecer entre parênteses no terminal, como `(nome-do-projeto)`.

---

## Passo 5: Adicionar Bibliotecas

```powershell
uv add nome_da_biblioteca
```

**Exemplo:**

```powershell
uv add pandas
```

O UV instalará a biblioteca e suas dependências rapidamente, registrando-as automaticamente no `pyproject.toml` e criando um arquivo `uv.lock` para garantir versões consistentes em qualquer computador.

---

## Passo 6: Executar o Código

Você pode rodar seu script de duas formas:

- Clicando no botão **▶ Play** do VS Code
- Ou pelo terminal:

```powershell
uv run nome_do_arquivo.py
```

---

## Passo 7: Remover Bibliotecas (Opcional)

```powershell
uv remove nome_da_biblioteca
```

---

## Passo 8: Desativar o Ambiente Virtual

```powershell
deactivate
```
