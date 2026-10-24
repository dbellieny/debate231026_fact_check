# Checagens do debate presidencial da Globo — documentação metodológica

**Evento analisado:** debate presidencial da TV Globo de 23 de outubro de 2026  
**Data do levantamento:** 24 de outubro de 2026  
**Versão documentada:** 1.2  
**Documento de referência:** `relatorio_checagens_debate_globo_20261023.pdf` (5 páginas)

## 1. Objetivo e escopo

Este conjunto de dados reúne **avaliações de checagem publicadas por diferentes origens** sobre declarações atribuídas aos participantes do debate presidencial da Globo de 23/10/2026. A compilação organiza registros e classificações, permitindo examinar a cobertura das fontes, consultar os vereditos e identificar convergências ou divergências entre publicações.

**O conjunto não é uma transcrição completa do debate nem uma amostra uniforme das falas.** Os veículos selecionam afirmações e empregam quantidades, formulações e critérios próprios. Assim, as contagens descrevem o **corpus de checagens recuperado**, e não a frequência geral de declarações verdadeiras ou falsas no debate.

## 2. Composição da base principal

A versão 1.2 registra **234 avaliações classificadas** na base editorial principal, distribuídas pelas seguintes origens:

| Origem | Avaliações na base principal | Forma de obtenção/classificação |
| --- |-----------------------------:| --- |
| UOL Confere |                           29 | Rótulos explícitos do texto consolidado. |
| Lupa / Folha |                           43 | Rótulos explícitos; tratados como uma única origem de checagem. |
| Estadão Verifica |                           42 | Rótulos explícitos do texto consolidado. |
| O POVO |                           13 | Correspondência analítica de conclusões textuais, identificada na base; não são selos formais. |
| Aos Fatos |                           46 | Selos explícitos recuperados do DOM renderizado. |
| Fato ou Fake (Grupo Globo) |                           54 | Avaliações recuperadas da reportagem consolidada, distribuídas por 53 citações. |
| **Total** |                      **227** | **Avaliações publicadas, não necessariamente alegações únicas.** |


## 3. Unidade de observação e regras de contagem

- **Uma linha representa uma avaliação publicada por uma origem e atribuída a um candidato.** Uma mesma temática pode aparecer em várias origens, e cada avaliação editorial permanece registrada.
- **Avaliações compostas podem permanecer em uma única linha.** O relatório cita um veredito do Estadão que considera duas afirmações sobre fome.
- **Quando há julgamentos explícitos distintos, eles podem ser separados.** No texto do O POVO sobre apostas (*bets*), foram contadas duas alegações julgadas, uma por candidato. No Fato ou Fake, uma citação sobre fome foi desdobrada em duas avaliações explícitas.
- **Outros trechos compostos foram preservados** conforme a unidade editorial encontrada.
- **Títulos repetidos ou republicações não são novas avaliações.** As publicações da Folha e da Lupa compõem uma origem; a lista direta do Aos Fatos é a referência principal da respectiva parceria.
- **A seleção do Terra foi separada da base principal** para não duplicar uma origem associada ao Aos Fatos. Divergências de formulação e de rótulo não foram harmonizadas por inferência.

Consequentemente, `número de linhas`, `número de citações` e `número de alegações distintas` são medidas diferentes e não devem ser tratados como equivalentes.

## 4. Taxonomia de categorias

As avaliações são apresentadas em quatro categorias analíticas:

| Categoria | Interpretação na compilação |
| --- | --- |
| `verdadeiro` | Avaliações registradas como verdadeiras na classificação consolidada. |
| `falso` | Avaliações registradas como falsas na classificação consolidada. |
| `impreciso` | Agrupa engano, exagero, subestimação, acerto parcial e falta de contexto. |
| `sem_conclusao` | Reúne **insustentável** e **inconclusivo**; permanece separado das três classes anteriores. |

**Os vereditos originais são preservados** para consulta. Em especial:

