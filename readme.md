<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Aplicações de Otimização sob Incerteza para Lançamento de Produtos

#### Aluno: [Victor Soledade Moraes Amaral Neto](https://github.com/link_do_github)
#### Orientador: [Ana Carolina Abreu](https://github.com/link_do_github).
#### Co-orientador: [Felipe Borges](https://github.com/link_do_github). <!-- caso não aplicável, remover esta linha -->

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/VictorAmaralNeto/TCC-BI-Master-Victor-Amaral/blob/main/Arquivo%20da%20Modelagem.xlsm)

- Trabalhos relacionados: <!-- caso não aplicável, remover estas linhas -->

     - [EMPREENDEDORISMO SUSTENTÁVEL: CAUSAS DA MORTALIDADE DAS MICRO E PEQUENAS EMPRESAS NO MUNICÍPIO DE GUARAPUAVA-PR NO PERÍODO DE 2006 A 2010 - Sansana (2013)](https://riut.utfpr.edu.br/jspui/bitstream/1/692/1/PB_PPGDR_M_Sansana%2C%20Jos%C3%A9%20Carlos_2013.pdf)
    - [OPORTUNIDADE OU NECESSIDADE? UM ESTUDO DO IMPACTO DO EMPREENDEDORISMO NO DESENVOLVIMENTO ECONÔMICO - Rocha (2014)](https://periodicos.unichristus.edu.br/gestao/article/download/146/377)
    - [Análise de Agrupamentos com Uso do Excel - Oliveira (2015)](https://repositorio.ufmg.br/bitstream/1843/BUBD-A3QEUR/1/monografia_davidson_vers_o_final.pdf).
    - [The Impact of Price Segmentation based on Customer Characteristics, Product Bundle or Product Features on Price Fairness Perceptions - Nazari e Sheikholeslami (2021)](https://jimm.journals.umz.ac.ir/article_3367_e408bef6742b349b39977526f3746607.pdf).
    - [Application of the Price Discrimination in Marketing - Porcheva (2013)](https://www.researchgate.net/profile/Tatyana-Netseva-Porcheva/publication/341452650_Application_of_the_Price_Discrimination_in_Marketing/links/5ec2311d92851c11a87043ce/Application-of-the-Price-Discrimination-in-Marketing.pdf)
  
---

### Resumo

Este trabalho procurou dar contribuição aos empreendedores e aos candidatos a ter um novo negócio para melhoria de seu processo decisório com os objetivos de reduzir o risco ou aumentar o potencial de resultado de seus novos produtos aplicando algoritmos de otimização. Utilizou dados primários de pesquisa de mercado de conceito, e precificação de um e-book voltado a finanças quantitativas para investidores pessoas físicas.
As abordagens aqui aplicadas implicaram: 1) utilização de otimização por algoritmo genético para buscar em uma pesquisa de mercado com 50 respondentes possíveis segmentos de mercado que, além das características sociodemográficas, considerassem preço máximo que o indivíduo pagaria pelo produto (WTP: Willingness to Pay); 2) aplicação de Simulação de Monte Carlo com otimização para definição de preço ótimo e alocação de verba de divulgação ótima para os segmentos de maior potencial de lucratividade identificados na etapa anterior.
A ferramenta utilizada foi Excel/Solver. Desta forma, espera-se que este trabalho possa ter utilidade mais abrangente tendo em vista o alcance de uso deste software.
Nesta abordagem pode-se confirmar que a aplicação das técnicas de otimização propiciou encontrar segmentos distintos na base de dados e propiciou também contribuir para com as decisões de precificação e alocação de verba de divulgação para atingir, dependendo da intenção do empreendedor, diferentes objetivos para o projeto: maximização do lucro, minimização do risco ou a maximização da relação retorno risco.
A aplicação de modelos de otimização neste trabalho resultou em estabelecimento dos 3 parâmetros de decisão (escolha dos segmentos de mercado, definição dos preços para cada segmento e alocação de verba de divulgação a cada segmento escolhido) que indicaram esperanças matemáticas de lucro e risco substancialmente melhores do que as do modo prevalente no mercado, que é o de lançar os produtos para diversos perfis de consumidores ao preço equivalente ao de produtos similares.

### 1. Introdução

O empreendedorismo, além de seu reconhecido valor para a Economia, vem se tornando necessidade de muitos indivíduos que não conseguem oportunidades no mercado formal de trabalho (Rocha, 2014). Por outro lado, como observa Sansana (2013), a taxa de insucesso dos novos negócios pode impactar materialmente todos os envolvidos (proprietário, empregados, fornecedores entre outros). Neste contexto, utilizando pesquisa de mercado de novo e-book sobre finanças quantitativas com 50 respondentes, procurou-se demonstrar como algoritmos de otimização conjugados com técnicas de decisão sob incerteza podem melhorar decisões complexas de mercado, tais como:

  - Identificar e escolher segmentos de mercado com dados estruturados?
  - Qual ou quais preços devem ser cobrados pelo produto de acordo com diferentes objetivos?
  - Qual ou quais segmentos de mercado devem ser acionados?
  - Qual é a lucratividade esperada do projeto?
  - Quais são os riscos de perda e qual é a probabilidade de que perdas ocorram?

Portanto, esta abordagem procurou lançar luz em três perguntas principais:

  - A segmentação de mercado com decorrente possibilidade de cobrar preços diferentes para cada um dos segmentos potencializa a relação retorno/risco do produto (Porcheva, 2013)?
  - A prática de otimização de preços potencializa a relação retorno/risco do produto?
  - Em que medida a aplicação de otimização sob incerteza contribui para que decisões mais assertivas sejam tomadas?  

Para alcançar estas intenções, lançou-se mão de matérias pertencentes às áreas de Microeconomia, Estatística, Machine Learning e Marketing. Elas foram aplicadas à mencionada pesquisa de mercado que além de testes de conceito e aceitação, mediu também m valor máximo que cada respondente estaria disposto a pagar, variável fundamental para buscar os objetivos deste trabalho.

Embora se reconheça a imprescindível necessidade de se contar com a sensibilidade do especialista, as técnicas quantitativas aqui aplicadas, ressalvadas as restrições à segmentação de preço observadas por Nazari e Sheikholeslami (2021), possibilitaram melhorar decisões, minimizando a chance de haver prejuízos ou, na melhor das hipóteses, de haver lucros sub ótimos em um projeto de lançamento de um novo produto.

Apesar das limitações desta abordagem (base reduzida, base desbalanceada e vieses de conveniência social), foi possível verificar o valor das modelagens matemáticas como complemento à experiência e à intuição humanas. As aplicações de análise de agrupamento para segmentação da base de dados de otimização sob incerteza indicaram caminhos de escolha de segmentos e de precificação que diminuíram o risco potencial do lançamento do produto e aumentaram substancialmente a esperança matemática de sua lucratividade.

Como tentativa de democratizar a aplicação da abordagem deste trabalho para pequenos empreendedores, toda a modelagem foi desenvolvida em Excel, tornando desnecessária qualquer programação em outras ferramentas, mas tão somente conhecimento avançado neste software.


### 2. Modelagem

A modelagem do trabalho incluiu 3 abordagens: 1) segmentação da base de dados utilizando técnica de agrupamento, aplicando Excel/Solver/Evolutinary; 2) Cálculo das curvas de demanda da base completa e dos dois segmentos mais promissores e 3) aplicação de otimização com Simulação de Monte Carlo para definir preços ótimos e alocação mais eficiente  da verba de divulgação para atender aos objetivos de maximizar lucro, minimizar riscos ou de encontrar relação ótima risco/retorno.

