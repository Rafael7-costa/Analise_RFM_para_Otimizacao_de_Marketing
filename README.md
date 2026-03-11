# Analise RFM para Otimização de Marketing

# PROBLEMA DE NEGOCIO

A empresa enfrenta um desafio clássico de e-commerce em escala: sabe que reter clientes é mais barato do que adquirir novos, mas não tem clareza sobre quem são seus clientes mais valiosos, quais estão em risco de abandono e onde concentrar esforços de marketing para maximizar o LTV da base. Sem essa visibilidade, o investimento em campanhas é distribuído de forma uniforme sobre uma base heterogênea — financiando igualmente clientes de alto valor e clientes com baixíssima probabilidade de retorno.

# OBJETIVO DA ANÁLISE

Identificar Padrões de Compra: Entender o que diferencia os clientes de alto valor dos demais (produtos que compram, frequência, valor médio do pedido, país).

# PREMISSAS DA ANÁLISE

Foram utilizados dados históricos de compras de 2010 a 2011, contemplando clientes de múltiplos países em que a empresa opera. 
A segmentação foi construída com base em regras de negócio aplicadas sobre as métricas RFM calculadas para cada cliente.

# ESTRATEGIA DA SOLUÇAO

#### Limpeza de Dados: Tratar valores nulos e corrigir valores inconsistentes
#### Cálculo do RFM:
 * Recência (R): Quantos dias faz desde a última compra de cada cliente.
 * Frequência (F): Total de transações únicas de cada cliente.
 * Valor Monetário (M): Soma do TotalPrice de cada cliente.

#### Segmentar a Base de Clientes: Utilizar a metodologia RFM (Recência, Frequência, Valor Monetário) para classificar os clientes em grupos estratégicos (por exemplo, "Clientes Leais", "Clientes em Risco", "Novos Clientes").

# FERRAMENTA UTILIZADAS
#### Python - Para tratamento, limpeza dos dados e criação de novas colunas 
#### Google Sheets - Para salvar os dados tratados e fazer as análises
#### Looker Studio - Para criar as visualizações gráficas

# HIPOTESES/PERGUNTAS ANALISADAS

#### Qual segmento possui mais clientes?
#### O que diferencia comportamentalmente um Cliente Campeão dos demais segmentos?
#### Qual País tem mais potencial de monetização?
#### Qual país tem mais Clientes Campeões?
#### Quais produtos são mais consumidos por país e por segmento?

# SEGMENTAÇÃO RFM
### A base está invertida — clientes perdidos dominam, campeões são minoria
A segmentação revelou desequilíbrio estrutural crítico: a empresa possui grande concentração de Clientes Perdidos e baixo volume de Campeões e Fiéis. Esse perfil indica que a empresa adquire clientes com eficiência, mas falha em convertê-los em compradores recorrentes — o custo de aquisição é pago, mas o LTV não é capturado. Cada real investido em reativar Clientes Perdidos compete diretamente com o que poderia ser investido em acelerar a progressão de Novos Clientes e Clientes em Risco para segmentos superiores.
![Análise 1](img/1.png)

# INSIGTHS DA ANALISE

#### Análise por segmento
#### O caminho para Campeão está mapeado — e é atingível
A análise definiu com precisão o benchmark do segmento de maior valor:
![Análise 1](img/2.1.png)
Esse parâmetro transforma a segmentação de um diagnóstico estático em uma régua de progressão: é possível identificar quais clientes estão mais próximos do benchmark e priorizá-los nas ações de ativação.

### Cada segmento tem uma alavanca específica — e custo-benefício distinto

1. Campeões: maior ROI de campanha — resposta positiva a exclusividade, acesso antecipado e ações de embaixador de marca. Investimento aqui tem retorno direto e imediato.

2. Clientes Fiéis: padrão de recência similar ao Campeão, mas frequência abaixo do benchmark. Upsell e cross-sell baseados em histórico de compra são as alavancas mais eficientes para elevar ticket e frequência.

3. Novos Clientes: janela crítica de conversão. O incentivo à segunda compra — com cupom de prazo curto — é o mecanismo com maior impacto na formação do hábito de recompra. Perder esse momento significa aumentar o risco de migração para Clientes Perdidos.

4. Outros/Atenção: ticket médio elevado com baixa frequência — perfil com potencial latente. Personalização forte baseada em histórico e programa de fidelidade podem ativar recorrência sem necessidade de desconto agressivo.

5. Clientes em Risco: longo período sem compra e baixa frequência. Campanhas de reativação com desconto ou frete grátis por tempo limitado são o principal recurso, mas a prioridade é entender a causa do abandono antes de investir em reativação genérica.

