# CognitivoAirbnbTest
Repositório para teste tecnico da Cognitivo.ai


## Como foi a definição da sua estratégia de modelagem?
    Minha estratégia de modelagem foi começar por uma análise exploratória dos dados e verificar por inspeção quais variáveis pelo bom senso e pelo meu conhecimento poderiam ser úteis para predizer o valor de preços de estadia. Isto é uma abordagem artesanal mas que produziu resultados razoáveis para uma primeira tentativa sob as condições que me foram apresentadas.
    
## Como foi definida a função de custo utilizada?
    A função de custo estava definida implícitament pela biblioteca uma vez escolhido o modelo de aprendizado. No caso eu utilizei regressão de ridge, o que implica uma função de custo do tipo diferença RMS penalizada. 


## Qual foi o critério utilizado para validação do modelo?
    O critério uilizado foi a análise do RMS do conjunto de teste. Este critério me permitiu descartar regressão linear simples para este problema. 
    
## Qual foi o critério utilizado na seleção do modelo final?
   O critério para seleção foi qual o modelo mais simples que apresenta uma diferença RMS minimamente razoável.

### Por que escolheu utilizar este método?
   Por que é o modelo mais simples que minimamente funcionou. É importante começar pelo mais simples possível, e para um teste de metodologia este se apresenta suficiente. Ele também permite eu dispensar tunagem complexa de hiper-parâmetros e considerações complicadas de escolha de funções de kernel, que seriam necessáias em modelos mais sofisticados. 
   
## Quais evidências você possui de que seu modelo é suficientemente bom?
   Ele não é suficientemente bom, e não é difícil ver isso pela minha escolha consciente em suprimir a informação temporal através de uma média no ano. Isso me conduziu a erros bastante elevados no pior caso, mas minimamente aceitáveis no caso médio, permitindo eu considerar suficiente para este teste. 
   A presença de um modelo simples que retorna resultados razoáveis permite eu me concentrar na seleção de features e limpeza de dados, as quais costumam ser etapas que apresentam melhores retornos para aplicações reais do que tunagem de modelos complexos, com excessão de casos como visão computacional onde extração de features é em si um processo excepcionalmente complexo, no qual o uso de técnicas de aprendizado para esta estapa se mostrou bastante útil. Felizmente não é o caso deste problema.
