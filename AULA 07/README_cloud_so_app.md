# Cloud SO App

## Links do Projeto

- **Repositório no GitHub:**  
  https://github.com/marcellegg/cloud-so-app

- **Aplicação publicada no Render:**  
  https://cloud-so-app-1.onrender.com

---

# Teste Online no Render

A aplicação está disponível online no seguinte endereço:

https://cloud-so-app-1.onrender.com

---

# Imagem do Teste Localhost

<p align="center">
  <img src="testelocal.png" width="800"/>
  <br>
  <em>Legenda: Captura de tela do Dashboard em ambiente local (Porta 3001).</em>
</p>

---

# 1. Introdução

Este manual documenta o desenvolvimento da atividade prática da disciplina de **Nuvem e Sistemas Operacionais**.

A proposta da atividade foi criar uma aplicação web utilizando **Node.js** e **Express.js**, capaz de exibir informações do sistema operacional por meio do módulo nativo `os` do Node.js.

A aplicação foi testada em ambiente local e posteriormente publicada em ambiente de nuvem utilizando a plataforma **Render**.

O objetivo principal foi comparar a execução local com a execução em nuvem, observando diferenças relacionadas ao sistema operacional, hostname, CPU, memória e tempo de atividade do sistema.

---

# 2. Objetivo da Atividade

O objetivo da atividade foi desenvolver uma aplicação chamada `cloud-so-app`, que exibe informações do sistema operacional, como:

- Nome do host;
- Plataforma do sistema operacional;
- Arquitetura do processador;
- Quantidade de CPUs;
- Modelo da CPU;
- Memória total;
- Memória livre;
- Tempo de atividade do sistema.

Além disso, a atividade também teve como objetivo publicar a aplicação em ambiente de nuvem utilizando o Render e comparar os dados exibidos no ambiente local com os dados exibidos no ambiente cloud.

---

# 3. Tecnologias Utilizadas

As tecnologias utilizadas no projeto foram:

- **Node.js** — ambiente de execução JavaScript no backend;
- **Express.js** — framework utilizado para criação do servidor web;
- **CORS** — mecanismo de segurança que controla acesso entre domínios diferentes no navegador;
- **HTML** — estrutura da página exibida ao usuário;
- **CSS / JavaScript** — estilização visual e lógica do frontend;
- **Git** — ferramenta de controle de versão;
- **GitHub** — plataforma utilizada para hospedar o código-fonte;
- **Render** — plataforma utilizada para publicar a aplicação em nuvem;
- **PowerShell / CMD** — terminal utilizado para execução dos comandos no Windows.

---

# 4. Instalação das Ferramentas

## 4.1 Node.js

Verificação da instalação:

```bash
node -v
npm -v
```

---

## 4.2 Git

Verificação da instalação:

```bash
git --version
```

---

## 4.3 Liberação de Scripts no Windows (PowerShell)

Para permitir a execução do `npm` no PowerShell:

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

---

# 5. Criação do Projeto

```bash
mkdir cloud-so-app
cd cloud-so-app
npm init -y
```

---

# 6. Instalação das Dependências

Instalação do Express.js e do CORS:

```bash
npm install express cors
```

Configuração do script no `package.json`:

```json
"scripts": {
  "start": "node index.js"
}
```

---

# 7. Estrutura do Projeto

```plaintext
cloud-so-app/
├── index.js
├── package.json
├── package-lock.json
├── .gitignore
└── public/
    └── index.html
```

---

# 8. Desenvolvimento da Aplicação

A aplicação utiliza o módulo nativo `os` para acessar dados do sistema:

- `os.hostname()` → Nome da máquina;
- `os.platform()` → Plataforma (`win32`, `linux`);
- `os.arch()` → Arquitetura (`x64`);
- `os.cpus()` → Dados dos processadores;
- `os.totalmem()` e `os.freemem()` → Gerenciamento de memória;
- `os.uptime()` → Tempo de atividade.

---

# 9. Criação do Arquivo `.gitignore`

```bash
echo node_modules/ > .gitignore
```

---

# 10. Funcionamento da Aplicação

O servidor serve a página HTML em `/`.

O JavaScript da página faz um `fetch` para o endpoint `/api/sysinfo`, que retorna o JSON com os dados do sistema operacional.

## Configuração de Porta Resiliente

```javascript
const PORT = process.env.PORT || 3001;
```

Localmente utiliza a porta `3001` e no Render utiliza automaticamente a variável `PORT`.

---

# 11. Execução Local

```bash
npm install
node index.js
```

Acesso:

```plaintext
http://localhost:3001
```

---

# 12. Resultado do Teste Local

