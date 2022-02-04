# Curso de Git e GitHub
Anotações do curso de "Git e Github Essencial" da Geek University (Udemy).

### O que é Git?
É um sitema de controle de versão código distribuido. Criado por Linus Torvalds em 2005.  
Tem o objetivo de responder as perguntas que são necessárias no desenvolvimento de software, são elas:
  - O que mudou?
  - Quando mudou?
  - Por que mudou?
  - Quem fez a mudança?
  - Podemos reproduzir esta mudança?

### O que é um sistema de controle de versão de código?
É um sitema que monitora e gerência as altereções de arquivos, garantindo a consistência nas alterações.

### O que o Git resolve?
Ao trabalhar em uma equipe com vários desenvolvedores as alterações de código são feitas em paralelo. Para que isto ocorra o git realiza o “merge" entre as alterações
de forma que ao final tenha-se um arquivo único com todas as alterações.

### Como o Git funciona?
Por ser um sistema de gerenciamento de controle de versão de código/documentos, o git possui
recursos avançados de monitoramento e acompanhamento de arquivos que fazem parte de um projeto.
Ou seja, após ativo em um projeto, o git começa a monitorar as mudanças ocorridas neste projeto e nos
mostra através de um poderoso sistema de estágios (ou fases) em que estágio ou fase se encontram os
arquivos.

### Quais são os 4 estágios do ciclo de vida de status para os arquivos no git?
 - Untracked:  
   São arquivos não rastreados pelo monitoramento do git. 
   __Importante:__ Enquanto não houver o monitoramento do arquivo o git não estará
   controlando o versionamento do mesmo.
   
 - Tracked:  
   Quando adicionamos arquivos ao monitoramento do git, o status deste arquivo
   passa a ser ‘tracked’, ou seja, rastreado.
   A partir de então o git passa a controlar as mudanças neste arquivo e todo o
   poder deste controlador de versão distribuído passa a fazer parte do seu projeto.
   Os arquivos com status ‘tracked’ são conhecidos como novos arquivos.
   
 - Modified:  
   Quando modificamos um arquivo que está sendo rastreado, seu status passa a
   ser ‘modified’, ou seja, ‘modificado’.
   Desta forma sabemos facilmente se um arquivo não está sendo rastreado, ou
   está sendo rastreado ou mesmo se está sendo rastreado, mas ocorreram modificações.
   OBS: É nesta etapa que podem ocorrer conflitos, pois imaginando que você e
   outra pessoa baixaram uma cópia do mesmo arquivo e ambos o modificaram, de
   alguma forma o arquivo deve ser juntado ao final para gerar apenas um atualizado.
   
 - Staged:  
   Quando um arquivo está pronto, ou seja, ele está sendo rastreado e já foi
   motificado e finalizado, então está pronto para ser enviado para o repositório.
   Então o status passa a ser ‘staged’, que seria algo como ‘preparado’.
   Os arquivos no estágio ‘staged’ são enviados para o repositório através de
   commits.
   
### Principais comandos
 ```
 - git help (Nome do comando)
 - git init // Inicia o monitoramento do git em um diretório.
 - git add (Nome do arquivo) // Altera o status do arquivo de "Untracked" ou "Modified" para "Tracked".
 - git commit -m "Digitar descrição da alterção realizada" // Altera o status de "Tracked" para "Staged".
 - git checkout (Id do Commit) // Retorna os arquivos do projeto para o estado do commit mencionado no comando.
 - git checkout main //Retorna para o último commit realizado
```
### Comandos Auxiliares
 ```
 - git status
 - git add . // Adiciona todos os arquivos do diretório raiz.
 - git log --oneline // Exibe o histórico de commits em apenas uma linha.
 - git mv (nome do arquivo atual) (nome do arquivo alterado) //Este comando realiza a alteração do nome do arquivo via git.  
     A vantagem é que esta alteração é realizada e já fica no estado de stage, podendo ser realizado um commit logo após a alteração.
 - git rm (Nome do arquivo) // Deletar um arquivo via git.
 - git diff --staged // Exibe as alterações realizadas no código (Utilizado antes de realizar o commit).
 - git diff (Id do commit) // Exibe as diferenças entre o commit atual e o mencionado no comando.
 - git diff (Id do commit anterior)..(Id do commit posterior) // Utilizado para exiber as diferenças entre dois commits. 
 - git commit --amend -m "Texto" // Realiza alterações no último commit, caso haja necessidade.
```

### Arquivo Git Ignore
Este arquivo faz com que o git ignore todos arquivos ou extensões mencionados. Exemplos:
```
db.sqlite3 // Ignora pelo nome do arquivo.
**__pycache__ // Ignora pelo nome do diretório. 
*sqlite3 // Ignora pelo nome da extensão.
```

### Como verificar se está identificado e se identificar em um repositório Git?
```
git config --list // Lista as configurações do Git
git config user.name "Digite seu nome" // Registra seu nome nas configurações
git config user.email "Digite seu e-mail" // Registra seu e-mail nas configurações

Para que não seja necessário se identificar em todos os repositórios, podemos realizar uma configuração global:

git config --global user.name "Digite seu nome" // Registra seu nome nas configurações Globais
git config --global user.email "Digite seu e-mail" // Registra seu e-mail nas configurações Globais
```

### Git Log
```
- git log --oneline // Exibe o histórico de commits em apenas uma linha.
- git log // Exibe o histórico de commits.
       (/ Para pesquisar um commit pela descrição)
       (b Para voltar a listagem de commits antes da pesquisa)
       (q Para sair)
       - git config core.page cat // Altera o comportamento do Log para exibir todos os commits e encerrar o comando.
       - git config core.page less // Volta para a configuração anterior
 - git log -2 // Exibe apenas os últimos dois commits.
 - git log --oneline -2 // Exibe apenas os últimos dois commits em apenas uma linha.
 - git log --before="aaaa-mm-dd" // Pesquisa commits por data anterior a mencionada.
 - git log --after="aaaa-mm-dd" // Pesquisa commits por data anterior a mencionada.
 - git log --since="2 days ago" // Pesquisa commits de dois dias atrás.
 - git log --after="1 week ago" // Pesquisa commits de após uma semana para trás, ou seja última semana.
 - git log --author="Nome do autor" // Pesquisa commits pelo nome do autor.
```
