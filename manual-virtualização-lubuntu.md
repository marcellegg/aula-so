# 🖥️ Manual de Virtualização com Lubuntu no VirtualBox

## 📚 Disciplina: Sistemas Operacionais

## 🎯 Objetivo da Atividade

Este manual apresenta o processo completo de inicialização e utilização de um ambiente virtualizado utilizando o software **Oracle VM VirtualBox** e o sistema operacional **Lubuntu Linux**.

A atividade consiste em:

- Instalar o VirtualBox
- Criar uma máquina virtual
- Inicializar um sistema Linux leve
- Explorar o ambiente virtualizado
- Utilizar recursos do sistema
- Documentar todo o processo
- Publicar o material no repositório da disciplina

A virtualização permite executar múltiplos sistemas operacionais dentro de um único computador físico, de forma isolada e segura.

---

# 🧠 1. O que é Virtualização?

A virtualização é uma tecnologia que permite criar computadores virtuais dentro de um computador físico.

Esses computadores virtuais são chamados de **Máquinas Virtuais (VMs)**.

Cada máquina virtual possui:

- Sistema operacional próprio
- Memória dedicada
- Disco virtual
- Configurações independentes

Essa tecnologia é muito utilizada para:

- Testar sistemas operacionais
- Criar ambientes de desenvolvimento
- Simular servidores
- Realizar estudos e treinamentos

---

# 💻 2. Requisitos do Sistema

Antes de iniciar o processo de virtualização, é importante verificar se o computador possui os requisitos mínimos.

## 🔧 Hardware recomendado

| Recurso | Requisito mínimo |
|------|------|
| Processador | Suporte à virtualização |
| Memória RAM | 4 GB |
| Espaço em Disco | 20 GB livres |
| Sistema operacional | Windows, Linux ou macOS |

---

## 📦 Software necessário

Para realizar a atividade serão utilizados os seguintes programas:

- Oracle VM VirtualBox
- Imagem ISO do Lubuntu Linux

A imagem ISO é um arquivo que contém todos os arquivos necessários para inicializar ou instalar o sistema operacional.

---

# ⬇️ 3. Download dos Programas

## 🔽 Baixar o VirtualBox

1. Acesse o site oficial do VirtualBox  
2. Clique na opção **Downloads**
3. Escolha a versão compatível com seu sistema operacional
4. Baixe o instalador

---

## 🐧 Baixar o Lubuntu

1. Acesse o site oficial do Lubuntu
2. Escolha a versão desejada
3. Baixe o arquivo **.ISO**

Versão utilizada nesta atividade:

- **Lubuntu 25.10**

Esse arquivo será utilizado para inicializar a máquina virtual.

---

# ⚙️ 4. Instalação do VirtualBox

Após baixar o instalador:

1. Execute o arquivo de instalação
2. Clique em **Next**
3. Aceite os termos de uso
4. Mantenha as configurações padrão
5. Clique em **Install**

Durante a instalação podem aparecer avisos sobre drivers de rede virtual.  
Esses drivers permitem que a máquina virtual tenha acesso à internet.

Após finalizar, clique em **Finish** para abrir o programa.

---

# 🖥️ 5. Criando uma Máquina Virtual

Com o VirtualBox aberto:

1. Clique em **Novo (New)**
2. Preencha as informações da máquina virtual

## 📌 Configurações recomendadas

| Configuração | Valor |
|------|------|
| Nome | Lubuntu Linux |
| Tipo | Linux |
| Versão | Ubuntu (64-bit) |

---

## 🧠 Configuração de Memória RAM

A memória RAM define quanto da memória do computador será utilizada pela máquina virtual.

### Recomendação

| Configuração | Valor |
|------|------|
| Memória | 2048 MB |

Caso o computador possua mais memória disponível, esse valor pode ser aumentado.

---

# 💾 6. Criando o Disco Virtual

O disco virtual é o espaço onde o sistema operacional será executado ou instalado.

## Configurações recomendadas

| Opção | Configuração |
|------|------|
| Tipo de disco | VDI |
| Armazenamento | Dinamicamente alocado |
| Tamanho | 20 GB |

### Explicação

- **VDI**: formato padrão do VirtualBox  
- **Dinamicamente alocado**: ocupa espaço conforme o uso  
- **20 GB**: suficiente para inicializar o sistema e realizar testes

Após finalizar essa etapa, a máquina virtual será criada.

---

# 🐧 7. Inicializando o Lubuntu

Agora será realizada a inicialização do sistema operacional.

### Passo 1

Selecione a máquina virtual criada.

Clique em **Iniciar (Start)**.

---

### Passo 2

O VirtualBox solicitará o arquivo de inicialização do sistema.

Selecione o **arquivo ISO do Lubuntu Linux**.

---

### Passo 3

O sistema será carregado e iniciará o ambiente do **Lubuntu em modo Live Session**.

Esse modo permite utilizar o sistema sem precisar instalá-lo imediatamente no disco virtual.

---

# ⚙️ 8. Exploração do Ambiente do Lubuntu

