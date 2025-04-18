---
layout: default
title: Sobre
nav_order: 1
description: ""
permalink: /
---

<!--## ATENÇÃO: SERVIDOR INDISPONÍVEL NO MOMENTO. Não há previsão para o retorno. Motivo: problemas nas instalações físicas do datacenter.-->
<!--## ATENÇÃO: SERVIDOR INDISPONÍVEL NO MOMENTO. Previsão de retorno: 17/03. Motivo: problemas nas instalações físicas do datacenter.-->

# Sobre

O grupo de pesquisa ["Matemática Aplicada e Computacional"](http://dgp.cnpq.br/dgp/espelhogrupo/7657905567244335) da UFES, campus São Mateus, disponha de um computador de bom desempenho para realização de suas pesquisas, o **“optimization_server”**. O equipamento foi adquirido com recursos da Fundação de Amparo à Pesquisa e Inovação do Espírito Santo (processo FAPES 116/2019) via projeto de pesquisa submetido pelo grupo à edital universal.

Outros pesquisadores e seus estudantes de iniciação científica podem ter acesso ao recurso para realização de suas pesquisas.


### Acesso remoto

- Acesso externo à UFES:
~~~
ssh USUARIO@externo.ceunes.ufes.br -p 25000
~~~

- Acesso interno à UFES:
~~~
ssh USUARIO@172.20.110.9 -p 25000
~~~


### Configuração da máquina

- 1 processador Intel(R) Xeon(R) Silver 4114 CPU @ 2.20GHz 10 núcleos (20 threads), 160Gb RAM
- Sistema GNU/Linux Ubuntu Server


### Acesso sem digitar senha (GNU/Linux)

É possível configurar o acesso à máquina pelo terminal sem a necessidade de digitar senha. Basta criar um par de chaves RSA público-privado e copiar o conteúdo da chave pública no servidor.

Na sua máquina, crie as chaves no diretório oculto `.ssh` (crie-o se não existir):
~~~
cd .ssh
ssh-keygen [PRESSIONE ENTER PARA TODAS AS PERGUNTAS]
~~~

Dois arquivos serão criados na sua máquina: `id_rsa` (chave privada) e `id_rsa.pub` (chave pública). Você então deverá copiar o conteúdo do arquivo `id_rsa.pub` para `.ssh/authorized_keys` no servidor. Uma maneira simples de fazer isso:
- Abra sua pasta pessoal remota no ambiente gráfico do GNU/Linux como descrito [neste link](/sftp);
- Peça para exibir arquivos ocultos, e entre na pasta oculta `.ssh`. Caso não exista, crie-a;
- Abra/Crie o arquivo `authorized_keys` e cole todo o conteúdo de `id_rsa.pub` em uma nova linha.
- Se tudo deu certo, os próximos *logins* pelo terminal não pedirão senha.


### Acesso pelo Windows

Os usuários de Windows devem instalar um cliente ssh. No Windows 10, há um cliente disponível na lista de programas do sistema. Em outras versões é necessário instalar *softwares* de terceiros. É recomendável um terminal com mais funcionalidades do que o `cmd`. Por exemplo, Powershell (já presente no Windows 10) ou [cmder](https://cmder.net/).
