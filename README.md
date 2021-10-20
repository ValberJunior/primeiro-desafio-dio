
# Primeiro Projeto Digital Innovation One<br>
<img src='https://hermes.digitalinnovation.one/site/images/cover_dio.jpg' width="500px">


<br><br>

 

# **GIT**      <img src='https://cdn.iconscout.com/icon/free/png-64/git-225996.png' width="50px">



- Criado por **Linus Torvalds**.
- Ferramenta **Open Source**.

 **GIT** é um sistema de controle de versões distribuído, usado  no desenvolvimento de software, mas tara registrar o histórico de edições de qualquer tipo de arquivo. **(Local , gerenciado principalmente por seu terminal chamado git bash)**

Podemos baixar o **Git** :point_right: <a href='https://git-scm.com/downloads'>Aqui</a>.


<br><br>


# **GIT**HUB   <img src='https://cdn.iconscout.com/icon/free/png-64/github-1521500-1288242.png' width="50px">

 

**GitHub** é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git. Ele permite que programadores, utilitários ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo... **( Servidor na nuvem que armazena códigos)**

Podemos criar nossa conta no **Github** :point_right:<a href='https://github.com/'>Aqui</a>



<br><br><br>



## Criando um repositório Local :computer:



Para criarmos um repositório em nossa máquina, precisamos criar uma pasta no diretório desejado, nesse caso podemos criar tanto pelo terminal quanto manualmente através do clique no botão direito do mouse e na seleção da opção "nova pasta".

Após isso, precisamos iniciar o **Git** dentro dessa pasta, então utilizaremos o **git bash** ( O terminal do Git), basta clicar no botão direito do mouse e ir na opção **git bash here**:point_left: , deste modo abrirá a janela de terminal do **git bash**.

![image-20211020140119549](C:\Users\Junior\AppData\Roaming\Typora\typora-user-images\image-20211020140119549.png)

No primeiro Acesso será necessário logar com o usuário do **Github** para posteriormente compartilhar o código na nuvem e para que seja ágil o processo de edição de outros códigos disponibilizados lá.

Normalmente usamos o seguinte comando:



_git config --global user.email "seu email cadastrado"_

_git config --global user.name "seu username"_



**Obs:** O comando "--global" indica que sua máquina estará logando no usuário informado (todos os diretórios presentes na sua máquina serão afetados por esse processo, por isso o termo global), para mais detalhes podemos dar uma olhada na documentação <a href='https://git-scm.com/docs'>aqui:file_folder:</a>.



Depois de logar no usuário, iniciaremos o nosso repositório com o comando :arrow_forward: **git init**  , o seguinte passo é renomear a **branch principal** para **main**, conforme na atualidade se tem por consenso, através do comando **Git branch -m "main"**.

**Obs**: branches são ramificações de um projeto, sendo que a principal é a parte do código validada. Para testar melhorias e updates em projetos, o aconselhável é criar uma nova branch e apenas após homologação do código modificado, fazer o update para a branch principal.

Conseguimos criar uma branch nova com o seguinte comando : 

_git branch **nome-da-branch**_



:point_right: **Resumo até aqui**

* Criar a Pasta :arrow_forward: Abrir o **git bash** dentro da pasta :arrow_forward: Logar com o usuário no terminal :arrow_forward: Iniciar o Git dentro da pasta com o comando **Git Init**.



Nesse estágio, você já pode criar seu projeto na sua pasta, a próxima etapa será enviar o projeto para a nuvem através do **GitHub**.



### Vinculando um repositório Local com um repositório na nuvem :cloud:



Nessa etapa iremos utilizar o **github** para subir os nossos projetos, é preciso ter uma conta no mesmo, e iniciar um **Novo Repositório**.



![image-20211020143532398](C:\Users\Junior\AppData\Roaming\Typora\typora-user-images\image-20211020143532398.png)