Após a inicialização, o Lubuntu carregará corretamente o ambiente gráfico padrão.

O Lubuntu utiliza o ambiente **LXQt**, conhecido por ser:

- Leve
- Rápido
- Organizado
- Ideal para computadores com menos recursos

Durante a exploração do sistema, é possível observar e utilizar:

- Área de trabalho do Lubuntu
- Atalho **Install Lubuntu 25.10**
- Atalho **Lubuntu Manual**
- Atalho **Network**
- Gerenciador de arquivos
- Navegador Firefox
- Terminal Linux
- Calculadora científica **Qalculate!**

---

# 📂 9. Explorando o Gerenciador de Arquivos

Durante a prática, também é possível abrir o gerenciador de arquivos do sistema, que no Lubuntu é o **PCManFM-Qt**.

Nele, é possível navegar pelas pastas padrão do usuário, como:

- Desktop
- Documents
- Downloads
- Music
- Pictures
- Public
- Templates
- Videos

Essa etapa é importante para confirmar que o ambiente gráfico está funcionando corretamente e que a estrutura do sistema está acessível.

---

# 🌐 10. Acessando o Manual Oficial do Lubuntu

Outro recurso importante é o acesso ao **manual oficial do Lubuntu**, por meio do navegador Firefox.

Esse recurso permite:

- Consultar a documentação oficial do sistema
- Entender melhor o ambiente LXQt
- Verificar instruções de instalação e uso
- Aprofundar o aprendizado sobre o sistema operacional

Esse acesso também demonstra que a navegação e os aplicativos gráficos estão funcionando corretamente no ambiente virtualizado.

---

# 💻 11. Utilizando o Terminal

O terminal é uma ferramenta importante no Linux.

Durante a atividade, também é possível abrir o terminal do Lubuntu para verificar o funcionamento da linha de comando.

O prompt exibido normalmente será:

```bash
lubuntu@lubuntu:~$
```

Isso indica que:

- o usuário é `lubuntu`
- o nome do host é `lubuntu`
- o diretório atual é a pasta pessoal (`~`)

Alguns comandos básicos que podem ser utilizados no terminal são:

## Listar arquivos

```bash
ls
```

## Verificar diretório atual

```bash
pwd
```

## Listar arquivos com detalhes

```bash
ls -la
```

## Verificar uso de memória

```bash
free -h
```

## Verificar espaço em disco

```bash
df -h
```

## Verificar interfaces de rede

```bash
ip a
```

## Atualizar lista de pacotes

```bash
sudo apt update
```

---

# 🧮 12. Teste com Aplicativos do Sistema

Durante a exploração da máquina virtual, também é possível abrir um aplicativo nativo do Lubuntu, como a calculadora científica **Qalculate!**.

Esse teste é importante para confirmar que:

- o menu de aplicativos está funcionando;
- o ambiente gráfico está responsivo;
- os programas nativos do sistema podem ser executados normalmente.

Esse tipo de teste ajuda a validar a estabilidade da máquina virtual durante o uso prático.

---

# 🧪 13. Testes Realizados

Durante a exploração da máquina virtual, alguns testes básicos podem ser realizados para verificar se o sistema está funcionando corretamente.

## Testes executados

- Inicialização da máquina virtual
- Carregamento do ambiente gráfico do Lubuntu
- Acesso à área de trabalho
- Abertura do gerenciador de arquivos
- Acesso ao navegador Firefox
- Consulta ao manual oficial do Lubuntu
- Abertura do terminal
- Teste com comandos básicos no terminal
- Execução da calculadora científica Qalculate!

Todos os testes podem ser realizados com sucesso, confirmando que a máquina virtual foi configurada corretamente e que o Lubuntu está funcionando de forma adequada.

---

# ⚡ 14. Vantagens da Virtualização

A virtualização oferece diversas vantagens para estudos, testes e desenvolvimento de sistemas.

## Segurança

Permite testar sistemas operacionais ou softwares sem afetar o sistema principal do computador.

## Isolamento

Cada máquina virtual funciona de forma independente, evitando interferência entre sistemas.

## Aprendizado

Facilita o estudo de diferentes sistemas operacionais sem a necessidade de instalar vários sistemas no computador físico.

## Flexibilidade

Máquinas virtuais podem ser criadas, modificadas ou removidas facilmente conforme a necessidade.

## Praticidade

Permite testar ambientes completos de forma rápida, segura e organizada.

---

# 🧾 15. Conclusão

A realização desta atividade permite compreender, na prática, o funcionamento da virtualização utilizando o software **VirtualBox**.

Também é possível inicializar e explorar o sistema operacional **Lubuntu Linux**, adquirindo conhecimentos importantes sobre criação de máquinas virtuais e utilização de sistemas baseados em Linux.

O Lubuntu se destaca como uma excelente opção para virtualização por ser um sistema leve, rápido e adequado para ambientes de estudo.

A virtualização é uma ferramenta essencial na área de tecnologia da informação, sendo amplamente utilizada em ambientes de desenvolvimento, testes, servidores e computação em nuvem.

---
