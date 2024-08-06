<h1>Deploy do Backend no Render - Github Organization</h1>



Quando estamos trabalhando com Organizações, além de conectar o Render com a Conta do Github é necessário autorizar o acesso do Render na Organização, para poder acessar os repositórios.
Neste material, o Passo 10 foi adaptado para o Deploy do Projeto Integrador via Github Organization. Substitua o Passo 10 do Guia do Deploy do Projeto Blog Pessoal pelas instruções abaixo. Os demais passos são iguais.

Antes de iniciar o processo do Deploy, verifique os pontos de atenção abaixo:

- Antes de atualizar o Repositório da sua aplicação no Github, verifique a compatibilidade dos tipos de dados do MySQL, que foram definidos nos decoradores **@Column** de cada atributo das Classes Entidade (Model) da sua aplicação, com os tipos de dados equivalentes, utilizados no Banco de dados PostgreSQL, através da tabela abaixo. Caso algum tipo seja diferente, ajuste o tipo de dado no decorador **@Column** do atributo, na respectiva Classe Entidade (Model).

**Tabela de Compatibilidade de tipos de dados - MySQL - PostgreSQL**

| **MySQL**                            | **PostgreSQL**                |
| ------------------------------------ | ----------------------------- |
| BIGINT                               | BIGINT                        |
| BINARY(n)                            | BYTEA                         |
| BIT                                  | BOOLEAN                       |
| CHAR(n), CHARACTER(n)                | CHAR(n), CHARACTER(n)         |
| DATE                                 | DATE                          |
| DATETIME                             | TIMESTAMP [WITHOUT TIME ZONE] |
| DECIMAL(p,s), DEC(p,s)               | DECIMAL(p,s), DEC(p,s)        |
| DOUBLE                               | DOUBLE PRECISION              |
| FLOAT                                | REAL                          |
| INT, INTEGER                         | INT, INTEGER                  |
| MEDIUMINT                            | INTEGER                       |
| NUMERIC(p,s)                         | NUMERIC(p,s)                  |
| SMALLINT                             | SMALLINT                      |
| TINYBLOB, BLOB, MEDIUMBLOB, LONGBLOB | BYTEA                         |
| TINYINT                              | SMALLINT                      |
| TINYTEXT, TEXT, MEDIUMTEXT, LONGTEXT | TEXT                          |
| TIME                                 | TIME [WITHOUT TIME ZONE]      |
| TIMESTAMP                            | TIMESTAMP [WITHOUT TIME ZONE] |
| VARBINARY(n), VARBINARY(max)         | BYTEA                         |
| VARCHAR(n)                           | VARCHAR(n)                    |
| VARCHAR(max)                         | TEXT                          |

- Observe que a maioria dos tipos são iguais, entretanto, existem alguns que são diferentes e podem causar erro durante o processo do Deploy no Render.
- Caso o seu grupo tenha algum problema para configurar um atributo do tipo Date/Time (problema muito comum), consulte o artigo: [Easy Guide to TypeORM Dates, Time, TimeStamp, and Timezone](https://thriveread.com/typeorm-date-and-timestamp/) (em Inglês).
- No **Passo 03 - Criar uma conta grátis no Render**, crie uma nova conta no Render utilizando a conta do Github que foi criada para o Projeto Integrador do seu grupo;

<br />

<h2>👣 Passo 09 - Criar o Web Service no Render a partir de uma Organização</h2> 



1. Na barra de menus principal do Render, clique no item Dashboard, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/AYQts2Z.png" title="source: imgur.com" /></div>

2. Para adicionar um novo Web Service, no Dashboard do Render, clique no botão **New +** e em seguida clique na opção **Web Service**.

<div align="center"><img src="https://i.imgur.com/FVGlwLN.png" title="source: imgur.com" /></div>

3. No item **GitHub**, clique no link **+ Connect account**, para conectar a sua conta do Render com a sua Conta do Github.

<div align="center"><img src="https://i.imgur.com/xaffIQz.png" title="source: imgur.com" /></div>

4. Na tela, **Install Render**, clique na **Organização** que foi criada na conta do Github do Projeto Integrador (no exemplo abaixo, **Projeto-Integrador-Modelo**), como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/F1Da8Nv.png" title="source: imgur.com" /></div>

5. Na próxima tela, clique no botão **Install**, para concordar que o Render acesse a Organização no Github.

<div align="center"><img src="https://i.imgur.com/OWUK5N8.png" title="source: imgur.com" /></div>

6. Conecte o Render com o Repositório onde você enviou o **Backend do Projeto Integrador**, clicando no botão **Connect**, localizado ao lado do Repositório.

<div align="center"><img src="https://i.imgur.com/hzNpT9m.png" title="source: imgur.com" /></div>

7. Na próxima tela, informe o nome da sua aplicação na propriedade **Name** (nome do seu projeto integrador) e verifique se a propriedade **Environment** está com a opção **Node** selecionada.

<div align="center"><img src="https://i.imgur.com/JxQQutS.png" title="source: imgur.com" /></div>

<br />

| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="120px"/> | <p align="justify"> **ATENÇÃO:** O NOME DO PROJETO NÃO PODE CONTER LETRAS MAIUSCULAS, NUMEROS OU CARACTERES ESPECIAIS. </p> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

8. Role a tela para baixo e verifique se o Plano Gratuito (**Free**) está selecionado.

<div align="center"><img src="https://i.imgur.com/GenKLYn.png" title="source: imgur.com" /></div>

<br />

> [!IMPORTANT]
>
> **Caso seja selecionado um plano diferente, o Render exigirá o Cartão de Crédito para emitir a fatura do serviço.**

<br /><br />
	

<div align="left"><a href="https://github.com/conteudoGeneration/cookbook_javascript/blob/main/04_nest/README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
