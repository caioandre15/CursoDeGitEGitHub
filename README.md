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
 - git init // Inicia o monitoramento do git em um diretório.
 - git add (Nome do arquivo) // Altera o status do arquivo de "Untracked" ou "Modified" para "Tracked".
 - git commit -m "Digitar descrição da alterção realizada" // Altera o status de "Tracked" para "Staged".
 
### Comandos Auxiliares
 - git status

### Arquivo Git Ignore
Este arquivo faz com que o git ignore todos arquivos mencionados. Exemplos:
```
db.sqlite3 // Nome do arquivo
**__pycache__ // Nome da pasta do arquivo 
```