Etapas da modelagem:

  - Análise exploratória da base de dados (50 respostas da pesquisa);
  
  - Discretização das variáveis e contínuas e codificação de todas as variáveis propiciando aplicar cálculo das distâncias de Hamming (capazes de lidar com dados categóricos), como base do método de agrupamento utilizando Excel/Solver;

  - Análise de Agrupamento sobre 50 respondentes para alocá-los a 5 grupos considerando semelhanças sociodemográfica e WTP, conforme abordagem de Oliveira (2015);
  
  - Identificação seleção de dois grupos mais promissores resultantes da etapa anterior. Buscou-se dois grupos homogêneos do ponto de vista sociodemográfico com as maiores propensões a pagar médias (WTP);
  
  - Cálculo das três curvas de demanda utilizando regressão linear simples: da base completa e de cada um dos dois segmentos mais promissores;
  
  -  Aplicação de otimização com Simulação de Monte Carlos com 1000 cenários para definição de preços e alocações e verba de divulgação ótimos para os objetivos de maximização de lucro, minimização de riscos ou maximização da relação retorno sobre risco (desvio padrão dos lucros esperados);
  -  
  -  Elaboração de experimento com 9 possibilidades de decisão decorrentes de dois objetivos diferentes de otimização combinados com opções de acionar todos os consumidores, consumidores do segmento 1, consumidores do segmento 2 ou os ambos os segmentos com diferentes preços.
 
### 3. Resultados

