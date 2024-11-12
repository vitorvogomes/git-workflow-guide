
# Guia Prático Git

## **Comandos Base**
- **`git init`**  
  Inicializa um novo repositório Git.

## **Configuração de Usuário**
- **`git config --global user.email "you@example.com"`**  
  Define o e-mail do usuário globalmente na máquina.
  
- **`git config --global user.name "Your Name"`**  
  Define o nome do usuário globalmente na máquina.

- **`git config user.email "you@example.com"`**  
  Define o e-mail do usuário para o repositório local.

- **`git config user.name "Your Name"`**  
  Define o nome do usuário para o repositório local.

## **Mapeamento e Arquivos**
- **`git status`**  
  Mostra as alterações e status dos arquivos no repositório.

- **`ls -a`**  
  Lista todos os arquivos, incluindo os ocultos.

- **`.gitignore`**  
  Arquivo para especificar padrões de arquivos e pastas que não devem ser rastreados pelo Git.

## **Adição de Arquivos**
- **`git add <file>`**  
  Adiciona um arquivo específico à área de staging.

- **`git add .`**  
  Adiciona todas as alterações do diretório atual à área de staging.

- **`git add *`**  
  Adiciona todos os arquivos (exceto os ignorados) à área de staging.

## **Commit de Alterações**
- **`git commit`**  
  Abre o editor padrão para adicionar uma mensagem de commit.

- **`git commit -m "commit message"`**  
  Faz o commit com uma mensagem inline.

- **`git commit -a`**  
  Commita alterações automaticamente de arquivos já rastreados.

- **`git commit -am "Commit message"`**  
  Adiciona e commit arquivos rastreados com uma mensagem inline.

## **Branching e Atualização**
- **`git branch`**  
  Lista as branches disponíveis e indica a branch ativa.

- **`git pull`**  
  Atualiza o repositório local com as últimas alterações remotas.

- **`git branch -M <branch name>`**  
  Renomeia ou define a branch principal.

- **`git remote add origin <repository>`**  
  Adiciona um repositório remoto.

- **`git push -u origin <branch name>`**  
  Sobe a branch atual para o repositório remoto.

## **Trabalho com Repositórios**
- **`git clone <repository>`**  
  Clona um repositório remoto para o local.

- **`git checkout -b <branchName>`**  
  Cria e alterna para uma nova branch.

- **`git branch -d <branchName>`**  
  Deleta uma branch local.

- **`git push origin --delete <branchName>`**  
  Deleta uma branch remotamente.

- **`rm -rf .git`**  
  Remove o repositório local Git.

## **Gerenciamento de Arquivos**
- **`git restore <file>`**  
  Desfaz alterações em um arquivo específico no diretório de trabalho.

- **`git reset <COMMIT_ID>`**  
  Reverte o repositório para um commit específico, mantendo as alterações locais.

- **`git revert <COMMIT_ID>`**  
  Cria um novo commit para desfazer mudanças de um commit específico.

- **`git checkout -- <file>`**  
  Desfaz alterações não confirmadas em um arquivo específico.

- **`git clean -fd`**  
  Remove novos arquivos não rastreados.

- **`git reset HEAD`**  
  Desfaz as alterações da área de staging.

- **`git reset --hard HEAD`**  
  Restaura o repositório ao último commit confirmado, descartando alterações locais.

- **`git stash`**  
  Salva temporariamente as alterações locais não confirmadas.

- **`git stash pop`**  
  Restaura as alterações salvas no stash.

## **Comandos Não Documentados**
- **`git restore --staged <file>`**  
  Remove um arquivo específico da área de staging, mas mantém as alterações locais.

- **`git rm --cached <file>`**  
  Remove um arquivo do controle de versão, mantendo-o no sistema de arquivos local.

---

# **Padrão de Mensagens de Commit**

### **[FEAT]**  
Para novas funcionalidades ou features.  
**Exemplo:**  
`git commit -m "[FEAT] Implementação da tela de login"`

### **[FIX]**  
Para correções de bugs.  
**Exemplo:**  
`git commit -m "[FIX] Correção de bug na validação de formulários"`

### **[UPDATE]**  
Para modificações em arquivos estáticos.  
**Exemplo:**  
`git commit -m "[UPDATE] Adicionado novo logo na pasta assets"`

### **[REFACTOR]**  
Para refatorações sem alterar a lógica do sistema.  
**Exemplo:**  
`git commit -m "[REFACTOR] Melhoria na estrutura do código do componente Header"`

### **[WIP]**  
Para trabalhos em progresso.  
**Exemplo:**  
`git commit -m "[WIP] Desenvolvimento da integração com API externa"`

### **[BREAKING] / [BREAKING CHANGE]**  
Indica alterações que quebram a compatibilidade.  
**Exemplo:**  
`git commit -m "[BREAKING] Alteração de estrutura de banco de dados"`

### **[TEST]**  
Para criação ou modificação de testes.  
**Exemplo:**  
`git commit -m "[TEST] Adicionado teste unitário para função validateEmail"`

### **[STYLE]**  
Para mudanças de estilo ou formatação.  
**Exemplo:**  
`git commit -m "[STYLE] Ajuste de identação e remoção de linhas em branco"`

### **[CHORE]**  
Para tarefas de manutenção ou setup do projeto.  
**Exemplo:**  
`git commit -m "[CHORE] Atualização das dependências do projeto"`

### **[DOCS]**  
Para atualizações de documentação.  
**Exemplo:**  
`git commit -m "[DOCS] Atualização do README com instruções de instalação"`

### **[PERF]**  
Para melhorias de performance.  
**Exemplo:**  
`git commit -m "[PERF] Otimização da função de carregamento de dados"`

### **[REVERT]**  
Para reverter commits anteriores.  
**Exemplo:**  
`git commit -m "[REVERT] Revertendo commit de integração incorreta"`

### **[CI]**  
Para alterações na configuração de integração contínua.  
**Exemplo:**  
`git commit -m "[CI] Configuração inicial do pipeline no GitHub Actions"`