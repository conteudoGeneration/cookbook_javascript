<h1>Criando uma Organização no Github</h1>



As organizações são contas compartilhadas onde empresas e projetos de  código aberto podem colaborar em muitos projetos de uma vez. Os  proprietários e administradores podem gerenciar o acesso de integrantes  aos dados e projetos da organização com recursos avançados  administrativos e de segurança.

Com a Organização, o Administrador consegue criar vários repositórios em um único lugar e conceder acessos específicos para cada membro ou time. Como um integrante da organização, você pode visitar o painel da sua  organização durante todo o dia para se manter atualizado sobre as atividades recentes e acompanhar problemas e pull requests nos quais está trabalhando ou seguindo na organização.

No projeto Integrador, a Organização será composta por diversos Repositórios, seguindo o padrão de nomes abaixo:

<table border="1" width="100%">
	<tr>
		<td><b>Repositório</b></td>
		<td><b>Conteúdo</b></td>
	</tr>
	<tr>
		<td><b>documentacao</b></td>
		<td>Arquivos contendo as documentações das 3 API's: <br />
		- Escopo do Projeto atualizado<br />
        - Documentação do Banco de Dados (DER, SQL e Dicionário de dados)<br />
		- Documentação do Backend (Documentação das Classes e PDF do Swagger)<br />
		- Documentação do Frontend
		</td>
	</tr>
	<tr>
		<td><b>nome_do_projeto-backend</b></td>
		<td>Projeto Nest completo</td>
	</tr>
	<tr>
		<td><b>nome_do_projeto-frontend</b></td>
		<td>Projeto React Completo</td>
	</tr>
</table>

Cada projeto Nest e React deverão ter o seu próprio repositório. A Documentação de todos os projetos serão mantidas no repositório documentação.

<br />

<h2>👣 Passo 01 - Preparação do ambiente</h2>



1. Crie uma conta de e-mail gratuita com o nome do grupo (grupo_NN-turma-javascript_NN).

2. Crie uma conta gratuita no Github utilizando o e-mail criado com o nome do projeto.

*NN é o número do grupo e da turma*

<br />

<h2>👣 Passo 02 - Criando a Organização e adicionando os Membros</h2>



Neste passo, vamos criar uma organização dentro da conta do Github que o Grupo criou.

1. Na Barra de Navegação superior da Conta do Github, clique no botão **+** e no menu que será aberto, clique na opção **New organization**.

<div align="center"><img src="https://i.imgur.com/5dopqz8.png" title="source: imgur.com" /></div>

2. Na próxima tela, role para baixo e clique no botão **Create a free organization**.

<div align="center"><img src="https://i.imgur.com/EboZUR7.png?1" title="source: imgur.com" /></div>

3. Na próxima tela, configure com os dados do seu projeto.

<div align="center"><img src="https://i.imgur.com/x3t6pR7.png" title="source: imgur.com" /></div>

| Item                             | Dados                        |
| -------------------------------- | ---------------------------- |
| **Organization account name**    | Grupo NN Turma JavaScript NN |
| **Contact e-mail**               | E-mail do seu grupo          |
| **This organization belongs to** | My personal account          |

*NN é o número do grupo e da turma*

4. Ao final, faça a verificação de segurança da sua conta clicando no botão **Verificar**, marque a opção de concordância com os **Termos de Uso do Serviço** (marcado em vermelho) e clique no botão **Next**.

<div align="center"><img src="https://i.imgur.com/DAACOex.png" title="source: imgur.com" /></div>

5. Na próxima tela, adicione todos os membros do seu grupo na Organização, através da conta do Github de cada integrante. Ao final clique no botão **Complete setup**.

<div align="center"><img src="https://i.imgur.com/mgE2E6t.png" title="source: imgur.com" /></div>

6. Os integrantes do grupo irão receber um **e-mail com o convite** para fazer parte da Organização, semelhante a figura abaixo:

<div align="center"><img src="https://i.imgur.com/TSmIDAO.png" title="source: imgur.com" /></div>

7. Clique no botão **Join** para aceitar o convite. 
8. Após clicar no botão **Join**, o Github solicitará a senha do Github pessoal para confirmar a aceitação do convite.

<br />

<h2>👣 Passo 03 - Criando Repositórios na Organização</h2>



Neste passo vamos criar os nossos Repositórios Remotos.

1. Na tela inicial da Organização, clique no link **Repositories**.

<div align="center"><img src="https://i.imgur.com/mmS2tld.png" title="source: imgur.com" /></div>

2. Na sequência, clique no botão **New repository**.

<div align="center"><img src="https://i.imgur.com/lD82tjh.png" title="source: imgur.com" /></div>

3. Na próxima tela, crie um **Repositório Público**, chamado **nome_do_projeto-backend** e em seguida clique no botão **Create Repository**.

<div align="center"><img src="https://i.imgur.com/9w8YSYN.png" title="source: imgur.com" /></div>

4. Repositório Criado!

