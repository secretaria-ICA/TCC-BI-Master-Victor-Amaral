<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Aplicações de Otimização para Lançamento de Novos Produtos

#### Aluno: [Victor Soledade Moraes Amaral Neto](https://github.com/link_do_github)
#### Orientador: [Ana Carolina Abreu](https://github.com/link_do_github).
#### Co-orientador: [Felipe Borges](https://github.com/link_do_github). <!-- caso não aplicável, remover esta linha -->

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/link_do_repositorio). <!-- caso não aplicável, remover esta linha -->

- [Link para a monografia](https://link_da_monografia.com). <!-- caso não aplicável, remover esta linha -->

- Trabalhos relacionados: <!-- caso não aplicável, remover estas linhas -->
    - [Nome do Trabalho 1](https://link_do_trabalho.com).
    - [Nome do Trabalho 2](https://link_do_trabalho.com).

---

### Resumo

Este trabalho procurou dar contribuição aos empreendedores ou aos candidatos a ter um novo negócio para que melhorassem suas decisões com os objetivos de reduzir o risco ou aumentar o potencial de resultado de seus projetos aplicando algoritmos de otimização.
As abordagens aqui aplicadas implicaram: 1) utilização de otimização por algoritmo genético para buscar em uma pesquisa de mercado com 50 respondentes possíveis segmentos de mercado que, além das características sociodemográficas, considerassem preço máximo que o indivíduo pagaria pelo produto (WTP: Willingness to Pay); 2) aplicação de Simulação de Monte Carlo com otimização para definição de preço ótimo para os segmentos de maior potencial de lucratividade identificados na etapa anterior. A ferramenta utilizada foi Excel/Solver. Desta forma, espera-se que este trabalho possa ter utilidade mais abrangente tendo em vista o alcance de uso deste software, que está ao alcance de qualquer interessado nestas aplicações.
Nesta abordagem pode-se confirmar que a aplicação das técnicas de otimização propiciou encontrar segmentos distintos na base de dados e propiciou também contribuir para com as decisões de precificação e alocação de verba de divulgação para atingir, dependendo da intenção do empreendedor, diferentes objetivos: otimização do lucro, minimização do risco ou ainda melhor relação retorno risco. A aplicação de modelos de otimização resultou em estabelecimento dos 3 parâmetros de decisão (Escolha dos segmentos de mercado, definição dos preços para cada segmento e alocação de verba de divulgação a cada segmento escolhido) materialmente melhores do que modo prevalente no mercado de lançar os produtos para diversos perfis de consumidores ao preço similar ao de produtos similares.




### 1. Introdução

Este trabalho tratou da continuação da abordagem feita na disciplina de OP em que buscou-se aplicar ferramentas de otimização e de técnicas de decisão sob incerteza para potencializar o retorno do lançamento de um novo produto. As técnicas aplicadas na disciplina de OP, por si, já indicaram o valor de modelagens matemáticas no auxílio dos decisores, mais especificamente neste caso dos empreendedores, para dar mais segurança a seus projetos.

Levando em conta a taxa de mortalidade de novos negócios e seu impacto nos diversos envolvidos, procurou-se demonstrar aqui como algoritmos de Machine Learning e de Otimização podem nortear decisões complexas de mercado, tais como:

  - Qual ou quais preços devem ser cobrados pelo produto?
  - Qual segmento de mercado deve ser acionado?
  - Qual é a lucratividade esperada do projeto?
  - Quais são os riscos de perda e qual é a probabilidade de que ocorra?

Embora se reconheça a importância da sensibilidade do especialista, as técnicas quantitativas possibilitam melhorar suas decisões, evitando eventualmente prejuízos ou lucros sub ótimos.

Para alcançar estas intenções, lançou-se mão de matérias pertencentes às áreas de Microeconomia, Estatística, Inteligência Artificial (Machine Learning) e Marketing. Elas foram aplicadas a uma pesquisa de mercado feita com cinquenta respondentes em que se procurou medir a aceitação de um e-book e, mais importante, medir o valor máximo que cada um deles estaria disposto a pagar.

Como tentativa de democratizar a aplicação da abordagem deste trabalho para pequenos empreendedores, toda a modelagem foi desenvolvida em Excel, tornando desnecessária qualquer programação, mas tão somente conhecimento avançado nesta ferramenta.


### 2. Modelagem

A modelagem do objeto deste trabalho de conclusão, como mencionado, foi integralmente feita em Excel. Seguiu as etapas abaixo:

  - Análise exploratória da base de dados (cinquenta respostas da pesquisa);
  
  - Normalização das variáveis numéricas por Z-Score.

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
