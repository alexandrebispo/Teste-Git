Teste-Git
=========
Neste Projeto foram usados os principais comandos para uso do Git e GitHub, segue abaixo os comandos:

1 - apt-get git install

Configuração inicial de Git
  git config --global user.nome Alexandre Bispo
  git config --global user.email alexandrebispo.mestre@gmail.com
  
Instruções para colorir as interações:
  git config --global color.ui true
  
acassar a pasta que será seu repositório e inicializar o git
  git init
  
Os três passos para controlar as versões:
  1 - git add "arquivo / pasta"
  2 - git commit -m "Escreva texto de descrição do commit"
  3 - git log para verificar o commit efetuado
  
OBS: você pode adicionar todos os arquivos do repositorio, como o comando:
  git add .
  
Comados para analise de Log:
  git log -p
  git log -p -"número de commit de commits que deseja verificar, aparece os ultimos"
  git log --stat
  git log --pretty=online
  git log --pretty=format "%h - %an - %ar : %s
  
Você pode adicionar um arquivo txt com o nome de .gitignore e listar dentro dele os arquivos que deseja ignorar e adicionar este arquivo no controle de versão.
  
Remover arquivo adicionado:
  git reset HEAD 'ARQUIVO'
  
  
Voltando versão:
  git checkout 'HASH'
  
git reset HEAD~"NUMERO DE VERSOES QUE DESEJA VOLTAR"  --soft  REMOVE APENAS OOS COMMITS

git reset HEAD~"NUMERO DE VERSOES QUE DESEJA VOLTAR"  --hard  REMOVE OS COMMITS e OS ARQUIVOS

BRANCHES

Adicionado um novo branch:

git checkout -b NOME DO BRANCH

Verificando o branch que que estou:
  git branch
  
OBS: É sugerido que se crie um branch apenas quando for criar uma funcionalidade nova, ou que fça sentido ter um galho.

Como mesclar duas versões:
  git merge NOME DO BRANCH
  
  No brach atual será mesclado com o branch informado no comando.
  
No caso de não ser necessário gerar um comando para mesclar os branches basta usar o REBASE, ele irá organizar e adicionar ao log todos os commits efetuados no projeto na ordem.
  git rebase nome do branch

como remover um branch:
  git branch -D NOME DO BRANCH
  
GitHub
======

Como criar uma chave de autenticação:
  ssh-keygen

Verificando se chave foi criada:
  cd ˜/.ssh/
  
Acessar o arquivo com editor de texto, id_rsa.pub

Cadastra a chave do arquivo na conta do github

Aplicando o primeiro push:
  1 - git remote origin URL(criado quando fizemos o repositorio no site do github)
  2 - git push origin nomedobranchlocal
  
  
Clone:
Para copiar um projeto para um repositorio local basta aplicar o comando abaixo:
  git clone URL
  
  Além disso pode dar um espaço apos a url e adicionar o nome do diretorio:
  
    git clone URL nomedodiretorio
    
Você pode verificar todos os repositorios criados locais e remotos com o comando abaixo:
  git branch -a
  
PUSH e PULL

Para verificar e pegar todas as alterações feitas no repositorio remoto:
  git pull repositorio_remoto local

    
    
