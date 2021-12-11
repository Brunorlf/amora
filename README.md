---
title: "Exercício Aula"
author: "Bruno Fernandes"
date: "`r Sys.Date()`"
output_dir: "."
output:
  prettydoc::html_pretty:
    theme: tactile
    highlight: github
---

## A New Output Format

> Minha frase importante

Lista:

1. Elemento 1
1. Elemento 2
1. Elemento 3

**Negrito**  *itálico* `html`

```{r dados}
library(tidyverse)
## Leitura dos dados
survey <- read_csv("dados/kaggle_survey_2021_responses.csv", 
                   locale = locale())

## Separação da primeira linha com a descr. da variável
descricao_survey <- survey %>% 
  slice(n = 1)

# Observações da base
survey_limpo <- survey %>% 
  slice(n = 2:n()) # n() total de linhas na base
```
