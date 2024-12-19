### Principais Comandos Git para o Terminal

---

### **1. Configuração Inicial**
- **Configurar nome de usuário**:
  ```bash
  git config --global user.name "Seu Nome"
  ```
- **Configurar e-mail**:
  ```bash
  git config --global user.email "seuemail@dominio.com"
  ```
- **Verificar configurações**:
  ```bash
  git config --list
  ```

---

### **2. Inicializar ou Clonar Repositórios**
- **Inicializar um repositório local**:
  ```bash
  git init
  ```
- **Clonar um repositório remoto**:
  ```bash
  git clone <url-do-repositorio>
  ```

---

### **3. Status e Logs**
- **Verificar status do repositório**:
  ```bash
  git status
  ```
- **Visualizar o histórico de commits**:
  ```bash
  git log
  ```
- **Ver histórico compacto**:
  ```bash
  git log --oneline
  ```

---

### **4. Trabalhando com Branches**
- **Criar uma nova branch**:
  ```bash
  git branch nome-da-branch
  ```
- **Trocar para uma branch existente**:
  ```bash
  git checkout nome-da-branch
  ```
- **Criar e mudar para uma nova branch**:
  ```bash
  git checkout -b nome-da-branch
  ```
- **Listar todas as branches**:
  ```bash
  git branch
  ```
- **Deletar uma branch local**:
  ```bash
  git branch -d nome-da-branch
  ```

---

### **5. Alterações no Código**
- **Adicionar arquivos ao staging**:
  ```bash
  git add arquivo.txt
  ```
- **Adicionar todos os arquivos modificados**:
  ```bash
  git add .
  ```
- **Fazer um commit**:
  ```bash
  git commit -m "Mensagem do commit"
  ```
- **Alterar o último commit** (se ainda não foi enviado ao repositório remoto):
  ```bash
  git commit --amend
  ```
- **Desfazer alterações em um arquivo**:
  ```bash
  git checkout -- arquivo.txt
  ```

---

### **6. Sincronização com Repositórios Remotos**
- **Verificar os remotes configurados**:
  ```bash
  git remote -v
  ```
- **Adicionar um repositório remoto**:
  ```bash
  git remote add origin <url-do-repositorio>
  ```
- **Enviar commits para o repositório remoto**:
  ```bash
  git push origin main
  ```
- **Enviar todos os branches para o remoto**:
  ```bash
  git push --all origin
  ```
- **Baixar mudanças do remoto**:
  ```bash
  git pull origin main
  ```

---

### **7. Mesclagem (Merge)**
- **Mesclar uma branch na branch atual**:
  ```bash
  git merge nome-da-branch
  ```
- **Abortar um merge em andamento**:
  ```bash
  git merge --abort
  ```

---

### **8. Rebase**
- **Rebase na branch atual**:
  ```bash
  git rebase nome-da-branch
  ```
- **Resolver conflitos durante rebase**:
  Após resolver os conflitos:
  ```bash
  git rebase --continue
  ```

---

### **9. Reset e Revert**
- **Desfazer mudanças no staging**:
  ```bash
  git reset arquivo.txt
  ```
- **Resetar o repositório para um commit anterior**:
  ```bash
  git reset --hard <hash-do-commit>
  ```
- **Criar um novo commit que reverte um commit anterior**:
  ```bash
  git revert <hash-do-commit>
  ```

---

### **10. Trabalhando com Tags**
- **Criar uma tag**:
  ```bash
  git tag -a v1.0 -m "Versão 1.0"
  ```
- **Listar todas as tags**:
  ```bash
  git tag
  ```
- **Enviar tags para o repositório remoto**:
  ```bash
  git push origin --tags
  ```

---

### **11. Outros Comandos Úteis**
- **Ver diferenças entre commits ou arquivos**:
  ```bash
  git diff
  ```
- **Excluir arquivos não rastreados**:
  ```bash
  git clean -f
  ```
- **Ver quem modificou cada linha de um arquivo**:
  ```bash
  git blame arquivo.txt
  ```
- **Verificar a árvore do projeto**:
  ```bash
  git log --graph --all --decorate --oneline
  ```

---

### **Resumo Rápido**
| **Ação**               | **Comando**                           |
|-------------------------|---------------------------------------|
| Inicializar repositório | `git init`                           |
| Clonar repositório      | `git clone <url>`                    |
| Verificar status        | `git status`                         |
| Adicionar arquivos      | `git add .`                          |
| Fazer commit            | `git commit -m "Mensagem"`           |
| Criar branch            | `git checkout -b nova-branch`        |
| Mesclar branch          | `git merge outra-branch`             |
| Enviar código remoto    | `git push origin main`               |
| Baixar mudanças         | `git pull origin main`               |
