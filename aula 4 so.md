# 🖥️ Estrutura e Arquitetura de Sistemas Operacionais

<p align="center">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Disciplina-Sistemas%20Operacionais-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Atividade-Estrutura%20e%20Arquitetura-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Formato-Markdown-black?style=for-the-badge">
  <img src="https://img.shields.io/badge/GitHub-Repositório%20Acadêmico-181717?style=for-the-badge&logo=github">
</p>

---

## 📚 Informações Acadêmicas

- **Disciplina:** Sistemas Operacionais  
- **Tema:** Estrutura e Arquitetura de Sistemas Operacionais  
- **Professor:** Prof. Me. Deivison S. Takatu  
- **Instituição:** Fatec  

---

# 📌 Sobre a atividade

Esta atividade foi elaborada com base no conteúdo da aula **“Estrutura e Arquitetura de Sistemas Operacionais”**, com foco especial no conceito de **reaproveitamento da estrutura**.

Durante a aula, foi apresentado que diversos sistemas operacionais não são criados totalmente do zero. Em vez disso, muitos aproveitam a base de sistemas já existentes, reutilizando elementos como:

- **kernel**
- **arquitetura interna**
- **gerenciamento de processos**
- **gerenciamento de memória**
- **drivers**
- **sistema de arquivos**
- **estrutura de comunicação com hardware**

A proposta da atividade é pesquisar **5 sistemas operacionais derivados ou baseados em outros sistemas operacionais**, analisando as diferenças entre eles e o sistema que serviu como base para seu desenvolvimento.

---

# 🎯 Objetivo

Identificar cinco sistemas operacionais que foram desenvolvidos a partir de outro sistema operacional ou que utilizam sua base (kernel, arquitetura ou estrutura), elaborando uma **tabela comparativa** e uma **análise técnica** que evidencie:

- o sistema operacional derivado;
- o sistema base;
- os elementos reaproveitados;
- as diferenças estruturais e funcionais;
- a finalidade de uso de cada sistema.

---

# 📑 Sumário

