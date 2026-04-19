# 🚀 Planejamento de Infraestrutura – DevStore

📚 **Estudo de Caso I – Sistemas Operacionais**
👩‍💻 Disciplina: Sistemas Operacionais
👨‍🏫 Professor: Prof. Me. Deivison S. Takatu

---

## 📌 Visão Geral

A **DevStore** é uma startup focada no desenvolvimento de aplicações web que enfrenta desafios relacionados à organização, escalabilidade e segurança de sua infraestrutura de TI.

Atualmente, utiliza servidores locais sem padronização, o que dificulta a manutenção e o crescimento. Além disso, não há separação entre ambientes de desenvolvimento, testes e produção — aumentando riscos de falhas e inconsistências.

💡 Este projeto propõe uma solução moderna baseada em:

* Virtualização
* Containerização
* Computação em nuvem
* Boas práticas de segurança

---

## 🧩 Diagrama da Arquitetura

<p align="center">
  <img src="diagrama.png/diagrama.png" alt="Diagrama da Arquitetura DevStore" width="800"/>
</p>

---

## ⚠️ Problemas Identificados

* Falta de padronização dos servidores
* Dependência de infraestrutura local
* Ausência de ambientes separados (dev/teste/prod)
* Falta de testes automatizados
* Inexistência de integração contínua
* Vulnerabilidades de segurança

---

## 🎯 Objetivos

* ✅ Padronizar ambientes
* ✅ Melhorar a organização da infraestrutura
* ✅ Permitir escalabilidade sob demanda
* ✅ Reduzir custos operacionais
* ✅ Aumentar a segurança dos sistemas

---

## 🏗️ Arquitetura Proposta

A solução integra quatro pilares principais:

### 🔹 Virtualização

* Uso em ambientes de teste
* Maior isolamento entre sistemas

### 🔹 Containerização (Docker)

* Ambientes leves e padronizados
* Execução consistente em qualquer máquina

### 🔹 Computação em Nuvem

* Hospedagem em produção
* Alta disponibilidade e escalabilidade

### 🔹 Segurança

* Controle de acesso
* Firewall
* Monitoramento contínuo

---

## 📍 Estrutura da Arquitetura

* 👨‍💻 **Desenvolvimento:** containers locais padronizados
* 🧪 **Testes:** containers + máquinas virtuais
* ☁️ **Produção:** nuvem com alta disponibilidade
* ⚙️ **Gestão:** segurança, controle e monitoramento

---

## 💻 Papel dos Sistemas Operacionais

Os sistemas operacionais são responsáveis por:

* Gerenciar recursos de hardware
* Executar containers e máquinas virtuais
* Garantir segurança e estabilidade

💡 Destaque: uso de **Linux** pela eficiência e estabilidade

---

## 🔄 Fluxo de Trabalho

1. Desenvolvimento local com containers
2. Testes em ambientes isolados
3. Integração contínua
4. Deploy na nuvem
5. Monitoramento contínuo

---

## 📊 Monitoramento

Permite acompanhar:

* Uso de CPU
* Memória
* Armazenamento
* Desempenho geral

🔍 Ajuda a prevenir falhas e melhorar a performance

---

## 🌐 Rede e Armazenamento

* Redes virtuais seguras na nuvem
* Armazenamento escalável
* Controle de acesso aos dados

---

## ⚙️ Implementação

1. Migração para nuvem
2. Padronização com containers
3. Implementação de testes automatizados
4. Configuração de monitoramento

---

## 🔧 Manutenção e Expansão

* Monitoramento contínuo
* Atualizações frequentes
* Backups periódicos
* Escalabilidade conforme demanda

---

## 💰 Análise de Custos

| Critério             | Local       | Nuvem       |
| -------------------- | ----------- | ----------- |
| Investimento inicial | 🔴 Alto     | 🟢 Baixo    |
| Escalabilidade       | 🔴 Limitada | 🟢 Alta     |
| Manutenção           | 🔴 Interna  | 🟢 Provedor |
| Disponibilidade      | 🟡 Média    | 🟢 Alta     |

---

## ✅ Conclusão

A adoção de uma infraestrutura baseada em **containers + nuvem** permite que a DevStore:

* Cresça de forma sustentável 📈
* Reduza custos 💰
* Aumente a segurança 🔒
* Melhore a organização ⚙️

---

## 📚 Referências

* TANENBAUM, Andrew S. *Sistemas Operacionais Modernos*
* Documentação Docker
* Documentação AWS
* Documentação Microsoft Azure

---

✨ *Projeto acadêmico desenvolvido para estudo de infraestrutura em Sistemas Operacionais.*
