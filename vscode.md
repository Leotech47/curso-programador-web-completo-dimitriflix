O **Visual Studio Code (VSCode)** é uma das IDEs mais populares para desenvolvimento de software, devido à sua leveza, extensibilidade e suporte a diversas linguagens de programação. Abaixo, explico detalhadamente como **instalar e utilizar** o VSCode no computador.

---

## **1. Instalando o Visual Studio Code**

### **1.1 Requisitos mínimos do sistema**
- **Windows**: Windows 8.1, 10 ou 11 (64 bits recomendado).
- **MacOS**: macOS 10.11 ou superior.
- **Linux**: Ubuntu, Debian, Fedora ou outras distribuições baseadas em Linux.

### **1.2 Download do instalador**
1. Acesse o site oficial do VSCode:  
   👉 [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Clique no botão **Download for...** (Windows, macOS ou Linux).
3. Escolha a versão apropriada:
   - Para **Windows**: Baixe o instalador `.exe` (recomendado).
   - Para **MacOS**: Baixe o `.zip` e arraste o VSCode para a pasta **Aplicativos**.
   - Para **Linux**: Baixe o `.deb` (Debian/Ubuntu) ou `.rpm` (Fedora) e instale via terminal.

### **1.3 Instalando o VSCode**
#### **No Windows**
1. Após baixar o instalador `.exe`, clique duas vezes para abrir.
2. Aceite os **termos de licença** e clique em **Avançar**.
3. Escolha o diretório de instalação (pode deixar o padrão).
4. Marque as opções úteis, como:
   - "Adicionar ao PATH" (para facilitar o uso no terminal).
   - "Criar atalho na área de trabalho".
5. Clique em **Instalar** e aguarde.
6. Após a instalação, clique em **Concluir** para abrir o VSCode.

#### **No macOS**
1. Extraia o arquivo `.zip` baixado.
2. Arraste o ícone do **VSCode** para a pasta **Aplicativos**.

#### **No Linux (Debian/Ubuntu)**
1. No terminal, execute:
   ```bash
   sudo dpkg -i code_*.deb
   ```
2. Para resolver dependências, caso necessário:
   ```bash
   sudo apt-get install -f
   ```

---

## **2. Configurando o VSCode**
Após a instalação, ao abrir o VSCode pela primeira vez, você verá a tela inicial. Para melhor aproveitamento, siga estas etapas:

### **2.1 Alterando o idioma para português**
1. Pressione `Ctrl + Shift + P` e digite `Configure Display Language`.
2. Escolha `Install additional languages`.
3. Procure por **Portuguese (Brazil)** e clique em **Install**.
4. Reinicie o VSCode.

### **2.2 Instalando extensões essenciais**
As extensões aumentam a produtividade. Para instalar:
1. Clique no ícone de **Extensões** (`Ctrl + Shift + X`).
2. Busque pelas extensões desejadas e clique em **Instalar**.
3. Recomendações:
   - **Python** (se for programar em Python).
   - **ESLint** (para JavaScript e TypeScript).
   - **Live Server** (para desenvolvimento web).
   - **Material Icon Theme** (ícones para organização).
   - **GitLens** (integração avançada com Git).

---

## **3. Como usar o VSCode**
### **3.1 Criando um novo projeto**
1. **Abrindo uma pasta de projeto**:
   - Vá em **File > Open Folder** e selecione a pasta do projeto.
   - Ou use o atalho `Ctrl + K + O`.

2. **Criando um novo arquivo**:
   - Pressione `Ctrl + N` para um novo arquivo.
   - Para salvar, `Ctrl + S` e defina o nome com a extensão adequada (ex: `index.html`, `script.js`).

### **3.2 Executando código no VSCode**
- **Para rodar código Python**:
  1. Instale a extensão **Python**.
  2. Pressione `Ctrl + Shift + P` e digite `Python: Select Interpreter`.
  3. Escolha a versão correta do Python.
  4. Para executar, clique no botão **Run** ou pressione `Ctrl + Shift + B`.

- **Para rodar código JavaScript**:
  1. Abra o terminal (`Ctrl + J`).
  2. Digite `node arquivo.js` (se o Node.js estiver instalado).

### **3.3 Atalhos úteis**
| Atalho | Ação |
|--------|------|
| `Ctrl + P` | Abrir rapidamente um arquivo |
| `Ctrl + Shift + P` | Abrir a barra de comandos |
| `Ctrl + J` | Abrir/fechar o terminal integrado |
| `Ctrl + B` | Mostrar/ocultar barra lateral |
| `Ctrl + Shift + X` | Abrir a aba de extensões |
| `Ctrl + Alt + ↑ / ↓` | Duplicar linha acima/abaixo |

---

## **4. Personalizando o VSCode**
1. **Alterando o tema**:
   - Vá em **File > Preferences > Color Theme** (`Ctrl + K + T`).
   - Escolha um tema, como **Dark+** ou **Dracula**.

2. **Configurando atalhos personalizados**:
   - Vá em **File > Preferences > Keyboard Shortcuts**.

3. **Ativando o AutoSave**:
   - Vá em **File > Auto Save** para salvar automaticamente.

---

## **5. Integração com Git e GitHub**
1. **Inicializando um repositório Git**:
   - No terminal, execute:
     ```bash
     git init
     ```
   - Ou clique na aba de **Controle de Código-Fonte** (`Ctrl + Shift + G`).

2. **Fazendo commit de arquivos**:
   - Adicione os arquivos ao Git (`+` na aba de Controle de Código-Fonte).
   - Escreva uma mensagem e clique em **Commit**.

3. **Publicando no GitHub**:
   - Autentique sua conta GitHub.
   - Clique em **Publish to GitHub**.

---

## **Conclusão**
Agora você sabe como **instalar, configurar e usar o VSCode**! Com as extensões corretas e boas práticas, ele se torna uma poderosa ferramenta para desenvolvimento de software.


# **Criando um Projeto no VS Code e Fazendo Upload para o GitHub**

Aqui está um guia passo a passo para **criar um projeto no VS Code** e **enviá-lo para o GitHub**.

---

## **1. Criando um Projeto no VS Code**
### **1.1 Abrindo o VS Code**
1. **Abra o VS Code** no seu computador.
2. Clique em **File** > **Open Folder...** e escolha a pasta onde deseja criar o projeto.
3. Se quiser criar uma nova pasta, clique com o botão direito dentro do Explorer do VS Code e selecione **New Folder**.

### **1.2 Criando Arquivos**
1. No Explorer do VS Code, clique em **New File** para criar arquivos dentro do projeto.
2. Exemplo: Crie um arquivo chamado `index.html`, `script.js` ou `app.py`, dependendo do tipo de projeto.

---

## **2. Inicializando o Git no Projeto**
Agora, vamos configurar o **Git** para controlar as versões do código.

### **2.1 Abrindo o Terminal**
1. No VS Code, **abra o terminal** pressionando `Ctrl + J` ou vá em **View** > **Terminal**.

### **2.2 Inicializando o Repositório Git**
No terminal, execute:
```bash
git init
```
Isso cria um repositório Git dentro da pasta do projeto.

### **2.3 Adicionando um Arquivo `.gitignore` (Opcional)**
Para evitar enviar arquivos desnecessários (ex: `node_modules`, `venv`), crie um arquivo chamado `.gitignore` e adicione regras como:

```
node_modules/
venv/
__pycache__/
.DS_Store
```

---

## **3. Criando um Repositório no GitHub**
Agora, precisamos criar um repositório remoto para armazenar o código no GitHub.

### **3.1 Criando um Novo Repositório**
1. Acesse **[GitHub](https://github.com/)** e faça login.
2. Clique no botão **New Repository**.
3. Escolha um nome para o repositório e, opcionalmente, adicione uma descrição.
4. **Não marque a opção "Initialize with a README"** (evita conflitos na sincronização inicial).
5. Clique em **Create Repository**.

O GitHub mostrará instruções com um **link HTTPS ou SSH** do repositório. Copie esse link.

---

## **4. Conectando o Projeto Local ao GitHub**
Agora, vamos **vincular o projeto local ao repositório remoto**.

### **4.1 Adicionando o Repositório Remoto**
No terminal do VS Code, execute (substitua pelo seu link do GitHub):

```bash
git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
```
Se estiver usando **SSH**, use:

```bash
git remote add origin git@github.com:seu-usuario/nome-do-repositorio.git
```

### **4.2 Adicionando os Arquivos ao Controle de Versão**
Agora, adicione todos os arquivos ao Git:

```bash
git add .
```

### **4.3 Criando um Commit**
Crie um commit inicial com uma mensagem:

```bash
git commit -m "Primeiro commit"
```

### **4.4 Enviando o Código para o GitHub**
Agora, envie o código para o repositório remoto:

```bash
git push -u origin main
```
Se o branch principal for `master`, use:

```bash
git push -u origin master
```

Agora seu projeto está disponível no GitHub! 🚀

---

## **5. Verificando se o Código Foi Enviado**
1. Acesse o GitHub e vá até o repositório.
2. Atualize a página e veja os arquivos do projeto.

---

## **6. Atualizando o Projeto no GitHub**
Se você fizer alterações no código e quiser atualizar no GitHub, siga estes passos:

1. **Verificar alterações**:
   ```bash
   git status
   ```
2. **Adicionar os arquivos modificados**:
   ```bash
   git add .
   ```
3. **Criar um novo commit**:
   ```bash
   git commit -m "Atualização do projeto"
   ```
4. **Enviar as mudanças para o GitHub**:
   ```bash
   git push origin main
   ```

---

## **7. Clonando um Projeto do GitHub para o VS Code**
Se precisar baixar um projeto do GitHub para o VS Code, use:

1. No GitHub, copie o link do repositório (HTTPS ou SSH).
2. No terminal do VS Code, execute:

   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   ```

3. Abra a pasta clonada no VS Code e comece a trabalhar!

---

## **Conclusão**
Agora você sabe **criar um projeto no VS Code, conectá-lo ao GitHub e fazer uploads de código**. 🚀
