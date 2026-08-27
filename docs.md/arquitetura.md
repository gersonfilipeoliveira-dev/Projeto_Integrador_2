arquitetura
# Modelagem da Solução - Sistema de Seleção de Esportes

## 1. Fluxograma do Usuário (Aluno)
Este diagrama ilustra o passo a passo do aluno, desde a entrada no sistema até a confirmação do voto nos jogos escolares.

```mermaid
graph TD
    A[Acesso ao Sistema] --> B{Login com Matrícula}
    B -- Inválido --> C[Exibir Erro: Matrícula não encontrada]
    B -- Válido --> D{Aluno já votou?}
    D -- Sim --> E[Redirecionar para Painel de Resultados Parciais]
    D -- Não --> F[Exibir Lista de Esportes: Futsal, Vôlei, Queimada, Handebol, etc.]
    F --> G[Aluno Seleciona Esporte de Preferência]
    G --> H[Confirmar Votação]
    H --> I[(Banco de Dados: Computar Voto)]
    I --> J[Tela de Sucesso / Agradecimento]
    J --> E

    2. Estrutura Básica de Dados
Tabela Aluno: ID_Aluno, Matricula, Nome, Voto_Realizado (Boolean)

Tabela Esportes: ID_Esporte, Nome_Esporte, Total_Votos
Com este planejamento de cartões e o código do diagrama acima, você cobre a modelagem inicial da solução e o fatiamento do trabalho exigidos nesta fase
