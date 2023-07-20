

## Exercícios de Mistura de Git e GitHub - Nível Fácil, Médio e Difícil


### Nível Fácil:

1.  Crie um novo repositório Git local, adicione alguns arquivos e faça o push para o GitHub.

```bash
# Crie um novo repositório local
git init

# Adicione alguns arquivos
touch arquivo1.txt arquivo2.txt

# Adicione os arquivos ao índice
git add arquivo1.txt arquivo2.txt

# Faça o commit das mudanças
git commit -m "Adicionar arquivo1.txt e arquivo2.txt"

# Conecte o repositório local ao repositório remoto no GitHub
git remote add origin URL-do-repositorio-no-github

# Faça o push dos commits para o GitHub
git push -u origin main

```

2.  Clone o repositório de outro colaborador, faça algumas mudanças e crie um Pull Request para enviar suas alterações.

```bash
# Clone o repositório do colaborador
git clone URL-do-repositorio-do-colaborador

# Faça algumas mudanças nos arquivos
# ...

# Adicione, confirme e envie as mudanças para o GitHub
git add .
git commit -m "Minhas mudanças"
git push origin nome-do-branch

# Vá para a página do repositório no GitHub e clique em "Compare & pull request"
# Siga as instruções para criar o Pull Request

```

3.  Adicione uma descrição detalhada ao README.md do seu repositório e atualize-o no GitHub.

```bash
# Adicione o arquivo ao índice
git add README.md

# Faça o commit das mudanças
git commit -m "Atualizar README.md com descrição detalhada"

# Envie as mudanças para o GitHub
git push origin main

```

### Nível Médio:

1.  Crie um novo branch, faça algumas alterações e envie para o GitHub, mas não confirme (commit) as mudanças. Depois, crie um Pull Request a partir desse branch.

```bash
# Crie um novo branch chamado "minhas-alteracoes"
git checkout -b minhas-alteracoes

# Faça algumas alterações nos arquivos
# ...

# Verifique o status para ver as mudanças não confirmadas
git status

# Adicione as mudanças ao índice
git add .

# Não faça o commit agora

# Envie o branch para o GitHub
git push origin minhas-alteracoes

# Vá para a página do repositório no GitHub e clique em "Compare & pull request"
# Siga as instruções para criar o Pull Request
```

### Nível Difícil:

1.  Crie um script Git Hook que execute testes automatizados antes de permitir que um commit seja confirmado.

```bash
# Crie um arquivo chamado "pre-commit" no diretório ".git/hooks/" do seu repositório local e adicione o seguinte conteúdo:
#!/bin/sh

# Execute seus testes automatizados aqui
# Se os testes falharem, o commit será cancelado

# Exemplo (assumindo que você tenha algum script de testes chamado "run_tests.sh"):
./run_tests.sh || exit 1

```

Lembre-se de tornar o arquivo "pre-commit" executável usando o seguinte comando:

```bash
chmod +x .git/hooks/pre-commit
```

Agora, sempre que você tentar fazer um commit, os testes automatizados serão executados e o commit será cancelado se os testes falharem.




</br>
2.  Crie uma estratégia de branching mais avançada para um projeto que envolva múltiplas funcionalidades e versões de lançamento.

Uma estratégia de branching comum envolve o uso de três tipos principais de branches:
main: Representa o estado de produção do projeto. Cada commit nessa branch corresponde a uma versão estável e lançada.

develop: Representa o desenvolvimento ativo do projeto. Os novos recursos são desenvolvidos e testados aqui antes de serem mesclados na main.

feature branches: Cada nova funcionalidade é desenvolvida em um branch separado. Quando concluído, o branch é mesclado de volta na develop.

Além disso, você pode criar branches adicionais para suporte de hotfixes (correção de bugs urgentes), releases (versões específicas) e versionamento (por exemplo, branches para versões 1.x, 2.x etc.).

A estratégia exata pode variar de acordo com as necessidades do projeto, mas essa abordagem é geralmente eficaz para projetos com múltiplas funcionalidades e lançamentos.