<div align="center"><img src="https://i.imgur.com/AHCz83P.png" title="source: imgur.com" /></div>

5. Para criar os demais Repositórios no futuro, siga os mesmos passos.

<br />

<h2>👣 Passo 04 - Criando um Time de Desenvolvimento</h2>



Time de Desenvolvimento ou Teams,  são grupos de membros da organização que refletem a estrutura de sua empresa ou grupo de um Projeto, com permissões e menções de acesso em cascata aos repositórios da Organização.

Os proprietários da organização e os mantenedores da equipe podem conceder às equipes acesso de administração, leitura ou gravação aos repositórios da organização. Os membros da organização podem enviar uma notificação para uma equipe inteira mencionando o nome da equipe. Os membros da organização também podem enviar uma notificação para uma equipe inteira solicitando uma revisão dessa equipe. Os membros da organização podem solicitar revisões de equipes específicas com acesso de leitura ao repositório onde a solicitação pull é aberta.

Neste passo vamos criar um time de desenvolvimento.

1. Na tela inicial da Organização, clique no link **Teams**.

<div align="center"><img src="https://i.imgur.com/v0zK9q8.png" title="source: imgur.com" /></div>

2. Na sequência, clique no botão **New team**.

<div align="center"><img src="https://i.imgur.com/koXOidc.png" title="source: imgur.com" /></div>

3. Configure conforme a imagem abaixo e clique no botão **Create team**. Se o Grupo desejar, pode alterar o nome do Time.

<div align="center"><img src="https://i.imgur.com/XXfEaEj.png" title="source: imgur.com" width="80%"/></div>

3. Na página inicial do Time, clique no botão **Add a member** para adicionar os integrantes do Grupo no Time.

<div align="center"><img src="https://i.imgur.com/8nCyrjD.png" title="source: imgur.com" /></div>

4. Na próxima tela, localize os integrantes do grupo e clique no botão **Invite**.

<div align="center"><img src="https://i.imgur.com/4YQJSk4.png" title="source: imgur.com" /></div>

<br />

<h2>👣 Passo 05 - Adicionando o Time no Repositório</h2>



Neste passo, vamos adicionar o time no Repositório do Projeto.

1. Na tela inicial da Organização, clique no link **Repositories** e na sequência clique no repositório que você deseja adicionar o grupo.

<div align="center"><img src="https://i.imgur.com/mmS2tld.png" title="source: imgur.com" /></div>

2. Na tela inicial do Repositório (no exemplo abaixo, **rh-backend**), clique no link **Settings**.

<div align="center"><img src="https://i.imgur.com/7Yt1fAQ.png" title="source: imgur.com" /></div>

3. Na próxima tela, no menu lateral do lado esquerdo da tela, clique na opção **Collaborators & teams**.

<div align="center"><img src="https://i.imgur.com/ovPFtJI.png" title="source: imgur.com" /></div>

4. Ainda nesta tela, clique no botão **Add teams**.

<div align="center"><img src="https://i.imgur.com/gVxbRlI.png" title="source: imgur.com" /></div>

5. Na próxima tela, localize e selecione o **Time**. Na opção **Choose role**, vamos deixar com **Admin**. Desta forma, todos os Integrantes do Grupo terão acesso total ao Repositório.

<div align="center"><img src="https://i.imgur.com/WOATswx.png" title="source: imgur.com" /></div>

5. Clique no botão **Add** (botão verde), para concluir.
6. Repita estes passos nos demais repositórios do projeto.

| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="150px"/> | <div align="left"> **ATENÇÃO:** Como todos os Integrantes do Grupo terão acesso de Administrador do Repositório, tenham cuidado para manter o repositório organizado e sem erros.</div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

<h2>👣 Passo 06 - Personalizando a Organização</h2>



1. Clique sobre logo da Organização

<div align="center"><img src="https://i.imgur.com/d4yDd2i.png" title="source: imgur.com" /></div>

2. Na janela General, para alterar ou inserir o logo do projeto, clique no botão **Upload new picture**, na sessão **Profile picture** e selecione o novo logo.

<div align="center"><img src="https://i.imgur.com/N9kFUHU.png" title="source: imgur.com" /></div>

3. Ainda nesta janela, personalize as informações da Organização, ajustando os dados para o seu grupo.

<div align="center">
    <img src="https://i.imgur.com/RN32XZb.png" title="source: imgur.com" />
	<img src="https://i.imgur.com/bKoPFap.png" title="source: imgur.com" width="96%"/>
</div>



| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="100px"/> | <div align="left"> **ATENÇÃO:** O item **URL**, **deverá ser preenchido apenas no final do Bloco 03**, quando o Frontend do projeto que será apresentado no Evento de Empregabilidade estiver concluído e na nuvem.</div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

4. Clique no botão **Update Profile** para concluir.

<br /><br />
	

<div align="left"><a href="https://github.com/conteudoGeneration/cookbook_javascript/blob/main/04_nest/README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
