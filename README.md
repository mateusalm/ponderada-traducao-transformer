# Uso de transformers para tradução de texto

## Vantagens

- Paralelismo: ao contrário de redes neurais recorrentes (RNNs), os Transformers processam as sequências em paralelo, tornando-os mais rápidos em hardware moderno.
- Atenção a contextos distantes: capturam dependências de longo alcance melhor que modelos sequenciais como RNNs ou redes neurais convolucionais.
- Escalabilidade: Transformers podem ser escalados para grandes volumes de dados e tarefas complexas.

## Desvantagens:

- Alto custo computacional: treinar transformers requer muito poder de processamento, especialmente em grandes modelos.
- Dados extensivos: precisam de grandes quantidades de dados para funcionar bem.
- Overfitting: alto risco, principalmente quando se trata de datasets pequenos.

## Modificações no notebook

Um ponto chave da redução de complexidade foi a limitação do número máximo de tokens processados por frase, ddefinido em MAX_TOKENS=128. A tokenização é feita de maneira similar, mas a versão rodada otimiza o uso da memória ao focar diretamente na conversão dos dados para tensor, reduzindo o processamento excessivo de dados além dos limites necessários para a tarefa.

O código para preparação de batches de dados foi simplificado, removendo redundâncias. Após ajustes, foi feito uso de funções mais diretas para a tokenização e conversão em tensores, que também contribuiu para a redução do tempo de processamento.
