# SAP — Simple As Possible Computer

Este diretório contém o projeto final da disciplina de Arquitetura de Computadores I:  
o **SAP (Simple As Possible Computer)**.

O SAP é um modelo didático de computador extremamente simplificado, criado para demonstrar de forma prática como uma CPU funciona internamente.

Seu objetivo não é desempenho, mas sim **compreensão estrutural**.

---

# 🧠 O Que é o SAP?

O SAP é um computador educacional baseado em:

- Arquitetura simples
- Conjunto mínimo de instruções
- Barramento único
- Unidade de controle baseada em estados

Ele permite visualizar claramente:

- O ciclo de busca (fetch)
- O ciclo de execução (execute)
- O fluxo de dados no barramento
- A interação entre registradores, ULA e memória

---

# 🏗️ Estrutura do SAP

## 1️⃣ Barramento

- Responsável por transportar dados entre os componentes
- Geralmente implementado como barramento de 8 bits
- Apenas um componente pode escrever no barramento por vez

---

## 2️⃣ Registradores

### 🔹 Registrador A (Acumulador)
- Armazena dados para operações na ULA
- Principal registrador de cálculo

### 🔹 Registrador B
- Armazena o segundo operando para a ULA

### 🔹 Program Counter (PC)
- Armazena o endereço da próxima instrução

### 🔹 Instruction Register (IR)
- Armazena a instrução atual

### 🔹 Memory Address Register (MAR)
- Armazena o endereço da memória a ser acessado

---

## 3️⃣ Memória

- Armazena dados e instruções
- Organizada por endereços
- No SAP clássico, geralmente pequena (ex: 16 bytes)

---

## 4️⃣ Unidade Aritmética e Lógica (ULA)

Responsável por realizar:

- Soma
- Subtração

A ULA opera principalmente com os dados dos registradores A e B.

---

## 5️⃣ Unidade de Controle

Responsável por:

- Gerar sinais de controle
- Coordenar a ativação dos componentes
- Controlar o ciclo de execução

Baseada em:

- Contador de etapas (microetapas)
- Máquina de estados

---

# 🔄 Ciclo de Instrução

O SAP executa instruções seguindo etapas bem definidas:

## 1️⃣ Fetch (Busca)
1. O PC envia o endereço ao MAR
2. A memória envia a instrução ao IR
3. O PC é incrementado

## 2️⃣ Decode (Decodificação)
- A instrução é interpretada
- Sinais de controle são preparados

## 3️⃣ Execute (Execução)
- Operação é realizada (ex: soma, carga, saída)

Esse processo se repete continuamente.

---

# 📜 Conjunto Básico de Instruções

Exemplos típicos:

- LDA (Load Accumulator)
- ADD
- SUB
- OUT
- HLT

Cada instrução ativa um conjunto específico de sinais de controle.

---

# 🔧 Nossa Modificação: Identificador de Número Par ou Ímpar

Além da implementação padrão do SAP, adicionamos uma modificação funcional:

## 🎯 Objetivo

Criar um mecanismo capaz de identificar se o valor presente no acumulador é:

- Par
- Ímpar

---

## 💡 Conceito Utilizado

A identificação foi baseada em uma propriedade fundamental do sistema binário:

> Um número é **par** quando seu bit menos significativo (LSB) é 0.  
> Um número é **ímpar** quando seu bit menos significativo (LSB) é 1.

---

## 🛠️ Implementação

- Extraímos o bit menos significativo do acumulador
- Utilizamos lógica combinacional para:
  - Acionar um sinal indicador de número par
  - Acionar um sinal indicador de número ímpar

Possível implementação:
- Uso direto do LSB
- OU
- Aplicação de porta lógica NOT para gerar sinal complementar

---

## 📌 Impacto da Modificação

Essa alteração demonstrou na prática:

- Aplicação de portas lógicas em nível de sistema
- Extensão funcional de uma arquitetura existente
- Integração entre lógica combinacional e arquitetura sequencial
- Personalização de uma CPU simples

---

# 🧩 Conceitos Aplicados no Projeto

O SAP integrou diversos conteúdos da disciplina:

- Álgebra Booleana
- Mapas de Karnaugh
- Somadores completos
- Complemento de 2
- Flip-flops
- Contadores síncronos
- Máquina de estados finitos
- Organização de memória
- Barramentos

---

# 🎓 Conclusão

O SAP foi essencial para compreender que um computador não é uma “caixa mágica”, mas sim:

- Um conjunto organizado de registradores
- Circuitos combinacionais
- Circuitos sequenciais
- Sinais de controle
- Fluxo estruturado de dados

A modificação de identificação de par/ímpar reforçou a compreensão de como pequenas alterações na lógica podem expandir funcionalidades de uma arquitetura.

---
