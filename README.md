# 🚀 Projeto de Estudo - GitHub Projects com Automação

Este repositório demonstra um sistema completo de automação para GitHub Projects, criando **verdadeiros relacionamentos hierárquicos** entre Epics e sub-issues.

## 🎯 Principais Funcionalidades

### ✅ Criação Automática de Sub-Issues
- 🤖 Cria sub-issues automaticamente a partir de Epics
- 🏷️ Aplica labels de prioridade, tipo e categorização
- 🎯 Associa automaticamente a milestones/sprints
- 🔗 Estabelece relacionamentos bidirecionais reais

### 📊 Tracking Automático de Progresso  
- ✅ Atualiza checklist do Epic quando sub-issues são fechadas
- 📈 Calcula percentual de progresso em tempo real
- 🎉 Fecha Epic automaticamente quando 100% completo
- 🔄 Reabre Epic se sub-issues forem reabertas

### 🎨 Interface Visual Melhorada
- 📋 Checklists automáticos com progresso visual
- 🏷️ Sistema de labels organizadas e consistentes  
- 📊 Indicadores de progresso com emojis
- 🔗 Navegação fácil entre Epic e sub-issues

## 📁 Estrutura do Projeto

```
.github/
├── ISSUE_TEMPLATE/
│   ├── epic.yml              # 📋 Template para Epics (atualizado)
│   ├── feature.yml           # ⚡ Template para Features  
│   └── task.yml              # ✅ Template para Tasks
└── workflows/
    ├── create-sub-issues-epic.yml     # 🤖 Cria sub-issues automaticamente
    ├── update-epic-progress.yml       # 📊 Atualiza progresso do Epic
    └── create-sub-issue.yml           # 📜 Workflow original (legado)

AUTOMATION_GUIDE.md           # 📖 Guia completo de uso
README.md                     # 📄 Este arquivo
```

## 🚀 Como Usar

### 1. Criar um Epic
1. Clique em **"New Issue"**
2. Selecione o template **"Epic"**
3. Preencha os campos:
   - **Objetivo:** Descrição do Epic
   - **Prioridade:** `baixa`, `media`, `alta`, `critica`
   - **Tipo:** `frontend`, `backend`, `fullstack`, etc.
   - **Sprint:** Nome da milestone/sprint
   - **Sub-issues a serem criadas:**
     ```
     - [ ] Implementando ambiente desenvolvimento
     - [ ] Criar API de autenticação
     - [ ] Implementar tela de login
     - [ ] Configurar testes
     ```

### 2. Automação Funciona Automaticamente
Ao criar o Epic, o sistema:
- ✅ Cria 4 Features automaticamente
- 🏷️ Aplica labels baseadas na prioridade e tipo
- 📊 Gera checklist no Epic com progresso 0/4 (0%)
- 🔗 Cria links bidirecionais entre Epic e sub-issues

### 3. Acompanhe o Progresso
Conforme você trabalha nas sub-issues:
- ✅ Fechar sub-issue → Epic atualizado automaticamente
- 📊 Progresso visual: `2/4 (50%) 📈`  
- 🎉 100% completo → Epic fecha automaticamente
- 🔄 Reabrir sub-issue → Epic reabre automaticamente

## 💡 Exemplo Prático

**Epic Criado:**
```
[Epic] Sistema de Autenticação
```

**Sub-issues Automáticas:**
```
✅ #123 [Feature] Implementando ambiente desenvolvimento
✅ #124 [Feature] Criar API de autenticação  
✅ #125 [Feature] Implementar tela de login
✅ #126 [Feature] Configurar testes
```

**Progresso Automático:**
```
📊 Epic atualizado: 0/4 (0%) ⏳
✅ #123 fechada → 1/4 (25%) 📊
✅ #124 fechada → 2/4 (50%) 📈  
✅ #125 fechada → 3/4 (75%) 🚀
✅ #126 fechada → 4/4 (100%) 🎉 Epic fechado!
```

## 🔧 Configuração

### Labels Necessárias
Crie as seguintes labels no repositório:
```
epic, feature, task, sub-issue
prioridade-baixa, prioridade-media, prioridade-alta, prioridade-critica
frontend, backend, fullstack, infrastructure, design, testing
```

### Permissões do Workflow
Os workflows precisam de:
- ✅ `issues: write` - Para criar/editar issues
- ✅ `contents: read` - Para ler templates
- ✅ `metadata: read` - Para acessar contexto

## 🎯 Diferenças do Sistema Anterior

| Recurso | ❌ Antes | ✅ Agora |
|---------|----------|----------|
| **Relacionamentos** | Apenas texto | Links bidirecionais reais |
| **Progresso** | Manual | Automático com % visual |
| **Fechamento** | Manual | Epic fecha automaticamente |
| **Labels** | Básicas | Sistema completo organizado |
| **Visibilidade** | Limitada | Dashboard visual completo |

## 📚 Documentação Completa

Para guia detalhado de uso, veja: **[AUTOMATION_GUIDE.md](./AUTOMATION_GUIDE.md)**

## 🤝 Contribuindo

1. 🍴 Fork este repositório
2. 🔧 Teste as automações  
3. 💡 Sugira melhorias via Issues
4. 🚀 Submeta Pull Requests

## 📞 Suporte

Encontrou problemas? 
1. 🔍 Verifique o [Guia de Automação](./AUTOMATION_GUIDE.md)
2. 📋 Consulte logs em Actions
3. 🐛 Abra uma Issue descrevendo o problema

---

🎉 **Agora você tem sub-issues reais e automação completa de progresso!**