| Informação | Valor Observado (Local) |
|---|---|
| Hostname | DESKTOP-RB6SL56 |
| Platform | win32 |
| Architecture | x64 |
| Modelo da CPU | Intel(R) Core(TM) i3-10100F @ 3.60GHz |
| Memória Total | 7.85 GB |

---

# 13. Versionamento com Git

```bash
git init
git add .
git commit -m "primeiro commit - cloud-so-app"
git branch -M main
git remote add origin https://github.com/marcellegg/cloud-so-app.git
git push -u origin main
```

---

# 14. Publicação no Render

Etapas realizadas:

1. Acesso ao dashboard do Render;
2. Criação de um novo Web Service;
3. Conexão com o repositório `marcellegg/cloud-so-app`;
4. Definição do Build Command:

```bash
npm install
```

5. Definição do Start Command:

```bash
node index.js
```

---

# 15. Resultado do Teste no Render

| Informação | Valor no Render |
|---|---|
| Hostname | [PREENCHER COM O DADO DO SITE] |
| Platform | linux |
| Architecture | x64 |
| Modelo da CPU | [PREENCHER COM O DADO DO SITE] |
| Memória Total | [PREENCHER COM O DADO DO SITE] |

---

# 16. Comparação entre Ambiente Local e Nuvem

| Informação | Ambiente Local | Ambiente Render | Observação |
|---|---|---|---|
| Hostname | DESKTOP-RB6SL56 | [PREENCHER] | Máquina física vs container |
| Platform | win32 | linux | Windows local vs Linux em nuvem |
| CPU | Intel i3-10100F | [PREENCHER] | Hardware físico vs infraestrutura virtual |
| Memória | 7.85 GB | [PREENCHER] | RAM física vs cota do container |

---

# 17. Análise das Diferenças

A execução local reflete diretamente o hardware físico do computador.

No Render, a aplicação roda em ambiente de nuvem, onde o hostname e a plataforma indicam o isolamento por containers.

O uptime no Render geralmente é menor devido à política de hibernação das instâncias gratuitas quando permanecem inativas.

---

---

# 18. Observações Técnicas

Durante os testes, as seguintes observações técnicas foram registradas:

## Abstração de Hardware

Notou-se que o código JavaScript permanece idêntico nos dois ambientes, mas o sistema operacional retorna dados completamente distintos, comprovando a eficiência da camada de abstração do Kernel.

## Virtualização no Render

O hostname exibido no Render (geralmente uma sequência aleatória de caracteres) confirma que a aplicação não roda diretamente no hardware físico, mas sim em um container isolado.

## Escalabilidade Vertical

Observou-se que a memória total disponível no Render (aproximadamente 512 MB no plano gratuito) é muito inferior à memória disponível na máquina local (8 GB), evidenciando a necessidade de otimização de recursos em ambientes cloud.

---

# 18.1. Problemas Encontrados e Soluções

Abaixo estão os principais desafios enfrentados durante o desenvolvimento e suas respectivas soluções:

| Problema | Causa | Solução |
|---|---|---|
| Erro de Porta em Uso | Tentativa de utilizar a porta `3000`, que já estava ocupada por outro processo local. | Alteração da porta padrão para `3001` no arquivo `index.js`. |
| Scripts Bloqueados | Política de execução do PowerShell impedia a execução do `npm`. | Execução do comando `Set-ExecutionPolicy` conforme descrito na Seção 4.3. |
| Erro de Deploy no Render | O Render não conseguia conectar ao servidor devido à porta fixa no código. | Implementação da variável `process.env.PORT` para utilização da porta automática fornecida pelo Render. |
| CORS Error | O frontend não conseguia consumir a API em alguns navegadores. | Instalação e configuração do middleware `cors` no Express.js. |

---

# 19. Relação com Conceitos de Sistemas Operacionais

## 19.1 Processos

O comando abaixo inicia um processo gerenciado pelo Kernel do Windows (local) ou Linux (Render):

```bash
node index.js
```

---

## 19.2 Gerenciamento de Memória

As funções:

```javascript
totalmem()
freemem()
```

demonstram como o sistema operacional gerencia recursos para os processos.

---

## 19.3 Virtualização

No Render, a aplicação utiliza conteinerização, uma forma de virtualização em nível de sistema operacional que compartilha o Kernel hospedeiro, mas isola as dependências da aplicação.

---

# 20. Conclusão

A atividade demonstrou na prática como a mesma aplicação Node.js se adapta a diferentes ambientes através da abstração de hardware proporcionada pelo sistema operacional e pela flexibilidade da computação em nuvem.

---

# 21. Identificação

| Informação | Dados |
|---|---|
| Projeto | Cloud SO App |
| Aluna | Marcelle de Góes Silva |
| Conteúdo | Nuvem e Sistemas Operacionais |
| Data | 07 de Maio de 2026 |
