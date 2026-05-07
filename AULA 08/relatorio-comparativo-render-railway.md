<div align="center">
  <h1>📊 Relatório Comparativo: Render vs. Railway</h1>
  <p><i>Análise de infraestrutura de nuvem, abstração de hardware e Sistema Operacional</i></p>

  ![NodeJS](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
  ![Render](https://img.shields.io/badge/Render-%2346E3B7.svg?style=for-the-badge&logo=render&logoColor=white)
  ![Railway](https://img.shields.io/badge/Railway-%23131415.svg?style=for-the-badge&logo=railway&logoColor=white)
</div>

<br>

> **Projeto:** Cloud OS Dashboard & Kernel Simulator  
> **Disciplina:** Nuvem e Sistemas Operacionais  
> **Instituição:** FATEC Itapetininga  
> **Aluna:** Marcelle de Góes Silva  
> **Professor:** Prof. Me. Deivison S. Takatu  

---

# 📑 Relatório Comparativo — Render vs Railway

---

# 1. 🎯 Objetivo do Relatório

Este relatório tem como objetivo comparar a execução da mesma aplicação em duas plataformas de hospedagem em nuvem:

- Render
- Railway

A aplicação utilizada para a comparação foi um dashboard desenvolvido com **Node.js** e **Express.js**, capaz de exibir informações do ambiente de execução, como:

- Sistema operacional
- Memória RAM
- CPU
- Rede
- Arquivos do projeto
- Variáveis básicas de ambiente
- Status da aplicação

A proposta da comparação é observar como a mesma aplicação se comporta em servidores diferentes, analisando:

- Características do ambiente
- Facilidade de deploy
- Configuração
- Recursos disponíveis
- Diferenças percebidas durante a execução

---

# 2. 🛠️ Tecnologias Utilizadas no Projeto

- **Node.js** — ambiente de execução JavaScript no servidor
- **Express.js** — framework utilizado para criar o servidor web e as rotas da aplicação
- **HTML, CSS e JavaScript** — utilizados para construir a interface visual do dashboard
- **Módulo `os` do Node.js** — utilizado para coletar informações do sistema operacional
- **Módulo `fs` do Node.js** — utilizado para listar arquivos do projeto
- **Render** — primeira plataforma de hospedagem em nuvem analisada
- **Railway** — segunda plataforma de hospedagem em nuvem analisada
- **GitHub** — utilizado como repositório do projeto e base para deploy

---

# 3. ☁️ Ambientes Analisados

---

# 3.1 Render

No Render, a aplicação foi executada como um serviço web Node.js.

O dashboard identificou o ambiente como:

```plaintext
Render
```

## Principais informações observadas

| Item | Valor observado |
|---|---|
| Plataforma detectada | Render |
| Sistema operacional | Linux |
| Usuário do sistema | render |
| Diretório home | /opt/render |
| Porta utilizada | 10000 |
| NODE_ENV | production |
| IP principal | 10.30.221.226 |
| Memória RAM total | Aproximadamente 30.65 GB |
| Memória RAM em uso | Aproximadamente 10.29 GB |
| CPU média | *(Inserir valor observado)* |
| Núcleos detectados | 8 |
| Modelo da CPU | AMD EPYC 7R13 Processor|
| Kernel / Release | 6.8.0-1052-aws |
| Versão do Node.js | v24.14.1 |
| Status | Online |

## Observações Técnicas

A presença do termo:

```plaintext
aws
```

no Kernel Linux (caso observado) indica que a infraestrutura utilizada pelo Render pode estar baseada em ambiente cloud sobre AWS ou infraestrutura compatível.

Além disso:

- O usuário `render`
- O diretório `/opt/render`
- A porta dinâmica

demonstram que o ambiente é padronizado e gerenciado pela plataforma.

---

# 3.2 Railway

No Railway, a mesma aplicação foi executada também como serviço web Node.js.

O dashboard identificou o ambiente como:

```plaintext
Railway
```

## Principais informações observadas

| Item | Valor observado |
|---|---|
| Plataforma detectada | Railway |
| Sistema operacional | Linux |
| Usuário do sistema | root |
| Diretório home | /app |
| Porta utilizada | 8080 |
| NODE_ENV | production |
| IP principal | 10.132.152.154 |
| Memória RAM total | Aproximadamente 384.22 GB |
| Memória RAM em uso | Aproximadamente 276.75 GB|
| CPU média | Load Average próximo a 13.01 |
| Núcleos detectados | 48 |
| Modelo da CPU | Intel Xeon Processor (Icelake) |
| Kernel / Release | 6.12.22+bpo-cloud-amd64 |
| Versão do Node.js | v22.22.2 |
| Status | Online |

## Observações Técnicas

O Railway apresentou:

- Grande quantidade de núcleos detectados
- Alta disponibilidade aparente de memória RAM

Isso não significa necessariamente que todos esses recursos estejam dedicados exclusivamente à aplicação.

Em plataformas cloud modernas, é comum:

- Compartilhamento de hardware
- Virtualização
- Containers compartilhando o mesmo host físico

---

# 4. ⚡ Comparação Direta entre Render e Railway

| Critério | Render | Railway |
|---|---|---|
| Tipo de plataforma | Plataforma cloud para aplicações web e APIs | Plataforma cloud para aplicações e projetos completos |
| Facilidade de deploy | Simples | Muito simples |
| Ambiente detectado | Render | Railway |
| Sistema operacional | Linux | Linux |
| Usuário do processo | render | root |
| Diretório padrão | /opt/render/app | /app |
| CPU detectada | CPU compartilhada | 48 núcleos lógicos |
| Memória total aparente | 30.65 GB | ~384 GB |
| NODE_ENV | production | production |
| Interface da plataforma | Tradicional e guiada | Moderna e centrada em projetos |
| Organização | Serviços separados | Projeto centralizado |
| Configuração de variáveis | Via painel | Via painel integrado |
| Melhor característica observada | Ambiente previsível e didático | Infraestrutura robusta e rápida |

---

# 5. 🧠 Principais Diferenças Técnicas Observadas

---

# 5.1 Porta de Execução

Cada ambiente utiliza portas diferentes.

Por isso, aplicações Node.js devem utilizar:

```javascript
const PORT = process.env.PORT || 3001;
```

Dessa forma, a aplicação consegue funcionar corretamente:

- Localmente
- No Render
- No Railway

---

# 5.2 Usuário do Sistema

Cada plataforma prepara o ambiente de execução de forma diferente.

Exemplos observados:

| Plataforma | Usuário |
|---|---|
| Render | render |
| Railway | root |

Em aplicações simples isso não altera o funcionamento, porém em sistemas maiores pode impactar:

- Segurança
- Permissões
- Acesso a arquivos
- Diretórios temporários

---

# 5.3 Diretórios do Ambiente

Os caminhos internos variam entre plataformas.

Boas práticas recomendadas:

```javascript
process.cwd()
path.join()
```

Evitar caminhos absolutos fixos torna a aplicação mais portátil.

---

# 5.4 Recursos de CPU, Memória e OOM (Out of Memory)

## Render

O Render apresentou:

- Aproximadamente 30.65 GB de RAM
- AMD EPYC 7R13 Processor

Com recursos limitados:

- O Garbage Collector atua com mais frequência
- Picos de uso podem acionar o:
  
```plaintext
OOM Killer
```

do Kernel Linux.

Isso pode derrubar o processo da aplicação.

---

## Railway

O Railway apresentou:

- Grande quantidade de RAM aparente
- Alto número de núcleos lógicos

Nesse cenário:

- O processo possui maior liberdade de alocação
- Menor risco de encerramento por falta de memória
- Ambiente mais próximo de servidores robustos de produção

Mesmo assim, os recursos exibidos não necessariamente pertencem exclusivamente ao container da aplicação.

---

# 5.5 Virtualização e Hibernação (Idle Timeout)

## Render

O Render aplica política agressiva de economia de recursos no plano gratuito.

Quando a aplicação fica sem tráfego:

- O container entra em suspensão
- O uptime é reiniciado
- Ocorre um:
  
```plaintext
Cold Start
```

na próxima requisição.

---

## Railway

O Railway manteve o processo executando continuamente.

O comportamento observado foi semelhante a um:

```plaintext
Daemon persistente
```

com menos interrupções.

---

# 6. 🎯 Diferenças entre as Ferramentas

---

# Render

O Render é uma plataforma bastante direta para:

- APIs
- Aplicações web
- Serviços
- Bancos de dados
- Jobs agendados

## Pontos positivos

- Deploy simples via GitHub
- HTTPS automático
- Boa organização dos serviços
- Ambiente didático
- Fácil para iniciantes
- Excelente para projetos acadêmicos

## Pontos de atenção

- Limitações severas no plano gratuito
- Idle Timeout
- Cold Starts frequentes

---

# Railway

O Railway possui abordagem mais moderna baseada em projetos integrados.

## Pontos positivos

- Deploy extremamente rápido
- Interface moderna
- Boa organização por projeto
- Integração forte entre serviços
- Infraestrutura aparentemente robusta
- Excelente para microsserviços

## Pontos de atenção

- Recursos aparentes muito elevados podem não ser totalmente dedicados
- Parte dos recursos pertence ao host compartilhado

---

# 7. 🚀 Qual Plataforma Foi Melhor para Este Projeto?

As duas plataformas atenderam muito bem aos objetivos da disciplina.

## Render

O Render se destacou como ambiente mais didático:

- Restrições de memória
- CPU limitada
- Hibernação
- Ambiente controlado

Essas características ajudam no estudo de:

- Gerenciamento de memória
- Ciclo de vida de processos
- Limitações do Kernel
- Containers compartilhados

---

## Railway

O Railway apresentou:

- Melhor desempenho bruto
- Persistência de processos
- Maior flexibilidade
- Melhor infraestrutura aparente

Ele se mostrou mais adequado para:

- Escalabilidade futura
- Microsserviços
- Aplicações maiores
- Ambientes mais próximos de produção

---

# 8. 🏁 Conclusão

A comparação entre Render e Railway demonstrou como plataformas cloud diferentes apresentam comportamentos distintos mesmo executando exatamente a mesma aplicação Node.js.

A principal conclusão é que:

- O módulo `os` do Node.js expõe instantaneamente características reais da infraestrutura subjacente
- Ambientes virtualizados possuem políticas diferentes de gerenciamento de CPU, memória e processos
- Aplicações preparadas para cloud devem evitar configurações fixas

Além disso, o projeto demonstrou na prática conceitos fundamentais de:

- Virtualização
- Containers
- Escalonamento
- Memória
- Processos
- Abstração de hardware
- Gerenciamento de recursos pelo Kernel Linux

Assim, o objetivo acadêmico foi plenamente alcançado, permitindo analisar de forma prática o comportamento de aplicações Node.js em diferentes ambientes de computação em nuvem.
