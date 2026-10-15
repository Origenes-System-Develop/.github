# Contribuindo

## Quem Pode Contribuir

- Cada projeto pertence a uma turma.
- Somente alunos da turma dona do projeto alteram o repositório.
- Alunos de outras turmas podem ler, clonar e estudar o código, mas não enviam alterações.
- O líder da turma gerencia o repositório e aprova os Pull Requests.

## Fluxo De Branches

~~~text
branch padrão
  ^
feature/nome-da-funcionalidade
~~~

- Branch padrão: única branch de longa duração, protegida. Somente código estável.
- `feature/*` (ou `fix/*`): trabalho isolado por funcionalidade ou correção, nasce da branch padrão e morre após o merge.

Não fazer push direto na branch padrão. PR obrigatório.

## Criar Feature Branch

~~~bash
git checkout <branch-padrao>
git pull
git checkout -b feature/nome-da-funcionalidade
~~~

## Antes Do Pull Request

- Rode os testes, o lint e o build do projeto, quando existirem.
- Confira que não há arquivo `.env`, senha, token ou segredo no commit.

## Pull Request

- Explique o problema resolvido.
- Liste mudanças principais.
- Informe testes executados.
- Aponte riscos.
- O líder da turma é pedido como revisor e precisa aprovar antes do merge.

## Revisão De Código

Priorize:

- bugs e regressão de regra de negócio
- validação de entrada
- vazamento de segredo ou senha
- testes
- documentação afetada

## Padrão De Commit

- `feat: adiciona módulo de notas`
- `fix: corrige fluxo de status`
- `docs: atualiza README`
- `test: cobre login inválido`
- `refactor: isola repositório de alunos`