- [🧠 Fundamentação Teórica](#-fundamentação-teórica)
- [⚙️ Componentes de um Sistema Operacional](#️-componentes-de-um-sistema-operacional)
- [🧩 Sistemas Operacionais Selecionados](#-sistemas-operacionais-selecionados)
- [📊 Tabela Comparativa](#-tabela-comparativa)
- [🔍 Análise Técnica Detalhada](#-análise-técnica-detalhada)
- [🖼️ Assets Visuais](#️-assets-visuais)
- [📈 Resultado da Pesquisa](#-resultado-da-pesquisa)
- [🧾 Conclusão](#-conclusão)
- [📚 Referências](#-referências)
- [🚀 Como subir no GitHub](#-como-subir-no-github)

---

# 🧠 Fundamentação Teórica

Na arquitetura de sistemas operacionais, o reaproveitamento de estruturas existentes é uma estratégia amplamente utilizada. Essa abordagem permite que novos sistemas sejam criados a partir de uma base consolidada, reduzindo o esforço de desenvolvimento e aumentando a confiabilidade do software.

As principais vantagens dessa prática incluem:

- **Redução de custos de desenvolvimento**
- **Maior estabilidade e segurança**
- **Reutilização de tecnologias maduras**
- **Compatibilidade com hardwares específicos**
- **Facilidade de manutenção**
- **Suporte contínuo e atualizações**

Durante a aula, foram apresentados exemplos claros desse conceito:

- **Raspberry Pi OS**, baseado em **Debian**
- **Orbis OS (PlayStation 4)**, baseado em **FreeBSD**

Esses exemplos demonstram como um sistema pode reutilizar uma base robusta e adaptá-la para atender necessidades específicas, como dispositivos embarcados ou consoles.

---

# ⚙️ Componentes de um Sistema Operacional

Com base no conteúdo estudado, um sistema operacional é composto por diversos elementos fundamentais. Entre os principais, destacam-se:

## 🔹 Kernel
É o núcleo do sistema operacional, responsável por gerenciar os recursos críticos do computador, como CPU, memória e dispositivos.

## 🔹 Gerenciamento de Processos
Controla a execução de programas, criação de processos, escalonamento e comunicação entre tarefas.

## 🔹 Gerenciamento de Memória
Responsável pela alocação, proteção e liberação de memória física e virtual.

## 🔹 Sistema de Arquivos
Organiza os dados em diretórios e arquivos, permitindo armazenamento, acesso e gerenciamento das informações.

## 🔹 Entrada e Saída (I/O)
Gerencia a comunicação entre o sistema operacional e os dispositivos externos, como teclado, mouse, impressora e rede.

## 🔹 Drivers de Dispositivos
São módulos que permitem a comunicação entre o sistema operacional e hardwares específicos.

> Esses componentes são essenciais para compreender como um sistema derivado pode reutilizar a estrutura de outro sistema operacional já existente.

---

# 🧩 Sistemas Operacionais Selecionados

Os sistemas operacionais escolhidos para esta atividade foram:

1. **Ubuntu**
2. **Linux Mint**
3. **Raspberry Pi OS**
4. **Orbis OS (PlayStation 4)**
5. **Android**

Esses sistemas foram selecionados por representarem diferentes contextos de uso:

- desktop
- produtividade
- educação
- sistemas embarcados
- consoles
- dispositivos móveis

---

# 📊 Tabela Comparativa

| Sistema Operacional Derivado | Sistema Base | Base reutilizada | Principais diferenças | Finalidade / Uso |
|---|---|---|---|---|
| **Ubuntu** | **Debian** | Estrutura do sistema, pacotes `.deb`, kernel Linux | O Ubuntu é mais voltado para usabilidade, interface amigável, atualizações regulares e suporte comercial. O Debian é mais conservador e prioriza estabilidade. | Desktop, servidores e ensino |
| **Linux Mint** | **Ubuntu** (indiretamente Debian) | Kernel Linux, repositórios, arquitetura e base de pacotes | O Linux Mint prioriza facilidade para iniciantes, interface tradicional e experiência pronta para uso. O Ubuntu possui maior adoção corporativa e integração com tecnologias da Canonical. | Desktop doméstico e produtividade |
| **Raspberry Pi OS** | **Debian** | Kernel Linux, sistema de pacotes, estrutura interna | O Raspberry Pi OS é otimizado para arquitetura ARM e placas Raspberry Pi. O Debian é mais genérico e atende múltiplas plataformas. | Educação, IoT, automação e embarcados |
| **Orbis OS (PlayStation 4)** | **FreeBSD** | Kernel e arquitetura do sistema | O Orbis OS é fechado, altamente customizado e voltado para desempenho gráfico e jogos. O FreeBSD é aberto e de propósito geral. | Consoles de videogame |
| **Android** | **Linux** | Kernel Linux | O Android utiliza o kernel Linux, mas constrói um ecossistema próprio para dispositivos móveis, com interface touch, apps e gerenciamento específico de energia e sensores. | Smartphones, tablets, smart TVs e dispositivos móveis |

---

# 🔍 Análise Técnica Detalhada

## 1️⃣ Ubuntu

### 📌 Sistema Base
**Debian**

### 🔧 Estruturas reaproveitadas
- Kernel Linux
- Sistema de pacotes `.deb`
- Repositórios
- Estrutura de diretórios
- Base de serviços do sistema

### 🆚 Diferenças principais
O Ubuntu foi projetado para oferecer uma experiência mais acessível ao usuário final. Seu foco está em:

- facilidade de instalação;
- interface amigável;
- atualizações previsíveis;
- suporte a usuários domésticos e corporativos;
- forte adoção em nuvem e servidores.

O Debian, por sua vez, é reconhecido por:

- extrema estabilidade;
- maior conservadorismo nas versões;
- forte aderência à filosofia do software livre;
- uso recorrente em servidores.

### ✅ Análise
O Ubuntu é um exemplo clássico de sistema derivado que reaproveita uma base estável (Debian), adaptando-a para uma experiência mais amigável e comercialmente viável.

---

## 2️⃣ Linux Mint

### 📌 Sistema Base
**Ubuntu** (com herança indireta do Debian)

### 🔧 Estruturas reaproveitadas
- Kernel Linux
- Base estrutural do Ubuntu
- Repositórios
- Compatibilidade de pacotes
- Serviços do sistema

### 🆚 Diferenças principais
O Linux Mint foi desenvolvido com foco em:

- simplicidade;
- experiência de desktop tradicional;
- menor curva de aprendizado;
- melhor experiência imediata para usuários iniciantes;
- recursos multimídia prontos para uso.

Comparado ao Ubuntu, o Linux Mint:
- oferece uma interface mais familiar;
- reduz mudanças bruscas na experiência do usuário;
- prioriza praticidade em vez de padronização corporativa.

### ✅ Análise
O Linux Mint demonstra como uma distribuição pode reutilizar uma base sólida e remodelar a experiência visual e funcional para atender um público específico.

---

## 3️⃣ Raspberry Pi OS

### 📌 Sistema Base
**Debian**

### 🔧 Estruturas reaproveitadas
- Kernel Linux
- Gerenciamento de pacotes
- Organização do sistema
- Estrutura de arquivos
- Serviços e processos básicos

### 🆚 Diferenças principais
O Raspberry Pi OS é otimizado para:

- arquitetura ARM;
- placas Raspberry Pi;
- baixo consumo de recursos;
- aplicações educacionais;
- automação;
- robótica;
- IoT.

O Debian:
- atende múltiplas arquiteturas;
- não é focado exclusivamente em placas embarcadas;
- é mais generalista.

### ✅ Análise
Esse é um dos exemplos mais alinhados com o conteúdo da aula, pois mostra claramente o **reaproveitamento da estrutura** para adaptação a um hardware específico.

---

## 4️⃣ Orbis OS (PlayStation 4)

### 📌 Sistema Base
**FreeBSD**

### 🔧 Estruturas reaproveitadas
- Base do kernel
- Arquitetura de sistema
- Gerenciamento interno de baixo nível
- Controle de recursos do hardware

### 🆚 Diferenças principais
O Orbis OS foi criado para:

- desempenho gráfico elevado;
- otimização para jogos;
- integração com hardware proprietário;
- execução multimídia;
- ambiente fechado e controlado.

Já o FreeBSD:
- é um sistema aberto;
- é voltado para múltiplos usos;
- é comum em servidores, redes e ambientes técnicos.

### ✅ Análise
O Orbis OS ilustra como uma base robusta pode ser adaptada de forma profunda para um ambiente altamente especializado, como um console de videogame.

---

## 5️⃣ Android

### 📌 Sistema Base
**Linux**

### 🔧 Estruturas reaproveitadas
- Kernel Linux
- Gerenciamento de memória
- Gerenciamento de processos
- Drivers
- Controle de hardware

### 🆚 Diferenças principais
Embora utilize o kernel Linux, o Android:

- não é uma distribuição Linux tradicional;
- possui ecossistema próprio;
- foi projetado para interface touch;
- possui framework específico para aplicativos móveis;
- faz gerenciamento otimizado de sensores, energia e permissões.

Em comparação, o Linux tradicional:
- é usado em desktops, servidores e embarcados;
- não é nativamente focado em smartphones;
- pode ter diferentes interfaces gráficas e modelos de uso.

### ✅ Análise
O Android é um excelente exemplo de reaproveitamento parcial: ele reutiliza a base central (kernel), mas constrói toda a camada superior de forma independente.

---
📈 Resultado da Pesquisa

A pesquisa realizada demonstra que o desenvolvimento de sistemas operacionais frequentemente ocorre por meio da adaptação de bases já consolidadas.

Essa prática permite:

    aproveitar kernels confiáveis;

    reduzir tempo de desenvolvimento;

    melhorar estabilidade;

    adaptar sistemas para hardwares específicos;

    criar plataformas especializadas com menor custo técnico.

Foi possível observar que essa estratégia está presente em diferentes categorias tecnológicas, como:

    distribuições Linux

    sistemas embarcados

    consoles de videogame

    dispositivos móveis

    ambientes educacionais

    
🧾 Conclusão

Conclui-se que o reaproveitamento da estrutura é uma prática essencial na evolução dos sistemas operacionais modernos.

Os sistemas analisados — Ubuntu, Linux Mint, Raspberry Pi OS, Orbis OS e Android — evidenciam que é possível reutilizar componentes fundamentais, como kernel, arquitetura e gerenciamento de recursos, para criar soluções altamente adaptadas a diferentes finalidades.

Essa abordagem é vantajosa porque:

    reduz custos;

    acelera o desenvolvimento;

    aumenta a estabilidade;

    facilita manutenção;

    melhora a compatibilidade com hardware.

Dessa forma, o conteúdo estudado em aula mostra-se diretamente aplicável à realidade tecnológica atual, onde a maioria dos sistemas modernos surge a partir da evolução e personalização de estruturas já existentes.

📚 Referências
Referências bibliográficas

    TANENBAUM, Andrew S.; BOS, Herbert. Sistemas Operacionais Modernos. 4. ed. São Paulo: Pearson, 2016.

    SILBERSCHATZ, Abraham; GALVIN, Peter B.; GAGNE, Greg. Fundamentos de Sistemas Operacionais. 9. ed. Rio de Janeiro: LTC, 2015.

    STALLINGS, William. Sistemas Operacionais: Conceitos e Projetos. 8. ed. São Paulo: Pearson, 2015.

    DENARDIN, G. W.; BARRIQUELLO, C. H. Sistemas Operacionais de Tempo Real e sua Aplicação em Sistemas Embarcados. Porto Alegre: Editora da UFRGS, 2014.

    DOWNEY, Allen B. Think OS: A Brief Introduction to Operating Systems. Green Tea Press, 2015.

Referências complementares

    Documentação oficial do Ubuntu

    Documentação oficial do Linux Mint

    Documentação oficial do Raspberry Pi OS

    Android Open Source Project (AOSP)

    Documentação técnica do FreeBSD
