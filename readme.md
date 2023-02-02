<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Aplicações de Otimização para Lançamento de Novos Produtos

#### Aluno: [Victor Soledade Moraes Amaral Neto](https://github.com/link_do_github)
#### Orientador: [Ana Carolina Abreu](https://github.com/link_do_github).
#### Co-orientador: [Felipe Borges](https://github.com/link_do_github). <!-- caso não aplicável, remover esta linha -->

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/link_do_repositorio). <!-- caso não aplicável, remover esta linha -->

- Trabalhos relacionados: <!-- caso não aplicável, remover estas linhas -->
    - [Nome do Trabalho 1](https://link_do_trabalho.com).
    - [Nome do Trabalho 2](https://link_do_trabalho.com).

---

### Resumo

Este trabalho procurou dar contribuição aos empreendedores ou aos candidatos a ter um novo negócio de melhoria de seu processo decisório com os objetivos de reduzir o risco ou aumentar o potencial de resultado de seus novos produtos aplicando algoritmos de otimização.
As abordagens aqui aplicadas implicaram: 1) utilização de otimização por algoritmo genético para buscar em uma pesquisa de mercado com 50 respondentes possíveis segmentos de mercado que, além das características sociodemográficas, considerassem preço máximo que o indivíduo pagaria pelo produto (WTP: Willingness to Pay); 2) aplicação de Simulação de Monte Carlo com otimização para definição de preço ótimo para os segmentos de maior potencial de lucratividade identificados na etapa anterior. A ferramenta utilizada foi Excel/Solver. Desta forma, espera-se que este trabalho possa ter utilidade mais abrangente tendo em vista o alcance de uso deste software, que está ao alcance de qualquer interessado nestas aplicações.
Nesta abordagem pode-se confirmar que a aplicação das técnicas de otimização propiciou encontrar segmentos distintos na base de dados e propiciou também contribuir para com as decisões de precificação e alocação de verba de divulgação para atingir, dependendo da intenção do empreendedor, diferentes objetivos: otimização do lucro, minimização do risco ou ainda melhor relação retorno risco. A aplicação de modelos de otimização resultou em estabelecimento dos 3 parâmetros de decisão (Escolha dos segmentos de mercado, definição dos preços para cada segmento e alocação de verba de divulgação a cada segmento escolhido) materialmente melhores do que modo prevalente no mercado de lançar os produtos para diversos perfis de consumidores ao preço similar ao de produtos similares.

### 1. Introdução

Este trabalho tratou de aplicações de ferramentas de otimização e de técnicas de decisão sob incerteza para potencializar a relação retorno/risco do lançamento de um novo produto.

O empreendedorismo, além de seu reconhecido valor para a Economia, vem se tornando necessidade de muitos indivíduos que não conseguem oportunidades no mercado formal de trabalho. Por outro lado, a taxa de insucesso dos novos negócios pode impactar materialmente todos os envolvidos (proprietário, empregdos, fornecedores entre outros) Neste contexto, utilizando pesquisa de mercado de novo e-book, procurou-se demonstrar como algoritmos de otimização conjugados com técnicas de decisão sob inceteza podem melhorar decisões complexas de mercado, tais como:

  - Qual ou quais preços devem ser cobrados pelo produto de acordo com diferentes objetivos?
  - Qual ou quais segmentos de mercado devem ser acionados?
  - Qual é a lucratividade esperada do projeto?
  - Quais são os riscos de perda e qual é a probabilidade de que ocorra?

Portanto, esta abordagem procurou lançar luz, através de modelagem matemática, a tês perguntas principais:

  - 1) A segumentação de mercado com decorrente possibilidade de cobrar preços diferentes para cada um deles potencializa a relação retorno/risco do produto?
  - 2) A prática de otimização de preços (precificação estratégica) potencializa a relação retorno/risco do produto?
  - 3) Em que medida a aplicação de otimização sob incerteza contribui para que decisões mais assertivas sejam tomadas?  

Embora se reconheça a imprescindível sensibilidade do especialista, as técnicas quantitativas possibilitaram melhorar decisões, minimizando a chance de haver prejuízos ou, na melhor das hipóteses, de haver lucros sub ótimos.

Para alcançar estas intenções, lançou-se mão de matérias pertencentes às áreas de Microeconomia, Estatística, Machine Learning e Marketing. Elas foram aplicadas a uma pesquisa de mercado feita com cinquenta respondentes em que se procurou medir a aceitação de um e-book e, mais importante, medir o valor máximo que cada um deles estaria disposto a pagar.

Embora haja obvias limitações nesta abordagem (base reduzida, base desbalanceada e vieses de conveniência social), foi possível, apesar disso, verificar o valor das modelagens matemáticas com complemento à experiência e intuição humanas.

Como tentativa de democratizar a aplicação da abordagem deste trabalho para pequenos empreendedores, toda a modelagem foi desenvolvida em Excel, tornando desnecessária qualquer programação, mas tão somente conhecimento avançado nesta ferramenta.


