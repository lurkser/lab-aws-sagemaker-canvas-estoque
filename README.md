-  Escolhi o dataset dataset-500-curso-sagemaker-canvas-dio.csv

-  Selecionei a quantidade de produto como coluna a ser analisada
-  Escolhi quick build para maior agilidade
-  Root Mean Square Error mede a média das diferenças entre os valores previstos pelo modelo e os valores reais no conjunto de dados, ficou em 1.527, satisfatório mas poderia ser menor com o treinamento longo de 4 horas, sendo o ideal o mais próximo de zero.
-  O Mean Absolute Square Error, é como o RMSE mas não eleva os erros ao quadrado dando um peso igual a todos, ficou em 0.178, muito bom para um modelo rápido, só de ficar menor que 1 já diz que a qualidade ficou boa.

-  O modelo criado apontou 2 colunas com possíveis impactos na principal de quantidade de estoque:
    1. Holiday_BR indica os feriados brasileiros e um impacto de 1.98%, o que aponta essa coluna como não impactante no estoque visto que está bem próxima da margem de erro do RMSE apontada acima.
    2. FLAG_PROMOCAO com valor de 0% indica que o fato do produto estar em promoção em nada afeta o estoque em nada.
       
-  É seguro dizer então que o melhor a seguir seria a análise P50 sendo ela o meio termo entre a otimista P90 e a pessimista P10 para manter um estoque bem abastecido sem faltar nem sobrar produto.
