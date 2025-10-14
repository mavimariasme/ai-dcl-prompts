# Regras do Fluxo de Trabalho Git

## Diretrizes de Commit

1. **Commits Frequentes**
   - Faça commits git após cada alteração significativa no código
   - Cada commit deve representar uma única alteração lógica
   - Mantenha os commits pequenos e focados em uma tarefa específica

2. **Mensagens de Commit**
   - Use mensagens de commit claras e descritivas
   - Siga o formato: `<tipo>: <descrição>`
   - Tipos incluem: feat, fix, docs, style, refactor, test, chore
   - Exemplo: `feat: implementa lógica de validação de palavras`

3. **Quando Fazer Commit**
   - Após implementar uma nova funcionalidade
   - Após corrigir um bug
   - Após refatorar código
   - Após escrever testes
   - Após atualizar documentação
   - Sempre que uma alteração significativa e funcional for feita

## Estratégia de Branches

1. **Branch Principal**
   - O branch `main` deve sempre conter código estável, pronto para produção
   - Commits diretos no `main` são proibidos, exceto para hotfixes
   - Todo trabalho de desenvolvimento deve ocorrer em branches de feature

2. **Branches de Feature**
   - Crie um novo branch para cada funcionalidade ou issue
   - Convenção de nomenclatura: `feature/<nome-da-feature>` ou `fix/<nome-do-issue>`
   - Exemplo: `feature/validacao-palavra` ou `fix/entrada-teclado`

3. **Fluxo de Desenvolvimento**
   - Crie um branch de feature a partir do `main`
   - Faça alterações e commits no branch de feature
   - Mantenha branches de feature atualizados com o `main` através de rebase
   - Quando a feature estiver completa, faça rebase no último `main` antes de mergear

## Processo de Merge

1. **Revisão de Código**
   - Todo código deve ser revisado antes do merge com `main`
   - Resolva todos os comentários da revisão antes de prosseguir

2. **Rebase e Merge**
   - Faça rebase do branch de feature no último `main` para garantir histórico limpo
   - Resolva quaisquer conflitos durante o rebase
   - Use merge `--ff-only` para manter histórico linear
   - Exemplo de fluxo:
     ```bash
     git checkout feature/minha-feature
     git rebase main
     git checkout main
     git merge --ff-only feature/minha-feature
     ```

3. **Limpeza**
   - Delete branches de feature após merge bem-sucedido
   - Mantenha o repositório limpo de branches obsoletos

## Melhores Práticas

1. **Pull Antes de Push**
   - Sempre faça pull das últimas alterações antes de fazer push para o remote
   - Resolva quaisquer conflitos localmente

2. **Commits Atômicos**
   - Cada commit deve deixar o código em estado funcional
   - Divida grandes alterações em commits menores e lógicos

3. **Nunca Reescreva Histórico Público**
   - Só faça rebase em branches que não foram compartilhados com outros
   - Se um branch já foi enviado e compartilhado, crie um novo commit em vez de fazer amend

4. **Faça Commit Cedo e Frequentemente**
   - Faça commits pequenos e incrementais em vez de grandes alterações
   - Isso facilita a depuração e revisão de código
