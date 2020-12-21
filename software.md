---
layout: default
title: Softwares instalados
nav_order: 1
description: ""
permalink: /software
---

# Software instalado e disponível para uso

Os seguintes programas/pacotes estão instalados no servidor e disponíveis para uso:

- compiladores GNU Fortran, C, C++; python 3.

- bibliotecas LAPACK e (Open)BLAS (liblapack-dev e libopenblas-dev)

- **AMPL**  
Para usar o AMPL com licenca completa, volte o
terminal no tempo executando  
> faketime '2020-06-01' bash -l  
Isso 'abrira' um bash com data em que a licenca eh
valida.  
O ambiente do AMPL pode ser acessado pelo comando  
> ampl

- Biblioteca 'amplsolver.a' pré-compilada em
> /opt/amplsolver/amplsolver.a

- IBM CPLEX 12.10 em  
> /opt/ibm/ILOG/CPLEX_Studio1210  
O comando 'cplex' abre o ambiente CPLEX 12.10.

* IBM CPLEX 12.9 em  
> /opt/ibm/ILOG/CPLEX_Studio129

- Intel MKL 2020 (Intel Math Kernel Library) em  
> /opt/intel/mkl

- Octave com varios pacotes. Caso precise de algum pacote nao instalado, contatar **leonardo.secchin@ufes.br**
- Julia  
Entre no Julia executando  
> julia  
Julia esta disponível para todos os usuarios. Nao é permitido a usuarios instalar pacotes dentro do Julia. Para tanto, contatar **leonardo.secchin@ufes.br**.  
É possivel fazer sua própria instalação do Julia em seu diretório pessoal. Porém isso ocupara grande parte da sua cota de disco. Portanto recomenda-se utilizar a instalação global e solicitar a instalação dos pacotes que precisa. Além disso, ao instalar um pacote no Julia pré-instalado, ele fica disponível a todos os usuários.


## Instalação de novos pacotes

Caso necessite instalar algum pacote, contatar **leonardo.secchin@ufes.br.**