- `impreciso` não deve ser automaticamente convertido em `falso`;
- `sem_conclusao` **não** corresponde a falsidade;
- ausência de informação em um campo do arquivo **não** é o mesmo que uma avaliação `sem_conclusao`;
- rótulos extraídos de selos formais e correspondências analíticas de texto devem continuar distinguíveis na documentação da origem.

## 5. Coleta, recuperação e rastreabilidade

A varredura descrita no relatório utilizou **32 consultas registradas**, pesquisas dirigidas por domínio e leitura de páginas e links. As avaliações foram recuperadas de textos consolidados, índices e elementos das páginas, conforme a fonte.

### Particularidades de recuperação

- **Aos Fatos:** os **46 selos** foram lidos do **DOM renderizado** por meio do atributo `data-stamp`, sem dedução do rótulo; as âncoras dos cards foram registradas como localizadores. O hash inicialmente obtido do HTML não representa o DOM renderizado dessa atualização.
- **Fato ou Fake:** foram recuperadas **54 avaliações em 53 citações**, usando o título e a URL canônica corretos da reportagem da Globo. Uma exclusão presente em recuperação anterior foi superada; o relatório não estabelece a causa da diferença entre as coletas.
- **UOL, Lupa e Estadão:** os rótulos foram obtidos dos textos consolidados efetivamente acessados.
- **O POVO:** as categorias consolidadas foram associadas a conclusões textuais, marcadas como correspondências analíticas em vez de selos formais.

O registro de fontes inclui URLs das reportagens, localizadores, hashes das páginas inicialmente coletadas e histórico de consultas nos arquivos de dados e na planilha.

## 6. Agrupamento e concordância entre checagens

A base utiliza identificadores de **núcleo temático por candidato e tema** para relacionar avaliações e URLs de diferentes origens. A aba **Comparações** registra convergências e divergências que merecem inspeção.

**Compartilhar `alegacao_id` ou um tema não prova equivalência integral das afirmações.** Antes de tratar registros como a mesma alegação, é necessário verificar formulação exata, período de referência, modalidade, quantificação e objeto mencionado.

O relatório descreve divergências relativas a recorte temporal, conceito contábil e formulações de indicadores econômicos. Essas diferenças são documentadas como achados de comparação entre fontes, **não como novas checagens independentes**.

### Divergências entre balanços e páginas consultadas

Foram identificadas diferenças entre números citados em balanços de terceiros e os itens efetivamente acessados nos textos primários; o relatório menciona, por exemplo, **35 versus 43** para uma referência à Lupa e **18 versus 17** para um recorte do UOL. **A regra adotada foi manter as contagens item a item das páginas acessadas**, sem atribuir causas não demonstradas a essas diferenças.

## 7. Materiais suplementares (fora das 227 avaliações)

Os conjuntos abaixo permanecem **separados** da base editorial principal:

| Suplemento | Dimensão informada | Motivo da separação |
| --- | --- | --- |
| Terra / Aos Fatos | 19 registros | Seleção vinculada a origem já contemplada; separação para evitar duplicidade de origem. |
| Daily Journal | 165 registros automatizados | Produção informada como baseada em IA, **sem revisão humana**; taxonomia distinta. |

No suplemento automatizado, `falso ou distorcido` é uma **classe mista**, que não equivale automaticamente a `falso` na taxonomia principal. O relatório registra ainda a categoria `opinião` na taxonomia da fonte, sem observações recuperadas.

**Não concatenar suplementos à base principal sem reavaliar origem, unidade de observação, taxonomia, sobreposição e existência de revisão humana.**

## 8. Matriz de cobertura e lacunas

A coleta mapeou **19 origens ou iniciativas**. Além das fontes incluídas na base principal, foram registrados materiais suplementares, transmissões e iniciativas com resultados não recuperados integralmente ou fora do recorte.

Entre as lacunas documentadas estão inventários completos de lives e painéis não recuperados, transmissões sem lista verificável de julgamentos e conteúdos referentes a outros eventos. Os casos descritos como **pendente** ou **não localizado** indicam o estado da **coleta**, não a inexistência de checagens.

