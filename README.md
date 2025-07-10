# 🛠️  Esquema conceitual para o contexto de oficina mecânica

Este projeto apresenta o **esquema conceitual e lógico** de um sistema de controle e gerenciamento de execução de **ordens de serviço (OS)** para uma oficina mecânica. O modelo foi desenvolvido com base em uma narrativa descritiva, abordando desde o recebimento de veículos até a execução e registro de serviços e peças.

---

## 📘 Contexto

Clientes levam veículos à oficina mecânica para manutenção corretiva ou revisões periódicas. Cada veículo é avaliado por uma **equipe de mecânicos**, que identifica os serviços necessários, consulta uma tabela de mão de obra, estima o custo total (incluindo peças), e preenche uma **Ordem de Serviço (OS)**. Os serviços são realizados mediante autorização do cliente.

---

## 🎯 Objetivo

Criar um **esquema conceitual** de banco de dados relacional para suportar o fluxo de trabalho de uma oficina, garantindo:
- Registro de clientes, veículos e mecânicos
- Acompanhamento de ordens de serviço
- Controle de peças e mão de obra

---

## 🧱 Estrutura do Modelo

O modelo foi elaborado em **modelo EER (Entidade-Relacionamento Estendido)**, incluindo:

### Principais Entidades:
- **Cliente**: dados cadastrais
- **Veículo**: vinculado a um cliente
- **Mecânico**: com especialidade
- **Equipe**: composta por mecânicos
- **Ordem de Serviço (OS)**: principal ponto de controle
- **Serviço**: catálogo de serviços disponíveis
- **Serviço Executado**: ligação entre OS e o serviço prestado
- **Revisão**: tipos de revisão dentro de uma OS
- **Peça**: catálogo de peças
- **Peça Utilizada**: peças utilizadas em uma OS
- **Tabela de Mão de Obra**: referência de preços

### Principais Relacionamentos:
- Um cliente possui vários veículos
- Cada veículo gera múltiplas ordens de serviço
- Cada OS é atribuída a uma equipe
- Mecânicos participam de várias equipes
- Cada OS possui múltiplos serviços executados e revisões
- Cada serviço executado pode usar um tipo cadastrado
- Cada OS pode usar várias peças

---

## 🗂️ Arquivos do Projeto

- `Esquema Conceitual Oficina Mecânica.png`: diagrama conceitual com cardinalidades
- `readme.md`: documentação do projeto


---

## 💡 Tecnologias Utilizadas

- Ferramenta de modelagem: [MySQL Workbench]
- SQL padrão para modelagem relacional

---

## 📊 Exemplo de Caso de Uso

1. Cliente leva um veículo para revisão.
2. Equipe é designada e avalia o serviço.
3. Ordem de Serviço é criada com previsão de entrega.
4. Sistema calcula os valores com base em serviços e peças.
5. Cliente autoriza a execução.
6. Serviço é realizado e OS finalizada.

---

## 🧑‍💻 Autor

**Luis Fernando Sosnoski de Souza**  
[](https://github.com/lfssouza)]  
Curso: SQL Database Specialist
