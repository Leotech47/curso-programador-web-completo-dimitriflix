# **Guia Completo: Criando uma Conta no GitHub e Utilizando seus Recursos**

O **GitHub** é uma plataforma de hospedagem de código-fonte baseada em Git, amplamente usada para versionamento de código e colaboração em projetos. Abaixo, explico detalhadamente **como criar uma conta no GitHub e utilizar seus principais recursos**.

---

## **1. Criando uma Conta no GitHub**
### **1.1 Acessando o site**
1. Abra um navegador e acesse 👉 [https://github.com/](https://github.com/)
2. Clique em **Sign up** (canto superior direito).

### **1.2 Preenchendo os dados**
1. Informe um **nome de usuário** (único).
2. Digite um **e-mail válido**.
3. Escolha uma **senha segura**.
4. Clique em **"Create Account"**.

### **1.3 Verificando a conta**
1. Resolva o captcha de segurança.
2. Confirme o código enviado para o seu e-mail.
3. Escolha as configurações iniciais (podem ser padrão).
4. Sua conta está pronta para uso! 🚀

---

## **2. Configurando o Git no Computador**
Para usar o GitHub localmente, é necessário instalar o **Git**.

### **2.1 Instalando o Git**
1. Acesse [https://git-scm.com/downloads](https://git-scm.com/downloads).
2. Baixe a versão correspondente ao seu sistema (Windows, macOS ou Linux).
3. Instale aceitando as configurações padrão.

### **2.2 Configurando o Git com sua conta**
Após a instalação, abra o **terminal** (ou **Git Bash**) e execute:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@example.com"
```

Isso vincula sua identidade ao Git.

### **2.3 Gerando uma chave SSH (opcional)**
Isso evita que você tenha que digitar senha sempre ao interagir com repositórios privados:

1. No terminal, execute:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "seu-email@example.com"
   ```
2. Pressione **Enter** para aceitar o local padrão do arquivo.
3. Copie a chave gerada com:
   ```bash
   cat ~/.ssh/id_rsa.pub
   ```
4. No GitHub, vá em **Settings > SSH and GPG Keys > New SSH Key** e cole a chave.

---

## **3. Criando e Gerenciando Repositórios**
### **3.1 Criando um Novo Repositório**
1. No GitHub, clique em **New Repository**.
2. Preencha os campos:
   - **Repository name**: Nome do repositório.
   - **Description** (opcional): Descrição do projeto.
   - **Public** ou **Private** (público ou privado).
   - **Initialize with a README** (se deseja criar um README).
3. Clique em **Create Repository**.

---

## **4. Clonando e Enviando Código para o GitHub**
Após criar um repositório, você pode cloná-lo e enviar arquivos.

### **4.1 Clonando um repositório**
Para baixar um repositório para seu computador:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```
Ou, se estiver usando **SSH**:

```bash
git clone git@github.com:seu-usuario/nome-do-repositorio.git
```

Agora você tem o projeto localmente.

### **4.2 Enviando arquivos para o GitHub**
1. **Acesse a pasta do repositório**:
   ```bash
   cd nome-do-repositorio
   ```

2. **Crie ou modifique arquivos**, por exemplo:
   ```bash
   echo "Meu primeiro repositório!" > README.md
   ```

3. **Adicione os arquivos ao controle de versão**:
   ```bash
   git add .
   ```

4. **Crie um commit**:
   ```bash
   git commit -m "Primeiro commit"
   ```

5. **Envie os arquivos para o GitHub**:
   ```bash
   git push origin main
   ```

Se o branch principal for `master`, use:

```bash
git push origin master
```

---

## **5. Criando e Gerenciando Branches**
Os **branches** permitem trabalhar em novas funcionalidades sem afetar o código principal.

### **5.1 Criando um novo branch**
```bash
git branch nova-funcionalidade
```

### **5.2 Mudando para o branch**
```bash
git checkout nova-funcionalidade
```
Ou use:
```bash
git switch nova-funcionalidade
```

### **5.3 Enviando um branch para o GitHub**
```bash
git push origin nova-funcionalidade
```

---

## **6. Fazendo Pull Requests (PR)**
Os **Pull Requests** permitem colaborar com outras pessoas antes de mesclar código ao repositório principal.

### **6.1 Criando um PR**
1. No GitHub, vá até o repositório.
2. Clique em **Pull Requests > New Pull Request**.
3. Escolha o branch que deseja mesclar.
4. Clique em **Create Pull Request**.
5. Escreva uma descrição e clique em **Submit**.

---

## **7. Utilizando Issues e Wikis**
### **7.1 Criando uma Issue**
As **Issues** são usadas para rastrear bugs ou novas ideias.

1. No repositório, clique em **Issues > New Issue**.
2. Dê um título e descreva o problema ou sugestão.
3. Clique em **Submit New Issue**.

### **7.2 Criando uma Wiki**
1. No repositório, clique em **Wiki**.
2. Clique em **Create the first page**.
3. Escreva a documentação e salve.

---

## **8. Trabalhando com GitHub Actions (Automação)**
O **GitHub Actions** permite automação de tarefas como testes e deploys.

### **8.1 Criando um Workflow Básico**
1. No repositório, crie a pasta `.github/workflows/`.
2. Crie um arquivo YAML (`workflow.yml`) e adicione:

   ```yaml
   name: CI/CD Pipeline
   on: push
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout código
           uses: actions/checkout@v2
         - name: Configurar Node.js
           uses: actions/setup-node@v2
           with:
             node-version: '16'
         - name: Instalar dependências
           run: npm install
         - name: Rodar testes
           run: npm test
   ```
3. Suba esse arquivo para o GitHub, e o workflow será executado automaticamente.

---

## **Conclusão**
Agora você sabe como **criar uma conta no GitHub, configurar o Git localmente e usar os principais recursos da plataforma**! O GitHub é essencial para desenvolvimento colaborativo e controle de versão.

---

# **9. Recursos Avançados do GitHub**

Agora que você já sabe como criar repositórios, trabalhar com branches e fazer pull requests, vamos explorar **recursos mais avançados** do GitHub.

---

## **9.1 Gerenciando Releases (Versões do Projeto)**
O **Releases** do GitHub permite publicar versões do seu projeto, útil para distribuir software de forma organizada.

### **Criando uma Release**
1. Acesse o repositório no GitHub.
2. Vá para a aba **Releases** e clique em **Draft a new release**.
3. Escolha um **tag name** (exemplo: `v1.0.0`).
4. Adicione uma **descrição das mudanças**.
5. Se necessário, **anexe arquivos binários** (ZIP, EXE, etc.).
6. Clique em **Publish Release**.

Isso facilita a distribuição de software para usuários e facilita a rastreabilidade de versões.

---

## **9.2 Trabalhando com GitHub Projects (Kanban)**
O **GitHub Projects** permite gerenciar tarefas e organizar o desenvolvimento com um quadro Kanban.

### **Criando um Projeto**
1. No repositório, clique em **Projects**.
2. Clique em **New Project**.
3. Escolha um template (como **Basic Kanban**).
4. Adicione colunas como **To Do**, **In Progress**, **Done**.
5. Crie e mova **Issues e Pull Requests** no quadro.

Isso ajuda a gerenciar tarefas em projetos colaborativos.

---

## **9.3 Criando e Utilizando Templates**
Os **Templates** permitem criar padrões para Issues, Pull Requests e até repositórios inteiros.

### **Criando Templates de Issue**
1. No repositório, crie a pasta `.github/ISSUE_TEMPLATE/`.
2. Dentro dela, crie um arquivo `bug_report.md` com o seguinte conteúdo:

   ```md
   ---
   name: Relatar um Bug
   about: Descreva um erro encontrado no projeto
   title: "[BUG] Descreva o problema"
   labels: bug
   ---
   **Descrição do problema**
   Explique o que aconteceu.

   **Passos para reproduzir**
   1. Vá até '...'
   2. Clique em '...'
   3. Veja o erro

   **Comportamento esperado**
   O que você esperava que acontecesse?
   ```

Agora, ao abrir uma nova **Issue**, esse modelo será usado.

### **Criando Templates de Pull Request**
1. No repositório, crie a pasta `.github/` e adicione um arquivo `PULL_REQUEST_TEMPLATE.md`:

   ```md
   # Descrição
   Descreva as mudanças feitas e por que são necessárias.

   ## Tipo de mudança
   - [ ] Correção de bug
   - [ ] Nova funcionalidade
   - [ ] Refatoração
   ```

Isso garante padronização nas contribuições.

---

## **9.4 Utilizando GitHub Pages (Hospedagem de Sites)**
O **GitHub Pages** permite hospedar sites estáticos (como portfólios ou documentações).

### **Ativando GitHub Pages**
1. Vá até as **Configurações** do repositório.
2. Role até a seção **GitHub Pages**.
3. Em **Source**, selecione `main` ou um branch específico.
4. Clique em **Save**.

Se houver um arquivo `index.html` no repositório, ele será publicado em:  
🔗 `https://seu-usuario.github.io/nome-do-repositorio/`

---

## **9.5 Segurança no GitHub**
Para proteger seus projetos, o GitHub oferece recursos como **proteção de branch**, **tokens de acesso** e **autenticação de dois fatores (2FA)**.

### **Ativando Autenticação de Dois Fatores (2FA)**
1. Vá em **Settings > Security**.
2. Clique em **Enable Two-Factor Authentication**.
3. Escolha o método (app autenticador ou SMS).

Isso melhora a segurança da sua conta.

### **Protegendo o Branch `main`**
1. Vá até as **Configurações** do repositório.
2. Clique em **Branches**.
3. Em **Branch Protection Rules**, adicione regras como:
   - Exigir aprovação antes de mesclar PRs.
   - Bloquear commits diretos no `main`.

Isso garante mais controle sobre o código principal.

---

## **10. Explorando GitHub Marketplace**
O **GitHub Marketplace** oferece **integrações e ferramentas** que automatizam o fluxo de trabalho.

### **Extensões Úteis**
- **CodeQL**: Analisa código em busca de vulnerabilidades.
- **Dependabot**: Atualiza dependências automaticamente.
- **Coveralls**: Gera relatórios de cobertura de testes.

Para instalar, acesse [https://github.com/marketplace](https://github.com/marketplace).

---

## **Conclusão**
Agora você domina desde a criação da conta até recursos avançados como **GitHub Actions, Releases, Templates e Segurança**.

---

