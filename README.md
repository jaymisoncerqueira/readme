# Neurowood

Captação de imagens por meio de equipamentos totalmente planejados para uma aplicação eficaz.


## Coleta de imagens e criação de banco de dados
----------------

### A execução de experimentos computacionais utilizando bases de dados de imagens de madeira.

Na inspeção visual automatizada de materiais naturais, em geral, é necessário um grande número de amostras de treinamento, as quais devem ser corretamente rotuladas. Entretanto, obter esse conjunto de dados pode ser um grande desafio para humanos, uma vez que estes são propensos a erros. Adicionalmente, caso a aparência do material mude entre os lotes, será necessário a readaptação dos dados de treinamento ou a nova rotulagem dos anteriores.



O processo da construção do banco de dados se dará em algumas etapas, sendo elas:

* Reconhecimento do local de instalação pela equipe técnica;
* Utilização de material próprio para aquisição de imagens preliminares;
* Treinamento do modelo com imagens preliminares e validação do mesmo;
* Captação de imagens para construção do banco de dados;
* Instalação do produto final de acordo com as especificações;
* Transferência de conhecimento entre o modelo treinado e o equipamento final que será utilizado;
* Validação do modelo final.


Inicialmente é necessário que algumas amostras preliminares sejam coletadas, para isso, algumas imagens de madeira serão capturadas no intuito de desenvolver um banco de dados, utilizando equipamento próprio da equipe técnica, e também de treinar o modelo e consecutivamente valida-lo. Para isso, Será realizado um contato inicial com o cliente para identificar e compreender o processo da linha de produção e as principais dificuldades de sua empresa e, assim, efetuar o estudo das melhores diretrizes para obtenção das imagens e implementação do algoritmo. Posteriormente, serão analisados os resultados prelminares e serão propostas melhorias, para averiguar se estão de acordo com a necessidade do cliente, demonstrando assim, por meio deste protótipo, os dados promissores e satisfatórios. Ainda nessa etapa inicial 

Uma vez implementada as melhorias e validado os resultados, será necessário realizar a montagem estrutural do equipamento conforme especificado anteriormente. Um próximo passo será a realização da transferência de conhecimento entre o modelo do protótipo para os equipamentos adquiridos, esse processo visa habilitar o equipamento final a tomar as decisões da mesma maneira como foi feita com os dados preliminares validadis. Por fim, será realizado uma validação final do modelo e entrega do produto final já com a parte estrutural e algoritmo implementados capaz de fazer a classificação das materias com base no banco de dados proposto.







### Rotulação dos dados

Um passo importante nessa etapa é justamente a rotulação de dados, a rotulação de dados está atrelada ao conhecimento das amostras que serão tratadas.
Levanto em consideração aplicação vigente para esse sistema, é necessário que os dados sejam rotulados a fim de entender o que será considerado como sendo bom ou ruim, o que sería uma amostra aceitável ou não. Isso se faz estremamente necessário pois a partir dessas informações será possível treinar o modelo novamente aumentando assim a sua acuracidade.

Não há a necessidade de todas imagens serem rotuladas, isso acaba demorando e diminuindo o desempenho do modelo. Visto isso, uma abordagem inicial é selecionar imagens mais detalhadas com maiores informações possíveis para que essas sim sejam rotuladas. Após esse processo, o algoritmo é capaz de selecionar uma amostra não rotulada e fazer a predição de sua classificação e após esse processo o modelo deve ser treinado novamente no entanto é possível que o modelo sejá mais eficaz mas também é possível que esse novo treinamento seja maléfico. Isso ocorre devido a dificuldade humana de rotulação de dados e levar em consideração todas as caracteristicas naquela imagem. Portanto, visto essa dificuldade humana de rutulação dos dados, utilizando uma quantidade reduzida de dados precisamente rotulados pode ter um grande retorno positivo. 

![es](https://user-images.githubusercontent.com/87779244/129075650-51cf0b14-7831-499e-9217-455ea8696a1c.png)



A rotulação de dados geralmente é feita por equipe especializada, de forma a minimizar as variações de interpretações a respeito de um resultado.
Visto que nem todos os dados são rotulados, a imagem acima mostra um pouco de como será feita a classificação das imagens.
O algoritmo seleciona uma amostra não rotulada que possui uma categorização incerta, logo após, é atribuido uma classificação para este exemplo com base nos dados préviamente rotulados. Em seguida, os modelos são treinadas novamente usando este novo conjunto de dados rotulados.
Por fim, dado à dispersão dos exemplos no espaço de amostras,o processo se baseará na suposição de uniformidade, isso quer dizer que se dois pontos estão próximos no
espaço de entrada, eles devem também estar próximos no espaço de saída, tornando possível assim a rotulação de novos dados. 





## FMEA (Failure Mode and Effect Analysis)

A FMEA foi utilizada para verificar as potenciais falhas de processo. Para isso, é importante primeiramente identificar as possíveis causas e efeitos dessas falhas. De acordo com cada modo de falha é necessário definir a severidade, ocorrência e detecção.

* Severidade da falha (IS): classificação que deve considerar questões importantes para a empresa e seus clientes como a segurança do cliente e a proteção ao meio ambiente. Sendo:

1: Pouco perceptível

2-3: Pouco importante

4-5-6: Moderado

7-8: Grave

9-10: Extremamente grave

* Ocorrência da falha (IO): indica a probabilidade da falha ocorrer. Sendo:

1: Remota

2: Muito pequena

3: Pequena

4-5-6: Moderada

7-8: Alta

9-10: Muito alta

* Detecção da falha (ID): classificação que mostra a probabilidade do problema ser detectado antes da ocorrência. Sendo: 

1: Muito alta

2-3: Alta

4-5-6: Moderada

7-8: Pequena

9: Muito pequena

10: Remota

* Após essa análise, multiplicamos os três números obtidos para encontrar o índice de risco (NPR), quanto maior for o resultado deste índice, mais crítica será aquela falha. O que significa que uma medida de ação corretiva deve ser tomada o quanto antes para evitar maiores problemas. Sendo assim temos as seguintes faixas para o NPR:


1-99: Baixo

100-500: Moderado

501-1000: Alto


![FMEA](https://user-images.githubusercontent.com/87779244/129820659-b18b5882-e0ab-4a89-8793-4a82eab5c7cd.png)
