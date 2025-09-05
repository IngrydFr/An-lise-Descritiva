```r
## Respostas do formulãrio de feedback

#questão 1
dados_1 <- data.frame(
  Resposta = factor(c("Discordo Completamente", "Discordo", "Neutro", "Concordo", "Concordo Completamente"),
                    levels = c("Discordo Completamente", "Discordo", "Neutro", "Concordo", 
                               "Concordo Completamente")),
  Quantidade = c(0, 2, 3, 16, 31)
)

#questão 2
dados_2 <- data.frame(
  Resposta = factor(c("Discordo Completamente", "Discordo", "Neutro", "Concordo", "Concordo Completamente"),
                    levels = c("Discordo Completamente", "Discordo", "Neutro", "Concordo", 
                               "Concordo Completamente")),
  Quantidade = c(0, 1, 6, 17, 27)
)

#questão 3
dados_3 <- data.frame(
  Resposta = factor(c("Discordo Completamente", "Discordo", "Neutro", "Concordo", "Concordo Completamente"),
                    levels = c("Discordo Completamente", "Discordo", "Neutro", "Concordo", 
                               "Concordo Completamente")),
  Quantidade = c(0, 0, 2, 7, 44)
)

#total de questões
dados_t <- data.frame(
  Resposta = factor(c("Discordo Completamente", "Discordo", "Neutro", "Concordo", "Concordo Completamente"),
                    levels = c("Discordo Completamente", "Discordo", "Neutro", "Concordo", 
                               "Concordo Completamente")),
  Quantidade = c(0, 3, 11, 40, 102)
)



#chamando o pacote de graficos
library(ggplot2) #chamando o pacote



#gráfico questão 1
ggplot(dados_1, aes(x = Resposta, y = Quantidade, fill = Resposta)) +
  geom_bar(stat = "identity") +
  geom_text(aes(label = Quantidade), vjust = -0.5, size = 4) +
  labs(
    title = "Distribuição de Respostas",
    x = "Categorias de Resposta", 
    y = "Número de Respostas"
  ) +
  scale_fill_manual(values = c("#FA8072", "#A52A2A", "#B22222", "#8B0000", "#800000")) +
  theme(panel.background = element_rect(fill = "#DCDCDC"))

#gráfico da questão 2
ggplot(dados_2, aes(x = Resposta, y = Quantidade, fill = Resposta)) +
  geom_bar(stat = "identity") +
  geom_text(aes(label = Quantidade), vjust = -0.5, size = 4) +
  labs(
    title = "Distribuição de Respostas",
    x = "Categorias de Resposta",
    y = "Número de Respostas"
  ) +
  scale_fill_manual(values = c("#FA8072", "#A52A2A", "#B22222", "#8B0000", "#800000")) +
  theme(panel.background = element_rect(fill = "#DCDCDC"))

#gráfico da questão 3
ggplot(dados_3, aes(x = Resposta, y = Quantidade, fill = Resposta)) +
  geom_bar(stat = "identity") +
  geom_text(aes(label = Quantidade), vjust = -0.5, size = 4) +
  labs(
    title = "Distribuição de Respostas",
    x = "Categorias de Resposta",
    y = "Número de Respostas"
  ) +
  scale_fill_manual(values = c("#FA8072", "#A52A2A", "#B22222", "#8B0000", "#800000")) +
  theme(panel.background = element_rect(fill = "#DCDCDC"))

#gráfico total
ggplot(dados_t, aes(x = Resposta, y = Quantidade, fill = Resposta)) +
  geom_bar(stat = "identity") +
  geom_text(aes(label = Quantidade), vjust = -0.5, size = 4) +
  labs(
    title = "Distribuição de Respostas",
    x = "Categorias de Resposta",
    y = "Número de Respostas"
  ) +


  scale_fill_manual(values = c("#0000FF", "#0000CD", "#00008B", "#000080", "#191970")) +
  theme(panel.background = element_rect(fill = "#DCDCDC"))
