Passo a passo para gerenciar seus projetos Python com o UV diretamente no VS Code:
Passo 1: Instalação Abra o terminal do VS Code (Ctrl + J) e utilize o PowerShell para colar o comando de instalação do UV para Windows
encontrado na documentação oficial:

powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

Após a instalação, feche e abra novamente o VS Code para que o terminal reconheça o novo comando.

Passo 2: Inicializar o Projeto Com a pasta do seu projeto aberta no VS Code, digite no terminal o comando uv init
Isso criará automaticamente arquivos essenciais como o pyproject.toml (ficha técnica do projeto), o .python-version e um arquivo main.py de exemplo
.
Passo 3: Criar o Ambiente Virtual (venv) No terminal, execute o comando uv venv
Isso criará uma pasta isolada chamada .venv que conterá todas as dependências específicas desse projeto
.
Passo 4: Ativar o Ambiente Virtual Para ativar o ambiente no terminal do VS Code (PowerShell), use o comando .\.venv\Scripts\activate
Nota: Se for a primeira vez e ocorrer um erro de permissão, você precisará alterar a política de execução de scripts do Windows.
Precisará rodar o Set-ExecutionPolicy -Scope CurrentUser RemoteSigned e depois o .\.venv\Scripts\activate novamente.
Você saberá que deu certo quando o nome do projeto aparecer entre parênteses no terminal
.
Passo 5: Adicionar Bibliotecas Para instalar pacotes (como o Pandas), use o comando uv add nome_da_biblioteca (Ex: uv add pandas)
O UV instalará a biblioteca e suas dependências rapidamente, registrando-as automaticamente no seu arquivo pyproject.toml e criando um arquivo uv.lock 
para garantir que as versões sejam as mesmas em qualquer computador
.
Passo 6: Executar o Código Você pode rodar seu script Python clicando no botão de "Play" do VS Code ou digitando no terminal o comando uv run nome_do_arquivo.py
.
Passo 7: Remover Bibliotecas (Opcional) Caso precise desinstalar algum pacote, basta usar o comando uv remove nome_da_biblioteca no terminal
.
Passo 8: Para desativar o ambiente, rode: deactivate
