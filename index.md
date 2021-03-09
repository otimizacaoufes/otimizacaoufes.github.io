---
layout: default
title: Acesso ao servidor
nav_order: 1
description: ""
permalink: /
---

<!--## ATENÇÃO: SERVIDOR INDISPONÍVEL NO MOMENTO. Não há previsão para o retorno. Motivo: problemas nas instalações físicas do datacenter.-->

# Acesso ao servidor

O grupo de otimização da UFES, campus São Mateus, disponha de um computador de bom desempenho para realização de pesquisas, o **“optimization_server”**. O equipamento está disponível a outros pesquisadores, bem como aos estudantes de iniciação científica que possuam relação com o grupo.

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

### Acesso sem digitar senha

É possível configurar o acesso à máquina pelo terminal sem a necessidade de digitar senha. Basta criar um par de chaves RSA público-privado e copiar o conteúdo da chave pública no servidor.

Na sua máquina, crie as chaves no diretório oculto `.ssh` (crie-o se não existir):
~~~
cd .ssh
ssh-keygen [PRESSIONE ENTER PARA TODAS AS PERGUNTAS]
~~~

Dois arquivos serão criados na sua máquina: `id_rsa` (chave privada) e `id_rsa.pub` (chave pública). Você então deverá copiar o conteúdo do arquivo `id_rsa.pub` para `.ssh/authorized_keys` no servidor. Uma maneira simples de fazer isso:
- Abra sua pasta pessoal remota no ambiente gráfico do GNU/Linux como descrito [neste link](/sftp/);
- Peça para exibir arquivos ocultos, e entre na pasta oculta `.ssh`. Caso não exista, crie-a;
- Crie o arquivo `authorized_keys` e cole todo o conteúdo de `id_rsa.pub` nele.
- Se tudo deu certo, os próximos *logins* pelo terminal não pedirão mais senha.

## Por favor, cite o apoio em suas pesquisas

Se utilizar o equipamento em sua pesquisa, considere citar o apoio da FAPES nos trabalhos publicados (mais informações ao logar-se):
- **FAPES 116/2019.**
