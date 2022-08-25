# CURSO GIT/GITHUB  
### ![](https://i.postimg.cc/bYSxTTgj/screenshot-20.png) [](https://github.com/professorjosedeassis) Prof. José de Assis 



#### [GIT/GITHUB O QUE É?](https://www.youtube.com/watch?v=FF1f4bKYhoo&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=1)

        Git linguagem de vercionamento
        GitHub-GH Rede social de hospedagem e compartilhamento dos códigos
        Grafo de commits: é uma estrutura que contem objetos relacionados, 
        nesse caso, usando o commit para se interrelacionar. |

#### [INSTALAR E CONFIGURAR GIT NO WINDOWS](https://www.youtube.com/watch?v=SOxafinthys&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=2)

#### [INSTALAR E CONFIGURAR GIT NO LUNUX](https://www.youtube.com/watch?v=YKjPi7Td3ZQ&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=9)

#####           COMANDOS DO GUIT BASH

* git version 

>      saber versão do git

* git config --global user.name "<nomedousuarioGitHub>      " 

>      configurar o usuário github.

* git config --global user.email "<emaildousuarioGitHub>      " 

>      configurar o email github.

* git config user.name 

>      mostrar o nome.

* git config user.email 

>      mostrar o email.

* git config core.editor 

>      saber o caminho do editor que tá padrão.

* git config --global core.editor "caminho do app"

>      adicionar o aplicativo de edição de código.

>      OBS: criar uma "variável de ambiente" e indicar "code" como nome e
>      o caminho do app editor de código.



#### [COMANDOS BÁSICOS](https://www.youtube.com/watch?v=v8-4rI0cJXE&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=3)

* git init

>      cria pasta .git no diretório. dentro do .git que é a identificação 
>      .git é uma pasta que guarda os arquivos, tipo uma pasta de backup

* git status 

