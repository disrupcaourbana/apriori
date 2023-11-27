# Carregar as bibliotecas necessárias
library(arules)

# Carregar o conjunto de dados a partir do arquivo CSV (substitua o nome do arquivo e o separador conforme necessário)
dados <- read.csv("NOMEDOARQUIVO.csv", header = TRUE, sep = ",")

# Converter o conjunto de dados em um formato de transações
transacoes <- as(dados, "transactions")

# Definir os parâmetros do algoritmo Apriori
parametros <- list(
  supp = 0.005,     # Suporte mínimo (ajuste conforme necessário)
  conf = 0.8,       # Confiança mínima (ajuste conforme necessário)
  minlen = 2        # Comprimento mínimo das regras (ajuste conforme necessário)
)

# Executar o algoritmo Apriori
regras <- apriori(transacoes, parameter = parametros)

# Exibir as regras de associação resultantes
inspect(regras)

# Salvar as regras de associação em um arquivo CSV
write(regras, file = "regras_associacao_resultados.csv")

# Salvar as regras de associação em um arquivo CSV com tabulações
write(regras, file = "regras_associacao.tsv", sep = "\t")
