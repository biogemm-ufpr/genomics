---
title: Detecção de assinaturas de mutação de ponto induzida por repetição (repeat-induced point mutation)
description: Softwares utilizados: The RIPper
tags: - fungos
- The RIPper
- elementos transponíveis
---

<div align="justify">
Texto inicial em breve!
</div>

## Detecção de assinaturas de mutação de ponto induzida por repetição (repeat-induced point mutation)

<div align="justify">
Para a detecção de mutações de ponto induzidas por repetição podemos utilizar um arquivo FASTA contendo o genoma completo. Para esta análise, utilizaremos a ferramenta The RIPper em sua versão <a href="https://theripper.hawk.rocks/#/home">online</a>. Na aba <i>"Background"</i> podemos encontrar informações gerais sobre a ferramenta e também breves orientações de uso em inglês. Para realizar a análise utilizaremos a aba <i>"Files"</i>:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_01.png" alt="Visão geral da página inicial do The RIPper" align="center">
</center>
<br><br>
Em seguida, na seção <i>"Create a New File"</i>, clique no botão <i>"Escolher arquivos"</i> para selecionar um arquivo de genoma no formato FASTA em seu computador, e faça upload clicando no botão <i>"Upload File"</i>. Nesse tutorial, utilizaremos o genoma da linhagem CBS 120486 de <i>Phyllosticta citriasiana</i>:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_02.png" alt="Upload de genoma de interesse no software The RIPper" align="center">
</center>
<br><br>
Após escolha do arquivo, a ferramenta apresentará um desenho de DNA e a mensagem <i>"Uploading File"</i>. Quando o envio for concluído, o The RIPper apresentará os dados referentes ao genoma enviado na seção <i>"Files"</i>. Em <i>"File Name"</i> é possível observar o nome do arquivo (nesse caso, "PCitriasiana_CBS120486.fasta). Em <i>"Sequence Count"</i>, a ferramenta indica o número de contigs/scaffolds presentes no arquivo FASTA, que nesse caso eram 133. Já em <i>"Options"</i>, podemos realizar diferentes análises.
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_03.png" alt="Informações de arquivo e opções de análise no software The RIPper" align="center">
</center>
<br><br>
</div>

### RIP Sequence

<div align="justify">
Na opção <i>"RIP sequence"</i> podemos avaliar as assinaturas de RIP separadamente para cada contig ou scaffold. Para cada contig/scaffold, a ferramenta informa o comprimento (Length) e conteúdo GC em porcentagem (GC Content), e fornece as opções de calcular as assinaturas de RIP ou LRAR. Primeiro avaliaremos as assinaturas de RIP, usando a sequência do scaffold_1 como exemplo:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_04.png" alt="Opção RIP sequence utilizada no scaffold_1 de montagem de genoma de Phyllosticta citriasiana CBS 120486 no software The RIPper" align="center">
</center>
<br><br>

Em seguida, faça o upload do arquivo de sequências de aminoácidos das proteínas da linhagem CBS 120486 de <i>Phyllosticta citriasiana</i> utilizando a opção <i>"Upload Data"</i>.
</div>