6. Clientes Perdidos: segmento que exige decisão antes de ação. O custo de reativação provavelmente supera o retorno esperado — a recomendação é uma oferta de última chance e, sem resposta, exclusão das listas de marketing pago para otimizar o custo de mídia nos demais segmentos.

#### Monetização por Pais
#### Europa concentra receita — mas Reino Unido esconde um risco de dependência

A maior força de monetização está na Europa, com o Reino Unido liderando em volume e variedade de produtos vendidos. Porém, mesmo o país de maior receita apresenta déficit significativo de Clientes Campeões — padrão que se repete nos demais países europeus. Isso indica que a empresa tem presença geográfica consolidada, mas ainda não converteu essa presença em base de alto valor. O potencial de crescimento dentro dos mercados já ativos é expressivo e não exige expansão geográfica para ser capturado.
![Análise 1](img/3.png)
![Análise 1](img/4.png)

#### Produto
#### O produto revela o estágio do cliente

O comportamento de compra por segmento entrega um sinal estratégico relevante: Novos Clientes concentram compras em materiais de escritório — produtos de baixo envolvimento e alta recorrência funcional, não emocional. Clientes Perdidos compraram principalmente um jarro de cerâmica — item específico que merece investigação: pode ter sido um produto de entrada que não gerou satisfação suficiente para uma segunda compra. Campeões apresentam alta variedade e volume de produtos — sinal de engajamento amplo com o portfólio, não dependência de uma categoria específica.
![Análise 1](img/5.png)

Uma observação em relação ao produto mais vendido, o segmento de "Novos Clientes" foi oque mais comprou materiais de escritório.

Já o segmento de "Clientes Perdidos" mais comprou foi um jarro de cerâmica, que seria interessante coletar o feedback sobre esse produto para medir a correlação por ter sido mais comprado por um segmento específico.
![Análise 1](img/6.png)

Já os "Clientes Campeões" possuem uma grande variedade e quantidade de produtos comprados, mostrando um forte engajamento com os produtos da empresa.

# RESULTADO/ RECOMENDAÇÃO

A análise RFM revelou que o principal problema da empresa não é falta de clientes — é falta de progressão entre segmentos.

**A base está concentrada no extremo errado:** Grande volume de Clientes Perdidos e baixo volume de Campeões e Fiéis indicam que o funil de retenção tem vazamento crítico nos estágios iniciais. Novos clientes não estão sendo convertidos em recorrentes com eficiência suficiente — e, sem intervenção estruturada, migram para Perdidos antes de gerar LTV relevante.

**O benchmark de Campeão é a maior entrega estratégica da análise:** Saber que um cliente precisa comprar a cada 11 dias, acima de 13 vezes, com ticket mínimo de R$ 590,00 transforma a segmentação em um sistema de gestão ativa da base — é possível monitorar quais clientes estão se aproximando ou se afastando desse perfil e agir antes que a janela se feche.

**O investimento de marketing precisa ser redistribuído por ROI esperado:** Campanhas para Campeões e Fiéis têm retorno comprovadamente superior ao investimento em reativação de Perdidos. Excluir Clientes Perdidos das listas de mídia paga e realocar esse orçamento para acelerar a progressão de Novos Clientes e segmentos de Atenção é a ação de maior impacto financeiro imediato identificada na análise.

# VISUALISE A ANALISE COMPLETA
https://lookerstudio.google.com/reporting/81e4d2bb-3685-4738-9f27-b87ead450ae3

# Próximos Passos

1. **Monitorar migração entre segmentos:** Acompanhar mensalmente a taxa com que clientes de segmentos inferiores progridem para Fiéis e Campeões — essa métrica é o principal indicador de eficácia das campanhas de retenção e deve se tornar KPI central do time de marketin
2. **Calcular ROI por segmento:** Mensurar o retorno de cada campanha separado por grupo RFM para confirmar a hipótese de que o investimento em Campeões e Fiéis supera o retorno de reativação de Perdidos — e usar esse dado para redistribuir o orçamento de mídia com base em evidência
3. **Estruturar régua de onboarding para Novos Clientes:** Criar sequência de comunicação com incentivo à segunda compra nos primeiros 30 dias — janela crítica onde a conversão para recorrência é mais barata e mais provável
4. **Investigar o produto dos Clientes Perdidos:** Coletar feedback sobre o jarro de cerâmica — produto concentrado no segmento de menor valor — para entender se há correlação entre a experiência com esse item e o abandono, e avaliar impacto no portfólio
5. **Refinar critérios RFM periodicamente:** Ajustar as pontuações de Recência, Frequência e Valor Monetário conforme o comportamento da base evolui — segmentações estáticas perdem precisão ao longo do tempo e devem ser recalibradas a cada ciclo de análise