A aplicação da metodologia deste trabalho evidenciou a utilidade da técnica de otimização sob incerteza para com o processo decisório do empreendedor, mais especificamente, na desafiadora tarefa de lançar um produto.

O software Excel e sua aplicação Solver mostraram-se suficientemente robustos para os objetivos de resolução de análise de agrupamentos e de otimização sob incerteza.

Como se vê na tabela abaixo, a modelagem aqui proposta possibilitou armar o decisor com informações valiosas, auxiliando-o com a escolha de quais preços praticar em que segmentos de mercado.


![alt text](https://github.com/VictorAmaralNeto/TCC-BI-Master-Victor-Amaral/blob/main/Imagem4.jpg)

O cenário 1 (doravante chamado cenário-base), por exemplo, apesar de ser prática recorrente entre iniciantes em negócios, ou seja, simplesmente atribuir o valor médio de e-books (neste caso R$ 50,00 por unidade) vendidos pela internet e divulgando indiscriminadamente para consumidores de perfis heterogêneos, mostrou-se a pior opção do experimento.

O cenário 2 é igual ao primeiro, porém praticando preço otimizado. Considerando a curva de demanda de todos os respondentes da base de dados, caso o empreendedor cobrasse R$ 70,00 ao invés de R$ 50,00, o lucro mensal final tenderia a aumentar 34% em relação ao cenário -base.

O cenário 3 tem objetivo diferente dos dois anteriores. No lugar do lucro, buscou-se otimizar a relação retorno / risco. Não houve diferença significativa em comparação com o cenário 2.

O cenário 4 representa a escolha do empreendedor em atuar apenas no segmento 2 (mulheres da classe B, região Sudeste e entre 25 e 35 anos). Neste cenário também foi aplicado o preço não otimizado de R$ 50,00. Como o segmento possui WTP maior do que a média, a lucratividade  esperada supera a do cenário-base em 36%.

O cenário 5, de mesmo conceito do cenário 4, mas atuando no segmento 3 (homens da classe B, região Sudeste entre 40 e 50 anos), a lucratividade esperada foi 136% maior do que a do cenário 1. Este segmento, portanto, é ainda menos sensível ao preço doque o segmento 2.

O cenário 6 tratou de buscar a maximização do lucro combinando os dois segmentos, variando os preços e variando a alocação da verba para divulgação entre os dois segmentos restrita à compra de 20.000 cliques por mês. A modelagem indicou que neste caso o decisor deveria explorar apenas o segmento 3, com preço ótimo de R$ 104,00. A lucratividade esperada desta opção é 340% maior do que a do cenário-base.

Os cenários 7 e 8 buscaram maximizar a relação retorno/risco esperada tomando os dois segmentos isolada e respectivamente. Não houve neste caso melhora significativa em relação ao objetivo de maximização de lucro deles, mas, como esperado, a aplicação da otimização indicou cobrança de preços que propiciaram tanto o risco quanto a rentabilidade superarem significativamente os verificados no cenário-base.

O cenário 9 replicou o cenário 6, mas mudou o objetivo da otimização para maximização do retorno/risco. Muito embora a rentabilidade esperada tenha sido menor do que o cenário 6 (a mais rentável do experimento), este cenário indicou ser mais eficiente no tratamento do risco. O indicador retorno/risco aqui ficou em 1,72 versus 1,48 do cenário 6. Pode-se concluir que o empreendedor menos avesso ao risco poderia optar pelo cenário 6 e um mais avesso poderia buscar a relação mais eficiente deste cenário 9. Aqui o resultado da otimização indicou que aproximadamente metade dos cliques deveria ser alocado para cada segmento e os preços ótimos praticados para o segmento 2 e 3 deveriam ser de R$ 68,00 e R$ 85,00, respectivamente.

### 4. Conclusões

Este trabalho procurou verificar se aplicações de otimização sob incerteza poderiam ser úteis para quem pretendesse lançar um produto. Mesmo restringindo o uso de ferramentas a apenas o Excel, e mesmo com uma base de dados pequena e desbalanceada, foi possível demonstrar o valor de algoritmos de otimização para o processo decisório do empreendedor. Sabe-se há tempo que práticas de segmentação de mercado e precificação próximas à ótima são estratégicas importantes a qualquer negócio, e seu afastamento pode, na melhor das hipóteses, comprimir a lucratividade de produtos ou trazer riscos mais elevados. A modelagem matemática de otimização aqui aplicada indicou poder auxiliar com a determinação de melhores segmentos de mercado e dos melhores preços a serem aplicados a eles.

---

Matrícula: 211.100.463

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
