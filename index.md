<!-- ## ATENÇÃO: SERVIDOR INDISPONÍVEL NO MOMENTO. Não há previsão para o retorno. -->

**O grupo de otimização da UFES, campus São Mateus, disponha de um computador de bom desempenho para realização de pesquisas, o “optimization_server”. O equipamento está disponível a outros pesquisadores, bem como aos estudantes de iniciação científica que possuam relação com o grupo.**

### Acesso ao “optimization_server”

- Acesso externo à UFES: ssh USUARIO@externo.ceunes.ufes.br -p 25000
- Acesso interno à UFES: ssh USUARIO@172.20.110.9 -p 25000

### Máquina

- 1 processador Intel(R) Xeon(R) Silver 4114 CPU @ 2.20GHz 10 núcleos (20 threads), 160Gb RAM
- Sistema GNU Linux Ubuntu

### Comandos básicos via terminal

- Mudar a senha do usuário: **passwd**
- Ver processos em andamento: **htop**
- Ver últimas reinicializações do servidor: **caiu**
- Ver lista dos softwares instalados: **softwares**
- Ajuda para comandos de compactação/descompactação: **compactar**

### Transferências de arquivos pelo ambiante gráfico do linux, ou “como abrir sua pasta remota no gerenciador de arquivos do linux em modo gráfico”

- Abra o gerenciador de Arquivos (nautilus) do seu Ubuntu (deve funcionar para outras distribuições Linux)
- Clique em “Outros locais”
- Na barra “Conectar ao servidor”, digite **sftp://USUARIO@ENDERECO:25000/home/USUARIO** onde ENDERECO varia se o acesso é interno ou externo à UFES.
- Clique em “Conectar”

### Observações importantes:

- Quando terminar de transferir seus arquivos, DESMONTE a pasta remota clicando na seta no menu lateral;
- A transferência de muitos arquivos em modo gráfico é lenta. Se for transferir muitos arquivos, considere compactá-los e transferir um único arquivo.
Depois descompacte-o VIA TERMINAL DIRETO NA PASTA REMOTA utilizando comandos como tar ou gzip/gunzip (execute **compactar** para ajuda).
**Evite o utilitário de descompactação do modo gráfico do seu linux direto na pasta remota, é muito lento.**

### Executando um programa depois de fechar a sessão ssh

Um ponto importante é como deixar um programa rodando mesmo depois de fechar a sessão ssh. Pois do contrário, qualquer problema na rede derruba a sessão ssh e fecha todos os programas que estão rodando nela. Uma opção é o comando **nohup**. Ele deve ser usado antes do 
comando que você quer rodar:

**nohup MEU_PROGRAMA &**

(não esqueça do & no fim). Isso executará o comando MEU_PROGRAMA em modo não iterativo e criará o arquivo **nohup.out**, que receberá 
a saída do seu programa. Você pode então fechar a sessão ssh que seu programa continuará rodando. Ao logar-se novamente, você poderá ver se ele 
já acabou, por exemplo, através do comando **htop**.

#### Alguns comandos úteis do htop

Dentro do **htop**,
- **c**: seleciona um ou mais processos e seus processos filhos
- **k -> enter**: encerra os processos selecionados
- **U** (maiúsculo): deseleciona processos
- **t**: exibe processos em árvore
- **u** (minúsculo): filtra processos de um usuário específico a partir de uma lista
- **q**: sai do htop
- **h**: exibe ajuda

> **O grupo de otimização, que integra e coordena o projeto, analisará a abertura de novas contas.**

> **Este recurso é de uso prioritário para pesquisas do grupo que integra o projeto que originou o recurso. 
Porém outros grupos/pesquisadores podem utilizá-lo a depender da disponibilidade da máquina.**

> **Se utilizar o equipamento em sua pesquisa, considere citar o apoio da FAPES nos trabalhos publicados (mais informações ao logar-se):**
- **FAPES 116/2019.**

> **Caso necessite instalar algum pacote, comunicar a leonardo.secchin@ufes.br.**
