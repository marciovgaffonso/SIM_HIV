Análise histórica dos óbitos por doenças associadas ao HIV no Estado do
Pará
================
Márcio V de G Affonso
2022-12-11

Considerando que estamos no mês **Dezembro Vermelho**, alusivo ao
combate ao HIV/AIDS, buscou-se fazer uma análise histórica dos óbitos
por doenças associadas ao HIV no Estado do Pará, no período entre 2011 e
2021. Os dados aqui utilizados estão disponíveis para consulta de forma
agregada no
[DATASUS](https://datasus.saude.gov.br/informacoes-de-saude-tabnet/),
que consolida as informações do **Sistema de Informação sobre
Mortalidade** (SIM). Contudo, neste relatório foi utilizado o pacote
`microdatasus`<sup>1</sup>, o qual permite a extração dos dados
individualizados.

<sup>1</sup>
[Link](https://www.scielo.br/j/csp/a/gdJXqcrW5PPDHX8rwPDYL7F/?lang=pt)
para acessar o artigo intitulado **Microdatasus: pacote para download e
pré-processamento de microdados do Departamento de Informática do SUS
(DATASUS)**.

## Introdução

- O que é o HIV?

  - De acordo com o Ministério da Saúde<sup>2</sup>, HIV é a sigla em
    inglês do vírus da imunodeficiência humana, causador da **AIDS**.
    Esse vírus ataca o sistema imunológico, especialmente as células
    chamadas de linfócitos T CD4+. E é alterando o DNA dessa célula que
    o HIV se multiplica no organismo para continuar a infecção.

- Doença pelo vírus da imunodeficiência humana (HIV)

  - Na Classificação Estatística Internacional de Doenças e Problemas
    Relacionados à Saúde – 10ª Revisão (CID-10), os códigos B20 a B24
    compõem o grupo Doença pelo vírus da imunodeficiência humana. Tais
    códigos são:

    - B20: Doença pelo vírus da imunodeficiência humana \[HIV\],
      resultando em doenças infecciosas e parasitárias
    - B21: Doença pelo vírus da imunodeficiência humana \[HIV\],
      resultando em neoplasias malignas
    - B22: Doença pelo vírus da imunodeficiência humana \[HIV\],
      resultando em outras doenças especificadas
    - B23: Doença pelo vírus da imunodeficiência humana \[HIV\],
      resultando em outras doenças
    - B24: Doença pelo vírus da imunodeficiência humana \[HIV\], não
      especificada

<sup>2</sup> Página do [Ministério da
Saúde](https://www.gov.br/aids/pt-br/assuntos/hiv-aids/o-que-e) sobre o
HIV/aids.

## Análises

### 1. Distribuição dos óbitos por doenças pelo HIV: um corte transversal

Durante o período entre 2011 e 2021 no Estado do Pará foram registrados
**7023** óbitos por doenças pelo HIV no SIM, o que representa **1.61%**
do total de óbitos registrados (437007).

A **Tabela 1**, que sumariza as características dos óbitos que ocorreram
nesse período, pode ser vista abaixo:

| **Characteristic**    | **N = 7,023** |
|:----------------------|:-------------:|
| Sexo                  |               |
| Feminino              |  2,263 (32%)  |
| Masculino             |  4,760 (68%)  |
| Faixa etária          |               |
| 0 - 14                |   70 (1.0%)   |
| 15 - 19               |   80 (1.1%)   |
| 20 - 29               |  1,327 (19%)  |
| 30 - 39               |  2,219 (32%)  |
| 40 - 49               |  1,699 (24%)  |
| 50 - 59               |  1,021 (15%)  |
| 60+                   |  555 (8.0%)   |
| Unknown               |      52       |
| Raça/Cor              |               |
| Amarela               |   23 (0.3%)   |
| Branca                |   891 (13%)   |
| Indígena              |   10 (0.1%)   |
| Parda                 |  5,426 (78%)  |
| Preta                 |  575 (8.3%)   |
| Unknown               |      98       |
| Escolaridade          |               |
| Nenhuma               |  602 (9.9%)   |
| 1 a 3 anos            |  1,551 (25%)  |
| 4 a 7 anos            |  1,851 (30%)  |
| 8 a 11 anos           |  1,666 (27%)  |
| 12 anos ou mais       |  422 (6.9%)   |
| Unknown               |      931      |
| Causa básica do óbito |               |
| B20                   |  4,743 (68%)  |
| B21                   |   93 (1.3%)   |
| B22                   |  680 (9.7%)   |
| B23                   |  154 (2.2%)   |
| B24                   |  1,353 (19%)  |
| Ano do óbito          |               |
| 2011                  |  507 (7.2%)   |
| 2012                  |  514 (7.3%)   |
| 2013                  |  601 (8.6%)   |
| 2014                  |  625 (8.9%)   |
| 2015                  |  664 (9.5%)   |
| 2016                  |  669 (9.5%)   |
| 2017                  |  667 (9.5%)   |
| 2018                  |  687 (9.8%)   |
| 2019                  |   709 (10%)   |
| 2020                  |  672 (9.6%)   |
| 2021                  |   708 (10%)   |

A partir dessa tabela podemos chegar a algumas conclusões, são elas:

- **68%** do total de indivíduos que foram a óbito eram do sexo
  masculino.

- **78%** do total de óbitos foram registrados como pardos.

- **65%** do total de indivíduos que foram a óbitos possuíam menos de 8
  anos de estudo.

- **68%** dos óbitos foram devido a doenças infecciosas e parasitárias,
  resultantes da infecção por HIV.

- **90%** dos óbitos se concentraram na faixa etária de 20 a 59 anos.

Quanto à distribuição dos óbitos, tais achados nos auxiliam na
identificação de alguns grupos predominantes, contudo apenas essa
análise transversal não é suficiente para identificarmos possíveis
nuances e variações. Portanto, é necessária também uma análise temporal.

### 2. Análise histórica dos óbitos por doenças pelo HIV: houve diferença ao longo dos anos?

Considerando os resultados acima, buscou-se identificar se houve alguma
mudança no perfil epidemiológico dos indivíduos que evoluíram a óbito
devido doenças pelo HIV, no período de 2011 a 2021.

No geral, em 2011, foram registrados **507** óbitos por doenças pelo
HIV, o que representou **1.55%** do total de mortes. Já em 2021, o
número de óbitos foi de **708**, **1.36%** do total.

A **Tabela 2** por sua vez sumariza os resultados observados ao longo do
período do estudo:

| **Characteristic**    | **2011**, N = 507 | **2012**, N = 514 | **2013**, N = 601 | **2014**, N = 625 | **2015**, N = 664 | **2016**, N = 669 | **2017**, N = 667 | **2018**, N = 687 | **2019**, N = 709 | **2020**, N = 672 | **2021**, N = 708 |
|:----------------------|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|
| Sexo                  |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |
| Feminino              |     167 (33%)     |     185 (36%)     |     196 (33%)     |     210 (34%)     |     207 (31%)     |     220 (33%)     |     213 (32%)     |     214 (31%)     |     214 (30%)     |     205 (31%)     |     232 (33%)     |
| Masculino             |     340 (67%)     |     329 (64%)     |     405 (67%)     |     415 (66%)     |     457 (69%)     |     449 (67%)     |     454 (68%)     |     473 (69%)     |     495 (70%)     |     467 (69%)     |     476 (67%)     |
| Faixa etária          |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |
| 0 - 14                |     4 (0.8%)      |     9 (1.8%)      |     6 (1.0%)      |     7 (1.1%)      |     6 (0.9%)      |     2 (0.3%)      |     16 (2.4%)     |     2 (0.3%)      |     11 (1.6%)     |     3 (0.4%)      |     4 (0.6%)      |
| 15 - 19               |     8 (1.6%)      |     6 (1.2%)      |     5 (0.8%)      |     10 (1.6%)     |     4 (0.6%)      |     11 (1.7%)     |     2 (0.3%)      |     12 (1.8%)     |     10 (1.4%)     |     8 (1.2%)      |     4 (0.6%)      |
| 20 - 29               |     101 (20%)     |     105 (21%)     |     126 (21%)     |     128 (21%)     |     127 (19%)     |     109 (16%)     |     133 (20%)     |     129 (19%)     |     116 (16%)     |     133 (20%)     |     120 (17%)     |
| 30 - 39               |     182 (36%)     |     154 (30%)     |     190 (32%)     |     202 (33%)     |     190 (29%)     |     237 (36%)     |     201 (30%)     |     219 (32%)     |     217 (31%)     |     222 (33%)     |     205 (29%)     |
| 40 - 49               |     119 (24%)     |     131 (26%)     |     149 (25%)     |     151 (24%)     |     157 (24%)     |     157 (24%)     |     145 (22%)     |     165 (24%)     |     187 (26%)     |     156 (23%)     |     182 (26%)     |
| 50 - 59               |     64 (13%)      |     65 (13%)      |     83 (14%)      |     78 (13%)      |     113 (17%)     |     102 (15%)     |     116 (18%)     |     94 (14%)      |     103 (15%)     |     88 (13%)      |     115 (16%)     |
| 60+                   |     24 (4.8%)     |     39 (7.7%)     |     38 (6.4%)     |     45 (7.2%)     |     60 (9.1%)     |     44 (6.6%)     |     49 (7.4%)     |     61 (8.9%)     |     62 (8.8%)     |     58 (8.7%)     |     75 (11%)      |
| Unknown               |         5         |         5         |         4         |         4         |         7         |         7         |         5         |         5         |         3         |         4         |         3         |
| Raça/Cor              |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |
| Amarela               |      0 (0%)       |     1 (0.2%)      |     2 (0.3%)      |     2 (0.3%)      |     3 (0.5%)      |     3 (0.5%)      |     2 (0.3%)      |     5 (0.7%)      |     2 (0.3%)      |     2 (0.3%)      |     1 (0.1%)      |
| Branca                |     73 (15%)      |     66 (13%)      |     93 (16%)      |     87 (14%)      |     74 (11%)      |     77 (12%)      |     54 (8.3%)     |     95 (14%)      |     77 (11%)      |     92 (14%)      |     103 (15%)     |
| Indígena              |      0 (0%)       |      0 (0%)       |     2 (0.3%)      |     1 (0.2%)      |     2 (0.3%)      |     1 (0.2%)      |     2 (0.3%)      |      0 (0%)       |     2 (0.3%)      |      0 (0%)       |      0 (0%)       |
| Parda                 |     375 (75%)     |     384 (75%)     |     448 (76%)     |     471 (77%)     |     528 (81%)     |     536 (80%)     |     550 (84%)     |     532 (78%)     |     568 (81%)     |     507 (76%)     |     527 (76%)     |
| Preta                 |     51 (10%)      |     59 (12%)      |     42 (7.2%)     |     54 (8.8%)     |     47 (7.2%)     |     49 (7.4%)     |     43 (6.6%)     |     48 (7.1%)     |     52 (7.4%)     |     65 (9.8%)     |     65 (9.3%)     |
| Unknown               |         8         |         4         |        14         |        10         |        10         |         3         |        16         |         7         |         8         |         6         |        12         |
| Escolaridade          |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |
| Nenhuma               |     39 (8.8%)     |     44 (9.4%)     |     54 (10%)      |     64 (12%)      |     59 (11%)      |     59 (9.9%)     |     46 (8.0%)     |     54 (9.0%)     |     59 (9.4%)     |     65 (11%)      |     59 (9.8%)     |
| 1 a 3 anos            |     138 (31%)     |     108 (23%)     |     138 (26%)     |     138 (26%)     |     148 (27%)     |     162 (27%)     |     154 (27%)     |     154 (26%)     |     167 (27%)     |     139 (25%)     |     105 (17%)     |
| 4 a 7 anos            |     143 (32%)     |     153 (33%)     |     162 (31%)     |     162 (30%)     |     159 (29%)     |     194 (33%)     |     196 (34%)     |     183 (31%)     |     174 (28%)     |     145 (26%)     |     180 (30%)     |
| 8 a 11 anos           |     91 (21%)      |     130 (28%)     |     138 (26%)     |     143 (26%)     |     155 (28%)     |     150 (25%)     |     132 (23%)     |     169 (28%)     |     170 (27%)     |     173 (31%)     |     215 (36%)     |
| 12 anos ou mais       |     32 (7.2%)     |     31 (6.7%)     |     37 (7.0%)     |     33 (6.1%)     |     35 (6.3%)     |     30 (5.0%)     |     44 (7.7%)     |     37 (6.2%)     |     56 (8.9%)     |     44 (7.8%)     |     43 (7.1%)     |
| Unknown               |        64         |        48         |        72         |        85         |        108        |        74         |        95         |        90         |        83         |        106        |        106        |
| Causa básica do óbito |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |                   |
| B20                   |     318 (63%)     |     353 (69%)     |     410 (68%)     |     443 (71%)     |     424 (64%)     |     422 (63%)     |     430 (64%)     |     480 (70%)     |     498 (70%)     |     466 (69%)     |     499 (70%)     |
| B21                   |     1 (0.2%)      |     6 (1.2%)      |     12 (2.0%)     |     10 (1.6%)     |     8 (1.2%)      |     3 (0.4%)      |     7 (1.0%)      |     10 (1.5%)     |     12 (1.7%)     |     7 (1.0%)      |     17 (2.4%)     |
| B22                   |     56 (11%)      |     37 (7.2%)     |     56 (9.3%)     |     41 (6.6%)     |     75 (11%)      |     72 (11%)      |     68 (10%)      |     70 (10%)      |     73 (10%)      |     64 (9.5%)     |     68 (9.6%)     |
| B23                   |     8 (1.6%)      |     4 (0.8%)      |     20 (3.3%)     |     16 (2.6%)     |     21 (3.2%)     |     14 (2.1%)     |     14 (2.1%)     |     15 (2.2%)     |     15 (2.1%)     |     15 (2.2%)     |     12 (1.7%)     |
| B24                   |     124 (24%)     |     114 (22%)     |     103 (17%)     |     115 (18%)     |     136 (20%)     |     158 (24%)     |     148 (22%)     |     112 (16%)     |     111 (16%)     |     120 (18%)     |     112 (16%)     |

Nesse sentido, podemos observar as seguintes variações:

- A diferença entre os sexos e entre raça/cor não apresentaram grandes
  variações ao longo dos anos.

- Enquanto a porcentagem de indivíduos com escolaridade de 1 a 3 anos
  diminuiu consideravelmente de 2011 para 2021, de 31% para 17%, o
  inverso ocorreu com aqueles que possuíam escolaridade entre 8 e 11
  anos, passando de 21% em 2011 para 36% em 2021.

- Ainda que os óbitos por doenças infecciosas e parasitárias resultantes
  da infecção por HIV continuem representando a maior parte dos casos,
  houve um aumento na porcentagem de óbitos por neoplasias malignas
  associadas ao HIV. Além disso, observou-se também uma diminuição na
  ocorrência de óbitos por outras doenças especificadas e não
  especificadas.

- Quanto à faixa etária, os óbitos nos indíviduos com idade entre 0 a 39
  anos diminuíram entre 2011 e 2021, mas houve um aumento naqueles com
  idade acima de 40 anos, mais especificamente nos idosos acima dos 60
  anos.

Os gráficos a seguir confirmam as variações na distribuição da
ocorrência dos óbitos de acordo com as diferentes variáveis estudadas,
ao longo dos anos do estudo:

    ## [[1]]

<img src="SIM_HIV_RMARKDOWN_files/figure-gfm/unnamed-chunk-7-1.png" style="display: block; margin: auto;" />

    ## 
    ## [[2]]

<img src="SIM_HIV_RMARKDOWN_files/figure-gfm/unnamed-chunk-7-2.png" style="display: block; margin: auto;" />

    ## 
    ## [[3]]

<img src="SIM_HIV_RMARKDOWN_files/figure-gfm/unnamed-chunk-7-3.png" style="display: block; margin: auto;" />

    ## 
    ## [[4]]

<img src="SIM_HIV_RMARKDOWN_files/figure-gfm/unnamed-chunk-7-4.png" style="display: block; margin: auto;" />

    ## 
    ## [[5]]

<img src="SIM_HIV_RMARKDOWN_files/figure-gfm/unnamed-chunk-7-5.png" style="display: block; margin: auto;" />

## Considerações finais

A partir dos achados, pode-se concluir que houve uma mudança no perfil
epidemiológico dos indivíduos que foram a óbito por doenças pelo HIV, no
período entre 2011 e 2021, no Estado do Pará.

As variações observadas nas variáveis faixa etária e escolaridade chamam
atenção. Nesse sentido, pode-se supor que considerando o aumento da % de
indivíduos acima dos 40 anos de idade que foram a óbito, pode também ter
aumentado o tempo de escolaridade desses indivíduos.

Quanto às causas básicas do óbito, é necessário um estudo investigativo
mais específico para identificar outros fatores relacionados ao óbito,
como a associação com doenças definidoras ou não da AIDS.

Conclui-se que, a definição detalhada do perfil de indivíduos que mais
evoluíram a óbito pelas doenças por HIV no Estado do Pará, viabiliza o
melhor planejamento e execução das políticas públicas que tenham como
foco o combate ao HIV/aids.
