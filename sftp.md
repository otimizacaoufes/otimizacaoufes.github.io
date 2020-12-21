---
layout: default
title: Transferência de arquivos
nav_order: 1
description: ""
permalink: /sftp
---

# Transferências de arquivos pelo ambiante gráfico do linux

Além da transferência via terminal com o comando **sftp**, você pode abrir sua pasta remota no gerenciador de arquivos do linux em modo gráfico. Os passos são os seguintes:

- Abra o gerenciador de Arquivos (nautilus) do seu Ubuntu (deve funcionar para outras distribuições Linux)
- Clique em “Outros locais”
- Na barra “Conectar ao servidor”, digite **sftp://USUARIO@ENDERECO:25000/home/USUARIO** onde ENDERECO varia se o acesso é interno ou externo à UFES.
- Clique em “Conectar”

### Observações importantes:

- Quando terminar de transferir seus arquivos, DESMONTE a pasta remota clicando na seta no menu lateral;
- A transferência de muitos arquivos em modo gráfico é lenta. Se for transferir muitos arquivos, considere compactá-los e transferir um único arquivo.
Depois descompacte-o VIA TERMINAL DIRETO NA PASTA REMOTA utilizando comandos como tar ou gzip/gunzip (execute **compactar** para ajuda).
**Evite o utilitário de descompactação do modo gráfico do seu linux direto na pasta remota, é muito lento.**
