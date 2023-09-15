<h1>Configurando o VSCode para trabalhar com o Nest</h1>

Neste Guia, vamos apresentar algumas dicas, recomendações e soluções para os problemas mais comuns que acontecem com o Nest.

<h2>1. Instalar o Eslint</h2>

O **ESLint** é uma ferramenta para identificar e relatar padrões encontrados no código ECMAScript, JavaScript e TypeScript, sugerindo correções e indicando comandos em desuso (deprecated), para melhorar o seu código. 

1. Abra o **Terminal** do VSCode através do menu **Terminal 🡪 New Terminal**
2. Será aberta janela do **Power Shell** na parte inferior da janela do VSCode.
3. Para instalar o **ESLint**, digite o comando abaixo:

```bash
npm install eslint
```

4. Ao concluir a instalação será exibida a mensagem abaixo:

<div align="center"><img src="https://i.imgur.com/Qnd9tLX.png?1" title="source: imgur.com" /></div>

<br />

<h2>2. Configurações</h2>

<h3>2.1. Configurar o Powershel para executar Scripts</h3>

O Windows PowerShell, por padrão, restringe a execução de scripts. Como iremos executar diversos Scripts no NestJS, precisamos alterar as políticas de execução de scripts, seguindo os passos abaixo:

1. Na Caixa de pesquisas, localize o **Windows PowerShell** (Marcado em verde na imagem), e clique na opção  **Executar como Administrador**  (Marcado em amarelo na imagem).

<div align="center"><img src="https://i.imgur.com/24fgzVO.png" title="source: imgur.com" /></div>

2. Na janela do **Windows PowerShell**, digite o comando abaixo:

```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
```

<h3>2.2. Configurações Recomendadas no VSCode</h3>

Vamos alterar 2 configurações no VSCode para nos auxiliar no Desenvolvimento da aplicação como Nest:

1. Abra as **Configurações do VSCode** através do menu **File 🡪 Preferences 🡪 Settings** (Arquivo 🡪 Preferências 🡪 Configurações)

   <div align="center"><img src="https://i.imgur.com/HHV5tH8.png" title="source: imgur.com" /></div>

2. Será aberta janela do **Settings** (Configurações)

   <div align="center"><img src="https://i.imgur.com/FAIEW4J.png" title="source: imgur.com" /></div>

3. No item **Search Settings** (Procurar Configurações), digite: **Implicit Project Config: Experimental Decorators** e habilite esta configuração, conforme indicado na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/msdAykm.png" title="source: imgur.com" /></div>

4. O VSCode emite mensagens de alerta com alguns decorators do Nest, informando que são decorators em versões experimentais. Esta configuração desliga estas mensagens desnecessárias.
5. Ainda no item **Search Settings** (Procurar Configurações), digite: **Preferences: Import Module Specifier** e altere para **relative**, conforme indicado na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/PoHA6Tl.png" title="source: imgur.com" /></div>

6. Esta opção "força" o VSCode a toda vez que importar um pacote TypeScript ou do Nest utilizar o Caminho relativo ao invés do Caminho absoluto. Como o Jest (Framework de testes) não aceita o caminho absoluto, para não ter o trabalho de mudar todas Classes na Sessão de testes, já vamos deixar o VSCode configurado para sempre usar o caminho relativo.

**Exemplo:**

**Caminho Absoluto:** *src/bcrypt/bcrypt*

**Caminho Relativo:** *./bcrypt/bcrypt*

<h2>3. Erros Comuns no NPM</h2>

Este tópico são dicas para resolver problemas comuns do NPM.

<h3>3.1. Warning Global e Local Deprecated</h3>

Ao instalar novos pacotes através do NPM, pode aparecer a mensagem de alerta abaixo:

<div align="center"><img src="https://i.imgur.com/MjGVkrq.png?1" title="source: imgur.com" /></div>

Para desativar este alerta vamos alterar as configurações do NPM nos arquivos **npm.cmd** e **npm** na pasta de instalação do Node.

1. No **Windows Explorer**, abra a pasta **C:\Arquivos de Programas\nodejs** e localize os arquivos **npm.cmd** e **npm**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/RKK5kjp.png" title="source: imgur.com" /></div>

2. No Windows Explorer, clique com o botão direito do mouse sobre o arquivo **npm** e clique na opção **Abrir com**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/5TobEim.png" title="source: imgur.com" /></div>

3. Na janela **Como você deseja abrir este arquivo?**, clique na opção **Bloco de notas**.

<div align="center"><img src="https://i.imgur.com/a81cEyx.png" title="source: imgur.com" /></div>

4. Na **linha 23 do arquivo npm**, substitua `prefix -g` por `prefix --location=global`, como mostra a figura abaixo e salve o arquivo.

<div align="center"><img src="https://i.imgur.com/NaSjyK3.png" title="source: imgur.com" /></div>

5. Ainda no Windows Explorer, clique com o botão direito do mouse sobre o arquivo **npm.cmd** e clique na opção **Editar**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/WM86MBR.png" title="source: imgur.com" /></div>

6. Na **linha 12 do arquivo npm.cdm**, substitua `prefix -g` por `prefix --location=global`, como mostra a figura abaixo e salve o arquivo.

<div align="center"><img src="https://i.imgur.com/2wyxwdA.png" title="source: imgur.com" /></div>

7. A mensagem de alerta deve desaparecer.

<h3>3.2. Erro nos pacotes @nestjs</h3>

Mesmo com todas as Bibliotecas devidamente instaladas, pode acontecer de alguma delas não ser encontrada, em virtude de alguma atualização, por exemplo. Caso a mensagem abaixo seja exibida no terminal, independente da Biblioteca (no exemplo abaixo vemos o Swagger), podemos corrigir de uma forma simples, como veremos abaixo:

<div align="center"><img src="https://i.imgur.com/eV6wgJk.png?1" title="source: imgur.com" /></div>

1. Abra o **Terminal** do VSCode através do menu **Terminal 🡪 New Terminal**
2. Será aberta janela do **Power Shell** na parte inferior da janela do VSCode.
3. Digite o comando abaixo para atualizar todas as Bibliotecas do Nest:

```bash
nest update -f -t latest
```

4. Será exibida a mensagem abaixo:

<div align="center"><img src="https://i.imgur.com/BO1lUKf.png?1" title="source: imgur.com" /></div>

<br />

<h2>4. Extensões recomendadas para o VSCode</h2>

Na tabela abaixo temos algumas sugestões de Extensões do VSCode para auxiliar no processo de construção do aplicativo Nest:

| Exetensão                                                    | Descrição                                        |
| ------------------------------------------------------------ | ------------------------------------------------ |
| **[Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)** | Integra o Eslint ao VSCode.                      |
| **[Auto Import](https://marketplace.visualstudio.com/items?itemName=steoates.autoimport)** | Auxilia na importação das Classes e Pacotes.     |
| **[Prettier Code Formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)** | Formata o código.                                |
| **[Bracket Pair Colorization Toggler](https://marketplace.visualstudio.com/items?itemName=dzhavat.bracket-pair-toggler)** | Coloriza os Parênteses, as Chaves e os Colchetes |
| **[VSCode Icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)** | Ícones usados no VSCode neste Cookbook.          |


<br /><br />

<div align="left"><a href="README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
