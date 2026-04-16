---
title: Detecção de assinaturas de mutação de ponto induzida por repetição (repeat-induced point mutation)
description: Softwares utilizados, The RIPper
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
Na opção <i>"RIP genome"</i> podemos avaliar as assinaturas de RIP de forma conjunta para o genoma inteiro. Ao clicar nesse botão, a ferramenta irá rodar a análise (o que pode levar um tempo considerável a depender do tamanho de genoma avaliado), e ao concluir, irá redirecionar para a página de resultados. Na seção <i>"RIP analysis"</i> é possível configurar os parâmetros da análise. Caso qualquer parâmetro seja modificado, é necessário clicar em <i>"Update"</i> para atualizar a análise:
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
No bloco abaixo da seção <i>"RIP Analysis"</i> é possível avaliar as assinaturas de RIP separadamente para cada contig ou scaffold. Na opção <i>"Select a Sequence"</i> é possível escolher o contig/scaffold de interesse, e definir o intervalo a ser avaliado em <i>"Start and End Range"</i>, e clicar em <i>"Update Range"</i>. Ao selecionar o intervalo, a ferramenta atualizará o gráfico dos indíces Product, Substrate e Composite apresentado a seguir. No exemplo indicado abaixo, vemos uma região de 20000 pares de bases no scaffold 1 em que o trecho próximo à coordenada de 7000 pares de basess apresenta um valor de Product maior que 1,1, Substrate menor que 0,75 e Composite maior que 0, indicando que a região possivelmente é afetada por RIP. Clicando na opção <i>"Download"</i>, é possível baixar a imagem para seu computador:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_05.png" alt="Exemplo de região afetada por RIP indicada no software The RIPper" align="center">
</center>
<br><br>
No bloco <i>"Percentage RIP Affected"</i> podemos detectar a porcentagem do genoma que é afetado pelo mecanismo de RIP e a porcentagem de conteúdo GC do genoma. Nesse exemplo, vemos que 10,16% da montagem do genoma da linhagem CBS 120486 de <i>P. citriasiana</i> tem assinaturas de atividade do mecanismo de RIP, e que o conteúdo GC dessa montagem de genoma é de 53,05%:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_06.png" alt="Dados de porcentagem de sequências afetadas por RIP e conteúdo GC da montagem de genoma de Phyllosticta citriasiana CBS 120486 segundo avaliação no software The RIPper" align="center">
</center>
<br><br>
Para salvar os resultados, utilizaremos a opção <i>"Export GFF3 RIP data (Genome)"</i>, que fornecerá um arquivo GFF3 contendo as coordenadas genômicas das regiões afetadas por RIP. A outra opção, intitulada "Export GFF3 RIP data (Sequence)", fornece somente as coordenadas da sequência escolhida na seção <i>"Select a Sequence"</i>. Clique no botão <i>"Export GFF3 RIP data (Genome)"</i> e salve o arquivo GFF3 na localização de preferência em seu computador:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_07.png" alt="Opções para exportar arquivos GFF3 no software The RIPper" align="center">
</center>
<br><br>
Ao abrir o arquivo GFF3 em algum editor de texto como o Notepad++, é possível observar a presença de 09 colunas:
<br><br>
<ol>
<li><b>01 - seqid: </b>nome do contig ou scaffold em que a coordenada está localizada</li>
<li><b>02 - source: </b>nome da ferramenta que gerou os dados apresentados (nesse caso, The RIPper)</li>
<li><b>03 - type: </b>tipo de coordenada anotada (nesse caso, RIP, uma região afetada por RIP)</li>
<li><b>04 - start: </b>posição de início da coordenada<br>
<li><b>05 - end: </b>posição de final da coordenada</li>
<li><b>06 - score: </b>score de confiabilidade atribuída pela ferramenta, quando aplicável</li>
<li><b>07 - strand: </b>indica se a coordenada anotada está na fita direta (+) ou reversa (-)<br>
<li><b>08 - phase: </b>fase de leitura, caso a coordenada se refira à uma região codificante</li>
<li><b>09 - attributes: </b>atributos ou informaçõess adicionais fornecidas pela ferramenta. Nesse caso, podemos observar os valores dos índices Product, Substrate e Composite para cada coordenada avaliada.</li>
</li>
</ol>
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_08.png" alt="Exemplo de arquivo GFF3 gerado pelo software The RIPper" align="center">
</center>
<br><br>
</div>

### Calculate LRAR