### 2. Modelagem

A modelagem do trabalho contou com três dimensões. 1) segmentação da base de dados utilizando técnica de agrupamento, aplicando Excel/Solver/Evolutinary; 2) Cálculo das curvas de demanda da base completa e dos dois segmentos mais promissores e 3) aplicação de otimização com Simulação de Monte Carlo para definir preços ótimos e verbas de divulgação para atender aos objetivos de maximizar lucro ou minimizar riscos ou de encontrar relação ótima risco/retorno.

Segmentação de Mercado

Como mencionado, a modelagem foi integralmente feita em Excel. Seguiu as seguintes etapas:

  - Análise exploratória da base de dados (cinquenta respostas da pesquisa);
  
  - Discretização das variáveis e contínuas e codificação de todas elas propiciando aplicar cálculo das distâncias de Hamming como base do método de agrupamento utilizando Excel/Solver;

  - Agrupamento dos 50 respondentes em 5 grupos considerando semelhanças sociodemográfica e WTP, conforme abordagem de ...... ;
  
  - Identificação seleção de dois grupos mais promissores resultantes da etapa anterior;
  
  - Cálculo das três curvas de demanda utilizando regressão linear simples: base completa e dos dois segmentos mais promissores;
  
  -  Aplicação de otimização com Simulação de Monte Carlos com 1000 cenários para definição de preços e alocações e verba de divulgação ótimos para os objetivos de maximização de lucro, minimização de riscos ou maximização da relação retorno sobre risco (desvio padrão dos lucros esperados);
  -  
  -  Elaboração de experimento com 8 possibilidades de decisão decorrentes de dois objetivos diferentes de otimização diferentes combinados com opções de acionar todos os consumidores, consumidores do segmento 1, consumidores do segmento 2, ambos os segmentos com diferentes preços.
 

  - Segmentação de mercado para determinação de grupos de respondentes utilizando o algoritmo KNN. Nesta etapa aplicou-se o algoritmo genético do Solver/Evolutionary para definir os integrantes iniciais dos grupos de forma a minimizar a distância total entre todos os integrantes e seu vizinho mais próximo. Como as variáveis escolhidas para definir os grupos resultantes foram categóricas e numéricas, para as primeiras utilizou-se a distância de Hamming e para as demais (normalizadas) a distância euclidiana. A distância total entre os integrantes e seu vizinho mais próximo foi calculada pela soma destas duas distâncias. Procurou-se selecionar um grupo correspondente ao segmento de mercado com propensão a pagar preços mais altos;
 
  - Cálculo da curva de demanda em relação ao preço utilizando Regressão Linear aplicada ao grupo identificado acima;
  
  - Definição da função lucro decorrente da curva de demanda conjugada aos custos variáveis e fixos;
  
  - Aplicação de Simulação de Monte Carlo com Otimização para definição do preço ótimo que maximiza a média dos lucros esperados;
  
  - Expandir a abordagem da Simulação de Monte Carlo com Otimização para segmentação de preços, ou seja, cobrar preços diferentes para o mesmo produto, levemente modificado, de forma a capturar os menos e os mais sensíveis ao preço dentro do segmento.


### 3. Resultados

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pulvinar nisl vestibulum tortor fringilla, eget imperdiet neque condimentum. Proin vitae augue in nulla vehicula porttitor sit amet quis sapien. Nam rutrum mollis ligula, et semper justo maximus accumsan. Integer scelerisque egestas arcu, ac laoreet odio aliquet at. Sed sed bibendum dolor. Vestibulum commodo sodales erat, ut placerat nulla vulputate eu. In hac habitasse platea dictumst. Cras interdum bibendum sapien a vehicula.

Proin feugiat nulla sem. Phasellus consequat tellus a ex aliquet, quis convallis turpis blandit. Quisque auctor condimentum justo vitae pulvinar. Donec in dictum purus. Vivamus vitae aliquam ligula, at suscipit ipsum. Quisque in dolor auctor tortor facilisis maximus. Donec dapibus leo sed tincidunt aliquam.

### 4. Conclusões

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pulvinar nisl vestibulum tortor fringilla, eget imperdiet neque condimentum. Proin vitae augue in nulla vehicula porttitor sit amet quis sapien. Nam rutrum mollis ligula, et semper justo maximus accumsan. Integer scelerisque egestas arcu, ac laoreet odio aliquet at. Sed sed bibendum dolor. Vestibulum commodo sodales erat, ut placerat nulla vulputate eu. In hac habitasse platea dictumst. Cras interdum bibendum sapien a vehicula.

Proin feugiat nulla sem. Phasellus consequat tellus a ex aliquet, quis convallis turpis blandit. Quisque auctor condimentum justo vitae pulvinar. Donec in dictum purus. Vivamus vitae aliquam ligula, at suscipit ipsum. Quisque in dolor auctor tortor facilisis maximus. Donec dapibus leo sed tincidunt aliquam.

---

Matrícula: 211.100.463

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