>      verifica se o arquivo está armazenado no contêiner(tracked "verde" ou 
>      untracked "vermelho"

* git add

>      adiciona os arquivos modificados dentro de um contêiner. usando "." 
>      ou  adiciona tudo

* git commit -m <comentário>      

>      identifica e armazena o contêniner, com os arquivos modificados 
>      dentro do contêiner, no repositório local .git.

* git log 

>      mostra a identificação do commit, autor e data local.

* git log --oneline

>      mostra a identificação do commit de uma forma mais reduzida, 7 dígitos
>      do Rash. O HEAD é que se rastreia os commits e recuperar uma versão 
>      anterior do projeto.

* code . 

>      abre o editor de códigos setado.

#### [RASTREANDO, DESFAZER E RECUPERAR VERSÕES ANTERIORES DO PROJETO](https://www.youtube.com/watch?v=_mB-TShMDvY&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=4)


        Master é o ramo principal. HEAD é ponto onde o seu projeto se encontra no Grafo de Commits, **sempre vai ser o último commit.**

* git log --graph
* git log --graph --all 
* git log --graph --oneline --all 

>             as três opções mostram o Grafo de Commit, o segundo mostra todos, e não apenas aquele em que estou. 
>             O terceiro a mesma coisa, apenas de forma reduzida 

* git commit -am <comentário>      

>       o comando acima, além de comitar ele, através do "a" do "-am" 
>      adiciona os arquivos, é o **git add**, só que mesclado em uma linha 
>      de comando. Ganha tempo.

        O git não gera novas cópias de projeto a cada novo commit, ele vai rastrear as alterçaões do projeto, só as alterações. 

* git branch

>      Identifica o ramo em que o projeto se encontra, mostra onde está o 
>      HEAD. Ao criar um repositório, será sempre criada uma branch Master

* git checkout <Rash>      

>      Rastrear as mudanças do commit,**Retorna para versão anterior** 
>      o HEAD deve ser apontado para o commit que se quer retornar a versão.
>      ao realizar o checkout, ao fazer a consulta _git log --online_ 
>      percebe-se que se está oculto o último commit.

* git checkout master

>      Entra na branch master.

* git diff 

>       ultima revisão e visualizar mudanças antes de fazer o commit. 
>      Mostra as alterações, o que foi removido e o que foi incluido verde.
>      Quando adiciona o conteudo no contâiner, o **git diff** não precisa 
>      mais ser usado, não vê nada. 

* git reset HEAD <file>      

>       remover o conteudo no contêniner

* git reset --hard <Rash>      

>       remover commit

#### [CRIAR RAMIFICAÇÃO NO PROJETO.](https://www.youtube.com/watch?v=iRs6sQOPcvg&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=5)

![Ramificação1](https://i.postimg.cc/DwNRPF9W/screenshot-2.png)

* git checkout -b <NomeDoNovoRamo>       

>      cria um novo ramo, **branch**. Todos os commits apartir da criação 
>      desse novo branch, serão realizadas nela.
>      Um ramo criado herda tudo da **master**, ficando dois ramos, "com mesmo conteúdo".
![Ramificação2](https://i.postimg.cc/nLy4kwVY/screenshot-3.png)

        O HEAD aponto para as duas ramificações, teste, master. 

* git checkout master

>      retornando a ramificação master após commits.

![Ramificação3](https://i.postimg.cc/gcXyxhdb/screenshot-4.png)


* git merge <NomeDoRamoParaFundirAoRamoMaster>      

>      fundir dois branchs para tornar uma versão estável. Havendo conflito deve ser resolvido.

![antes do merge](https://i.postimg.cc/xC1MRkWY/screenshot-5.png)

![Git coloca dentro dos arquivos avisos](https://i.postimg.cc/xT3mW3nY/screenshot-6.png)

![após o merge](https://i.postimg.cc/85bD1c5F/screenshot-7.png)



#### [CRIAR REPOSITÓRIO REMOTO NO GITHUB E CLONAR NA MÁQUINA LOCAL.](https://www.youtube.com/watch?v=j2exng2k3z4&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=6)

* git remote
* git remote -v 

>      verifica se há algum repositório remoto na máquina local. O segundo mostra detalhes do link remoto

* git remote add origin <LinkRepositórioGitHub> 

>       linka o repositório online com o local

* git push 
* git push -u origin master

>       Empurra(sincroniza) os arquivos do pc local para o servidor do GitHub.
>       
>       O 1º sem cerimônia, empurra o conteúdo.
>       O 2º , mais completo, especifica o nome do repositório e o branch, em que os arquivos farão parte. 
> 
>       Significados:
>       -u, de upstream;
>       origin, que é o nome do repositório remoto;
>       master, que é o ramo principal do projeto.


#### [RESOLVENDO PROBLEMAS DE AUTENTICAÇÃO(ERRO 403) E TOKENS.](https://www.youtube.com/watch?v=j_Z4PopPt_o&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=7)

        Ao dar o **push** pode ocorrer o seguinte erro
 
 ![ErroGitPush1](https://i.postimg.cc/RhLD6pJG/screenshot-8.png) 

>       Esse erro pode ocorrer devido a duas situações. Uma, tendo dois repositórios no GH só ter a credencial de uma no Windows.
>       A outra é relacionada a segurança.

* 1º passo : remover as credênciais ![removendo_credencial_windows](https://i.postimg.cc/bJcP1Mdj/screenshot-9.png)

>       Após realizar novamente o **git push** será solicitado novamente o TOKEN do GH.

* Criar TOKENS > Site do GH > Setings > Config do Desenvolvedor > Personal Acess Token > Marcar todas as caixas e clicar no botão "gerar TOKEN"

>       COPIE O CÓDIGO DO TOKEN EM LOCAL SEGURO, ELE NÃO APARECE MAIS


#### [CRIANDO REPOSITÓRIO NO GH E CLONANDO PARA O WINDOWS](https://www.youtube.com/watch?v=h1-XZ9Kh1H4&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=8)

* git clone <LinkRepositórioGitHub>

>       Traz o diretório para máquina local. Ele cria a pasta oculta .git que é o repositório local.  


#### [CRIAR E EDITAR ARQUIVOS E PASTAS DIRETO NO GH](https://www.youtube.com/watch?v=Xsulc8agj_A&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=10)

        Logado no GH, navegue até o diretório, e clique no arquivo. Após clique 
        aqui ![aqui](https://i.postimg.cc/1RHYsTGY/screenshot-10.png) para editar o código.

        Em "Preview Changes visualiza as alterações" ![PreviewChanges](https://i.postimg.cc/wBqVB5hc/screenshot-11.png) 
        Após precisa "commitar" ![](https://i.postimg.cc/jSzg2dBK/screenshot-12.png)

        Após alterações no site do GH é necessário atualizar o repositório local

* git pull 

>       sincroniza do site do GH, online, para o repositório da máquina local.


#### [TRABALHANDO EM UM PROJETO EM VÁRIOS REPOSITÓRIOS LOCAIS - RESOLVENDO CONFLITOS](https://www.youtube.com/watch?v=yNCBpSX9Yj4&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=11)

        Repositórios de exemplo, o da esquerda deu **push** e não obteve "problema".
        O da direita, ao enviar as alterações retornou "rejeitado", pois há conflitos entre os repositórios.

![Repositórios](https://i.postimg.cc/cCPC2z33/screenshot-13.png)


* git fetch 

>       realiza o download das alterações realizadas no repositório remoto, para ver o que foi modificado
>       e poder resolver os conflitos. Equivale ao **pull** porém não realiza o *merge*, a fusão dos projetos.

* git remote 

>       verifica qual o repositório remoto habilitado.

 
#### [FORK E PULL REQUEST](https://www.youtube.com/watch?v=l1rwvDvD1og&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=12)

        **FORK** clona um repositório/projeto de terceiro pro seu GH, alterando-o sem alterar o original.
        Poderá realizar um **pull request** para o dono do repositório será sinalizado para aceitar ou não as alterações. **pull request** contribui com a comunidade.

        Sinalização do **pull request** na conta de origem.

![sinalização_pullrequest_ProjetoOriginal](https://i.postimg.cc/bN8sXwzv/screenshot-16.png)


        Aceitando, MERGE, as alterações.

![Aceitar_pullrequest](https://i.postimg.cc/jSnVZyGn/screenshot-17.png)


#### [GITHUB COMO PORTIFÓLIO E CURRÍCULO](https://www.youtube.com/watch?v=fj3mPSVlEi0&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=13)

Muitas empresas usam o GH para contratação, ajudar e contribuir são até melhores que diplomas e cursos.
#####           DICAS DE ALTERAÇÃO DE PERFIL E REPOSITÓRIOS
                1. No campo <Location> colocar : Cidade,duasSiglasdoEstado,País; Ex: Goianésia do Pará,PA,Brazil
                
                2. Adicionar licença a seus repositórios, **MIT License**, algumas pessoas irão copiar seu repositório sem
                lhe indicar como criador. A licensa te garante ser o dono da idéia. 

                Pode adicionar a licença posterior a criação do repositório. 
                Vá até o repositório, **clique Creat nwe file**
                
                Figura a seguir mostra isso 
![criar_licença](https://i.postimg.cc/6qQHmN15/screenshot-18.png)

                no campo que surgiou, ao digitar LICENSE, sugirá o botão _Chosse a license template_ 
                
![botão_licença](https://i.postimg.cc/PqhQ7jCs/screenshot-19.png)

                Depois realiza o COMMIT.

                
                3. Pode usar emojis.

                
                4. Sempre adicione os tópicos, pois são palavras chaves para busca do GH. 


#### [EDITANDO O ARQUIVO README NO GH ](https://www.youtube.com/watch?v=T70t3mDiwvg&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=14)


        O Readme, é um dos principais arquivos, escrever documentar e exemplificar seu projeto. No GH é usado como cartão de visita. É usado a extensão .md.
        pode-se usar .gif
        Vídeos não rodam no README.

[Modelo Readme Projetos de softwares-Professor Assiss](https://gist.github.com/professorjosedeassis/d1c08e6667f43be18a1f25c40e1ac2de)

[MarkDown - Sintaxes - GitHub ](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[MarkDown comandos básicos](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown#open)

#### [SELOS DINÂMICOS DE METADADOS USANDO SHIELDS.IO](https://www.youtube.com/watch?v=hQb0I3M2BuQ&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=17)

        Para ter acesso primeiro deve-se acessar o link abaxo:
<https://shields.io/> 

Importante observar que os selos usam os dados dos usuários e dados externos.
Cada selo pede pra configurar algo, tipo nome do usuário, nome do repositório, Copy Badgue URL, MarkDown format.

[](https://i.postimg.cc/cJxFFb4J/screenshot-26.png)





#### [KANBAN - GERANCIANDO PROJETOS (ABA PROJECTS) FERRAMENTA NATIVA](https://www.youtube.com/watch?v=KmH1o6wCuDE&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=15)

        **KANBAN** É um sistema visual de gerenciamento de projetos. Significa cartão ou sinalização.
        Exemplo simplificado:

![KANBAN](https://i.postimg.cc/mgsKRhkt/screenshot-21.png)

        Pode ser utilizado dentro do repositório. **Projetcts**, clicando em **novo projeto**, **criar novo projeto**.
        Após criar as colunas, que serão os quadros, só clicar no sinal de mais do canto superior direito e adicionar os cartões.
        Dentro dos cartões podem ser usados o MarkDown.
![](https://i.postimg.cc/VLfmB797/screenshot-22.png) 

        - [ ] na linguagem MarkDown cria uma caixa de seleção. 

          - [ ] Exemplo.  Não deu certo.. :( nesse arquivo. --dois espaços cria subitens


#### [Abrindo uma issue e integrando com GitHub projects kanban](https://www.youtube.com/watch?v=ZzQYCt3M4_k&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=16)

        Issue, se pronuncia *ixu*, ela é um aviso ou solicitação, que se pode fazer, ao desenvolvedor de um projeto hospedado no GH.

![](https://i.postimg.cc/0Qzcsqqt/screenshot-23.png)

        Sempre verifique no repositório se não há uma **Issue** já criada e resilvida para o problema.

        No repositório que recebeu a **Issue** poderá se aplicado um rótulo, *labels*, para o **Issue** recebido.

![](https://i.postimg.cc/15B6JYk4/screenshot-24.png) 

        Após receber, lá na em Projetcts, poderá adicionar um card no KANBAN da **Issue** recebida.

![](https://i.postimg.cc/rscjtRrH/screenshot-25.png)


#### [CRIANDO UM PERFIL PROFISSIONAL NO GITHUB](https://www.youtube.com/watch?v=CjfbzZZfoqA&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=18)

Criar um repositório com o mesmo nome do perfil, obrigatóriamente, deve ser publico, e Add a README file.


Gera no perfil um local diferente. Para personalizar editando-os.

![](https://i.postimg.cc/fTXZsJ79/screenshot-27.png)

Link do gerador
[](https://rahuldkjain.github.io/gh-profile-readme-generator/)


#### [HOSPEDAR SITE GRATUITAMENTE NO GH](https://www.youtube.com/watch?v=28lkK072FCY&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=19) 

Tem um serviço chamado GitHub Pages, para hospedar vai em SETINGS, GitHubPages.


#### [HOSPEDAR SITE GRATUITAMENTE NO GH COM DOMÍNIO PERSONALIZADO E CERTIFICADO SSL (HTTPS)](https://www.youtube.com/watch?v=lCz_Snbqd1M&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=20)

Domínio próprio deve estar registrado no regisro.br

#### [INTEGRANDO O GITHUB COM A IDE ECLIPSE](https://www.youtube.com/watch?v=MdioIaiK9-Y&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=21)


















>       













