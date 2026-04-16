---
title: Detecção de assinaturas de mutação de ponto induzida por repetição (repeat-induced point mutation)
description: > Softwares utilizados: The RIPper
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

### RIP Genome

<div align="justify">
Na opção <i>"RIP genome"</i> podemos avaliar as assinaturas de RIP de forma conjunta para o genoma inteiro. Ao clicar nesse botão, a ferramenta irá rodar a análise (o que pode levar um tempo considerável a depender do tamanho de genoma avaliado), e ao concluir, irá redirecionar para aa página de resultados. Na seção "RIP analysis" é possível configurar os parâmetros da análise. Caso qualquer parâmetro seja modificado, é necessário clicar em "Update" para atualizar a análise:
<br><br>
<ol>
<li><b>Window Size: </b>tamanho da janela a ser utilizada, em pares de bases</li>
<li><b>Slide size: </b>tamanho da janela deslizante a ser utilizada, em pares de bases</li>
<li><b>Minimum Composite: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Change em GC content: </b>avaliação de mudanças no conteúdo GC<br>
<li><b>Minimum Product: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Maximum Product: </b>valor máximo do índice Substrate a ser considerado</li>
</li>
</ol>
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_04.png" alt="Parâmetros da seção RIP Analysis no software The RIPper" align="center">
</center>
<br><br>
No bloco abaixo da seção "RIP Analysis" é possível avaliar as assinaturas de RIP separadamente para cada contig ou scaffold. Na opção "Select a Sequence" é possível escolher o contig/scaffold de interesse, e definir o intervalo a ser avaliado em "Start and End Range", e clicar em "Update Range". Ao selecionar o intervalo, a ferramenta atualizará o gráfico dos indíces Product, Substrate e Composite apresentado a seguir. No exemplo indicado abaixo, vemos uma região de 20000 pares de bases no scaffold 1 em que o trecho próximo à coordenada de 7000 pares de basess apresenta um valor de Product maior que 1,1, Substrate menor que 0,75 e Composite maior que 0, indicando que a região possivelmente é afetada por RIP. Clicando na opção "Download", é possível baixar a imagem para seu computador:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_05.png" alt="Exemplo de região afetada por RIP indicada no software The RIPper" align="center">
</center>
<br><br>
No bloco "Percentage RIP Affected" podemos detectar a porcentagem do genoma que é afetado pelo mecanismo de RIP e a porcentagem de conteúdo GC do genoma. Nesse exemplo, vemos que 10,16% da montagem do genoma da linhagem CBS 120486 de P. citriasiana tem assinaturas de atividade do mecanismo de RIP, e que o conteúdo GC dessa montagem de genoma é de 53,05%:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_06.png" alt="Dados de porcentagem de sequências afetadas por RIP e conteúdo GC da montagem de genoma de Phyllosticta citriasiana CBS 120486 segundo avaliação no software The RIPper" align="center">
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