<div align="justify">
Na opção <i>"Calculate LRAR"</i> podemos avaliar a presença de grandes segmentos genômicos com assinaturas de RIP (<i>Large RIP Affected Genomic Regions</i>). Por padrão, a ferramenta considera uma região como potencial LRAR ao avaliar janelas de 1000 pares de bases com passos de 500 pares de bases, e encontrar sete janelas consecutivas contendo assinaturas de RIP. Na seção <i>"Parameters"</i> é possível configurar os parâmetros da análise. Caso qualquer parâmetro seja modificado, é necessário clicar em <i>"Update"</i> para atualizar a análise:
<br><br>
<ol>
<li><b>Window Size: </b>tamanho da janela a ser utilizada, em pares de bases</li>
<li><b>Slide size: </b>tamanho da janela deslizante a ser utilizada, em pares de bases</li>
<li><b>Minimum Composite: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Minimum Product: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Maximum Product: </b>valor máximo do índice Substrate a ser considerado</li>
<li><b>Composite Index Chain: </b>quantidade mínima de janelas consecutivas com assinatura de RIP</li>
<li><b>Change em GC content: </b>avaliação de mudanças no conteúdo GC<br>
</li>
</ol>
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_09.png" alt="Parâmetros da seção Calculate LRARs no software The RIPper" align="center">
</center>
<br><br>
A seguir, podemos ver um exemplo de resultado da análise, utilizando os dados da montagem de genoma da linhagem CBS 120486 de <i>P. citriasiana</i>. A ferramenta gera uma tabela indicando as coordenadas de LRARs encontradas, bem como tamanho e respectivos índices. Clicando no ícone de lista no canto superior direito da tabela, é possível exportar os resultados em diferentes formatos, como PDF, Excel e CSV. Utilizaremos a opção <i>"Export all data as csv"</i> para gerar um arquivo CSV dos resultados:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_10.png" alt="Exportação de arquivo CSV contendo coordenadas de LRARs a partir de análise do software The RIPper" align="center">
</center>
<br><br>
</div>

## RIP Profile

<div align="justify">
Na opção <i>"RIP profile"</i> podemos avaliar gerar um resumo geral do perfil de assinaturas de RIP e presença de LRARs no genoma, complementando os resultados obtidos nas análises anteriores. Na seção <i>"Parameters"</i> é possível configurar os parâmetros da análise. Caso qualquer parâmetro seja modificado, é necessário clicar em <i>"Update"</i> para atualizar a análise:
<br><br>
<ol>
<li><b>Window Size: </b>tamanho da janela a ser utilizada, em pares de bases</li>
<li><b>Slide size: </b>tamanho da janela deslizante a ser utilizada, em pares de bases</li>
<li><b>Minimum Composite: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Minimum Product: </b>valor mínimo do índice Composite a ser considerado</li>
<li><b>Maximum Product: </b>valor máximo do índice Substrate a ser considerado</li>
<li><b>Composite Index Chain: </b>quantidade mínima de janelas consecutivas com assinatura de RIP</li>
<li><b>Change em GC content: </b>avaliação de mudanças no conteúdo GC<br>
</li>
</ol>
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_11.png" alt="Parâmetros da seção RIP Profile no software The RIPper" align="center">
</center>
<br><br>
A seguir, podemos ver um exemplo de resultado da análise, utilizando os dados da montagem de genoma da linhagem CBS 120486 de <i>P. citriasiana</i>. A ferramenta gera uma tabela indicando várias informações:
<br><br>
<ol>
<li><b>Genome size (pb): </b>tamanho do genoma avaliado em pares de bases</li>
<li><b>Count of Genomic Windows Investigated: </b>quantidade de janelas avaliadas, de acordo com o tamanho de janela definido nos parâmetros</li>
<li><b>GC Content of Genome Assembly (%): </b>conteúdo GC% do genoma avaliado</li>
<li><b>Number of RIP Affected Windows: </b>número de janelas avaliadas contendo assinaturas de RIP</li>
<li><b>RIP Affected Genomic Proportion (%): </b>proporção da montagem de genoma avaliada que possui assinaturas de RIP</li>
<li><b>Count of LRARs: </b>quantidade de grandes segmentos genômicos afetados por RIP, de acordo com a quantidade mínima de janelas consecutivas especificada nos parâmetros</li>
<li><b>Average Size of LRARs (bp): </b>tamanho médio das LRARs em pares de bases<br>
<li><b>Average GC Content of LRARs (%): </b>conteúdo GC% médio das LRARs</li>
<li><b>Genomic Proportion of LRARs (bp): </b>proporção da montagem de genoma que corresponde às LRARs encontradas, em pares de bases</li>
<li><b>Product Value for LRARs: </b>valor médio do índice Product para LRARs<br>
<li><b>Substrate Value for LRARs: </b>valor médio do índice Substrate para LRARs<br>
<li><b>Composite Value for LRARs: </b>valor médio do índice Composite para LRARs<br>
</li>
</ol>
<br><br>
Para realizar o download de um arquivo CSV contendo essas informações, utilizaremos a opção <i>"Download RIP Profile"</i>:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_12.png" alt="Resultados da análise RIP Profile no software The RIPper e opção de exportação de arquivo" align="center">
</center>
<br><br>
</div>

### RIP Sequence

<div align="justify">
Na opção <i>"RIP sequence"</i> podemos avaliar as assinaturas de RIP separadamente para cada contig ou scaffold. Para cada contig/scaffold, a ferramenta informa o comprimento (Length) e conteúdo GC em porcentagem (GC Content), e fornece as opções de calcular as assinaturas de RIP ou LRAR individualmente, conforme já explorado nas seções anteriores. A imagem a seguir mostra um exemplo baseado na montagem de genoma da linhagem CBS 120486 de <i>P. citriasiana</i>:
<br><br>
<center>
<img src="https://raw.githubusercontent.com/biogemm-ufpr/genomics/master/_data/img/fungos/TEs/RIPper/ripper_13.png" alt="Opções RIP sequence e Calculate LRARs para avaliar scaffolds individualmente na montagem de genoma de Phyllosticta citriasiana CBS 120486 no software The RIPper" align="center">
</center>
<br><br>
</div>