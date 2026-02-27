# Arquitetura de Computadores I (AC1)

Este repositório reúne os conteúdos estudados na disciplina **Arquitetura de Computadores I**, abordando os fundamentos matemáticos, lógicos e estruturais que sustentam o funcionamento de sistemas computacionais.

## 📂 Estrutura do Repositório

- 📄 `Anotacoes-AC1.pdf` → PDF com anotações importantes do meu caderno  
- 💻 `SAP/` → Projeto final: Simple As Possible Computer  
- 📘 Este README → Resumo dos conteúdos estudados  

---

# 📚 Conteúdo Estudado

---

## 1. Sistemas de Numeração

### 🔢 Sistema Decimal (Base 10)
- Utiliza os dígitos de 0 a 9  
- Sistema posicional  
- Base natural utilizada pelos humanos  

### 💻 Sistema Binário (Base 2)
- Utiliza apenas 0 e 1  
- Base fundamental dos sistemas digitais  
- Representação por bits  

### 🔡 Sistema Hexadecimal (Base 16)
- Dígitos: 0–9 e A–F  
- Facilita a leitura de grandes sequências binárias  
- Conversão direta agrupando 4 bits  

### 🔁 Conversões
- Decimal → Binário (divisões sucessivas por 2)  
- Binário → Decimal (soma das potências de 2)  
- Binário ↔ Hexadecimal (agrupamento de 4 bits)  
- Decimal ↔ Hexadecimal  

---

## 2. Representação de Números no Computador

### 📌 Sinal, Expoente e Mantissa
- Base da representação em ponto flutuante  
- Estrutura composta por:
  - Bit de sinal  
  - Expoente  
  - Mantissa  
- Introdução ao padrão IEEE 754  

### 🔢 Complemento de 2
- Método para representar números negativos  
- Processo:
  1. Inverter todos os bits  
  2. Somar 1  
- Permite realizar subtração usando circuitos de soma  

### 🔡 Decimal Codificado em Binário (BCD)
- Cada dígito decimal é representado por 4 bits  
- Muito utilizado em sistemas financeiros  

### 🔄 Código de Gray
- Apenas 1 bit varia entre números consecutivos  
- Reduz erros em sistemas digitais  

---

## 3. Portas Lógicas

Base de todos os circuitos digitais.

### Operações Fundamentais
- AND  
- OR  
- NOT  

### Operações Derivadas
- XOR  
- XNOR  
- NAND  
- NOR  

**Observação:**  
As portas **NAND** e **NOR** são universais, ou seja, é possível implementar qualquer circuito lógico utilizando apenas uma delas.

---

## 4. Álgebra Booleana

Ferramenta matemática para simplificação de expressões lógicas.

### 📐 Propriedades Fundamentais
- Idempotência  
- Comutatividade  
- Associatividade  
- Distributividade  
- Elemento neutro  
- Complementaridade  
- Dupla negação  

### 🧠 Teoremas de Uma Variável
- A + A = A  
- A · A = A  
- A + A' = 1  
- A · A' = 0  

---

## 5. Mapas de Karnaugh

- Método visual para simplificação de funções booleanas  
- Reduz o número de portas lógicas necessárias  
- Agrupamentos devem ser feitos em potências de 2  
- Aplicável para 2, 3 e 4 variáveis  

---

## 6. Circuitos Combinacionais

### ➕ Somador Completo (Full Adder)
- Soma dois bits e um carry-in  
- Produz:
  - Soma  
  - Carry-out  

### 🔢 Somador de 4 Bits
- Conjunto de 4 full adders encadeados  
- Base para unidades aritméticas  

### 🔀 Multiplexador (MUX)
- Seleciona uma entrada entre várias  
- Controlado por bits de seleção  

### 🔁 Demultiplexador (DEMUX)
- Direciona uma entrada para uma das saídas possíveis  

### 🔢 Codificador
- Converte múltiplas entradas em um código binário  

### 🔓 Decodificador
- Converte código binário em múltiplas saídas  

---

## 7. Circuitos Sequenciais

Dependem do estado anterior (possuem memória).

### 🔒 Latch
- Armazena 1 bit  
- Sensível ao nível do sinal  

### 🔁 Flip-Flops
- Armazenam 1 bit  
- Sensíveis à borda do clock  
- Tipos estudados:
  - SR  
  - JK  
  - D  
  - T  

### ⏱️ Contadores

#### Assíncronos (Ripple)
- Mudança em cascata  
- Mais simples  
- Mais lentos  

#### Síncronos
- Compartilham o mesmo clock  
- Mais rápidos  
- Mais estáveis  

---

## 8. Máquinas de Estados Finitos (FSM)

- Modelo matemático de sistemas sequenciais  
- Composto por:
  - Estados  
  - Entradas  
  - Transições  
  - Saídas  

Tipos:
- Máquina de Moore  
- Máquina de Mealy  

---

## 9. Conceitos Básicos de Memória

- Bits organizados em palavras  
- Endereçamento de memória  
- Conceito de leitura e escrita  
- Introdução a registradores e memória RAM  

---

## 10. Projeto Final — SAP (Simple As Possible Computer)

O SAP (Simple As Possible Computer) foi o projeto final da disciplina.

Objetivo:  
Construir um computador didático simples para compreender o funcionamento interno de uma CPU.

### Componentes Principais:
- Registradores  
- Unidade Aritmética e Lógica (ULA)  
- Barramento  
- Memória  
- Unidade de Controle  

### Conceitos Aplicados:
- Execução de instruções  
- Ciclo de busca (fetch)  
- Ciclo de execução (execute)  
- Controle por sinais  

O projeto integrou todos os conceitos estudados ao longo da disciplina, permitindo visualizar na prática como um computador realmente funciona internamente.

---

# 🎯 Objetivo da Disciplina

Compreender como a informação é representada, processada e armazenada em sistemas digitais, construindo a base necessária para disciplinas futuras como:

- Organização de Computadores  
- Sistemas Operacionais  
- Arquitetura Avançada  
- Microprocessadores  

---