No próprio **GitHub** encontramos a dica para prosseguir, tanto para criar um repositório zerado quando para subir um projeto já pronto.

Para vincular um **repositório local** com o criado no **github** devemos digitar a seguinte linha de comando no nosso **git bash** ou mesmo dentro do **VS Code** , através do terminal.



:arrow_forward:  **git remote add origin endereço_do_github_referente_ao_seu_projeto**



**OBS:** Por convenção, utilizamos o termo **origin** para nos referirmos a branch principal.



Então, após vincularmos nosso repositório, precisamos subir os arquivos para ele...

Utilizamos os seguintes passos no nosso terminal:

- **git add ***(para adicionar todos os arquivos);

- **git status** (para verificar os arquivos selecionados);

- **git commit -m "mensagem detalhando o motivo da alteração"** (primordial, o commit é a confirmação de que os arquivos serão adicionados e o porque dessa alteração deve ser bem explicada).

  

Para finalizar, devemos confirmar que todas os arquivos serão adicionados através do comando **git push**:



:arrow_forward:  **git push -u origin main  endereço-do-github-referente-ao-seu-projeto**



**OBS: **_É bom notar que o "-u" só será utilizado quando subirmos o nosso projeto pela primeira vez, também devemos informar qual branch será atualizada e informar também o url do projeto no github_...





### Como editar um projeto que já existe:interrobang:



Podemos editar um projeto que já está no **github** que esteja no nosso perfil, através do **clone**. Para isso basta ir no repositório e copiar o link referente ao projeto, e após isso abrir o **git bash** no diretório local desejado, feito isso basta digitar o seguinte comando no terminal:



:arrow_forward: **git clone  url_do_projeto**



Então será criado uma pasta com todos os componentes do projeto para que localmente possam ser feitas melhorias e alterações no código.



:floppy_disk:  **Para Salvar mudanças em um projeto**



:point_right: Devemos ter a consciência de quantas pessoas estão mexendo no projeto, e o impacto da alteração que será implementada. Caso ainda não esteja homologada ou precise de autorização para ser incorporada ao código, o recomendado é criar uma branch nova e nela salvar as alterações efetuadas para posteriormente:



 Para a mudança ser enviada ao **Github** devemos antes fazer uma requisição para o url do projeto para que a última versão do mesmo seja sincronizada a nossa pasta local, ou seja, que tanto a versão da nuvem quanto a versão local sejam alinhadas. E fazemos através do seguinte comando:



:arrow_forward: **git pull**



Após receber a confirmação de que não houveram erros para sincronizar a versão do projeto, então podemos subir nossas mudanças através do seguinte comando:



:arrow_forward: **git push origin main**



![image-20211020153206350](C:\Users\Junior\AppData\Roaming\Typora\typora-user-images\image-20211020153206350.png)



###  Pull Request – Pedido de incorporação do seu código na árvore do código.



 Raramente fazemos **commits** (quando se tem mais de um programador) diretamente

No **branch principal**. Todas as alterações são feitas através do chamado **Pull Request**, e um

Responsável (**marge**) analisa as **pull request** e adiciona no **branch principal.**



:arrow_forward:  **Pull Request - Pedido de incorporação do seu código na árvore do código.**

 



### **Trabalho em equipe** :busts_in_silhouette:

 

 Não podemos trabalhar diretamente na **branch principal**, o correto é criar uma nova branch e selecionar a mesma:



:arrow_forward: **git branch branch-nova** 

:arrow_forward: **git checkout branch-nova**.

 

**OBS:** Devemos abrir o **Github** para criar o **Pull Request**. Esse **Pull Request** irá descrever as mudanças e deixar uma área para discussão, colocando um título e uma descrição mais detalhada possível.

 

#### **Como gerenciar conflitos de códigos**:interrobang:



É normal acontecer. O git consegue resolver grande parte dos conflitos, o que ele não

Conseguir, ele deixará **marcado para que seja fácil identificar**.

 

 

 

 

 
