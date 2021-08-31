---
layout: default
title: Usando Jupyter
nav_order: 7
description: ""
permalink: /jupyter
---

# Usando Jupyter

Jupyter é um ambiente gráfico para programação em Python, Julia e outras linguagens, que funciona no navegador de internet. É possível abrir o Jupyter em seu navegador local conectado ao servidor, e assim executar códigos no servidor atavés o seu navegador. Para tanto, siga os passos:

1. Acesse o servidor redirecionando uma porta ssh para sua máquina (localhost). Por exemplo, o comando abaixo redireciona a porta 8892:
~~~
ssh -L 8892:localhost:8892 USUARIO@ENDERECO -p 25000
~~~
onde ENDERECO varia se o acesso é interno ou externo à UFES ([veja detalhes](/)). Note que o acesso à sua conta é feito normalmente adicionando as diretivas para redirecionamento da porta. Não confunda a porta ssh 8892 (que você pode escolher) com a porta 25000 de acesso ao servidor.


1. **No servidor** execute `jupyter-notebook` apontando para a porta ssh escolhida e sem abrir o navegador web:
~~~
jupyter-notebook --no-browser --port 8892
~~~
Você pode executar o `jupyter-lab`, que é um ambiente mais completo:
~~~
jupyter-lab --no-browser --port 8892
~~~

   **Observação:** você não precisa instalar o Jupyter em sua máquina.


1. Ao executar o Jupyter no servidor, aparecerá na tela uma URL começando com `http://localhost:8892/` seguida de um código. Copie este *link* e cole no navegador da sua máquina. Se tudo funcionou, Jupyter será executado em seu navegador.

   **ATENÇÃO:** Para que o Jupyter fique ativo em seu navegador, a conexão com o servidor deve ser mantida. Portanto, não feche o terminal ou deslogue da sua conta. Se o acesso for interrompido, seu Jupyter parará de funcionar e um novo acesso deverá ser feito.


1. O Jupyter do servidor vem com os *kernels* para Python 3 e Julia.

<!--1. O Jupyter vem com o *kernel* do Python 3 por padrão. **Se você quer usar o Julia no Jupyter**, você precisará copiar o *kernel* do Julia para sua pasta pessoal. Para tanto, execute **no servidor** os seguintes comandos em sequência:
~~~
rm -rdf ~/.local/share/jupyter/
mkdir -p ~/.local/share/jupyter
ln -s /opt/julia_jupyter_kernels/kernels/ ~/.local/share/jupyter
~~~
Isso (re)criará um *link* para o diretório contendo as configurações de todos os *kernels* presentes no servidor. Após isso, (re)execute o Jupyter e verifique que Julia aparece nas opções.

   **ATENÇÃO:** o procedimento acima deve ser feito uma única vez, ou sempre que você verifique não possuir todos os *kernels* atualizados em seu Jupyter.-->