A busca **não foi declarada exaustiva**. Mudanças e correções nas páginas das fontes podem alterar o corpus em coletas futuras.

## 9. Formatos, identificadores e organização dos arquivos

### Formatos

- **CSV:** codificação UTF-8 com BOM; separador `;`; contagens inteiras; campos indisponíveis representados como vazios.
- **JSON:** tabelas reunidas em uma estrutura única; campos indisponíveis representados por `null`.
- **Excel:** contagens do resumo obtidas por fórmulas vinculadas à base de checagens.

### Identificadores

| Campo | Função |
| --- | --- |
| `checagem_id` | Identifica uma avaliação individual. |
| `alegacao_id` | Agrupa o candidato e um núcleo temático; não garante equivalência literal das formulações. |
| `fonte_id` | Vincula a avaliação ao registro da fonte. |

Os registros automatizados do suplemento possuem identificadores próprios da plataforma e não integram a tabela editorial.

### Abas da planilha

| Aba | Finalidade documentada |
| --- | --- |
| **Resumo** | Contagens por origem e candidato. |
| **Checagens** | Consulta e filtragem das 234 avaliações da base principal. |
| **Originais** | Rótulos de veredito preservados. |
| **Comparações** | Relações, convergências e divergências entre avaliações. |
| **Pendências** | Questões remanescentes da recuperação. |
| **Cobertura** | Mapa de origens e estado da coleta. |
| **Método** | Regras e procedimentos. |
| **Secundários** | Informações de fontes e balanços não integrados à base principal. |
| **Fontes e consultas** | Proveniência e registro da busca. |

O relatório também descreve o **suplemento Terra** como separado da base principal.

## 10. Diretrizes para análises e gráficos

- Apresentar contagens e percentuais como **distribuição de avaliações coletadas**, não como descrição de todas as falas do debate.
- Explicitar o **denominador** de cada percentual: avaliações publicadas, alegações temáticas agrupadas ou outro recorte explicitamente definido.
- Não somar automaticamente avaliações de agências distintas como se fossem alegações independentes.
- Manter as quatro classes diferenciadas, em especial `impreciso` e `sem_conclusao`.
- Ao agregar origens, informar se há ponderação ou simplesmente soma de avaliações; na base principal, as fontes têm coberturas quantitativamente diferentes.
- Identificar filtros adicionais aplicados nos notebooks, sobretudo exclusões de portais e inclusão/remoção de suplementos.
- Não inferir **intenção de enganar**, honestidade pessoal ou um **placar geral** a partir das classificações compiladas.

## 11. Procedimento recomendado para atualizações

Conforme as orientações de manutenção do relatório:

1. Priorizar inventários ainda pendentes de lives e painéis.
2. Recuperar os julgamentos individualizados, verificando **origem, unidade de registro e revisão humana**.
3. Reabrir fontes para identificar correções ou novas publicações e **registrar a data de cada coleta**.
4. Preservar classificações originais, URLs e localizadores; revisar possíveis sobreposições entre parcerias e republicações.
5. Recontar as avaliações após alterações na base; ao acrescentar linhas ao Excel, ampliar os intervalos das fórmulas ou regenerar a planilha.
6. Atualizar este README, a versão do corpus e as legendas dos gráficos para refletir o recorte efetivamente utilizado.

## 12. Referência e limites desta documentação

Este README reorganiza as informações metodológicas do documento **_Checagens do debate presidencial da Globo_**, levantamento de **24/10/2026, versão 1.2**, páginas **1 a 5**.

- **Página 1:** base principal, categorias e recuperação de fontes.
- **Página 2:** contagens por origem/candidato e suplementos.
- **Página 3:** regras de contagem, agrupamento de alegações e divergências.
- **Página 4:** matriz de cobertura e limites da varredura.
- **Página 5:** fontes, formatos, identificadores e atualização.

O documento de origem não descreve um teste estatístico inferencial aplicado à base. Qualquer teste, modelo ou inferência adicional deve ser documentado separadamente, com hipóteses, critérios de inclusão, unidade amostral e tratamento da dependência entre avaliações.
