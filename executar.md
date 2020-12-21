---
layout: default
title: Executar testes
nav_order: 1
description: ""
permalink: /executar
---

# Executando um programa depois de fechar a sessão ssh

Um ponto importante é como deixar um programa rodando mesmo depois de fechar a sessão ssh. Pois do contrário, qualquer problema na rede derruba a sessão ssh e fecha todos os programas que estão rodando nela. Uma opção é o comando **nohup**. Ele deve ser usado antes do 
comando que você quer rodar:

**nohup MEU_PROGRAMA &**

(não esqueça do & no fim). Isso executará o comando MEU_PROGRAMA em modo não iterativo e criará o arquivo **nohup.out**, que receberá 
a saída do seu programa. Você pode então fechar a sessão ssh que seu programa continuará rodando. Ao logar-se novamente, você poderá ver se ele 
já acabou, por exemplo, através do comando **htop**.
