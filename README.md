# Jardim Digital de Engenharia

Um espaço público de Bruno César Angst para registrar raciocínios, decisões e estudos sobre construção de software.

Este repositório não é uma coleção de respostas definitivas. É um sistema de trabalho: ideias começam incompletas, são confrontadas com casos reais e amadurecem conforme novas evidências aparecem.

> Complexidade não deve ser escondida. Deve ser modelada, explicada e controlada.

## Linhas de investigação

- arquitetura de software para domínios complexos;
- editores visuais e sistemas orientados a regras;
- modelagem de estados e interações de interface;
- contratos entre produto, front-end, back-end e dados;
- documentação e rastreabilidade de decisões;
- automação de desenvolvimento e revisão de código;
- ambientes Linux, polyrepos, worktrees e ferramentas de engenharia.

## Notas de engenharia

| Nota | Questão central |
| --- | --- |
| [Seleção não é foco](notes/selecao-nao-e-foco.md) | Como modelar navegação e edição em interfaces complexas sem misturar estados diferentes? |
| [Decisões arquiteturais precisam sobreviver ao código](notes/decisoes-arquiteturais.md) | Como preservar contexto, alternativas e consequências de uma decisão? |
| [Polyrepos e worktrees sem perder governança](notes/polyrepos-e-worktrees.md) | Como trabalhar em múltiplos repositórios mantendo isolamento e rastreabilidade? |

## Estudos de caso

| Estudo | Competência demonstrada |
| --- | --- |
| [Editor visual de regras](case-studies/editor-visual-de-regras.md) | Domínio, interação, AST, contratos e evolução incremental |
| [Automação segura de revisão de código](case-studies/automacao-segura-de-revisao.md) | Governança, isolamento, autorização e automação operacional |

## Princípios editoriais

1. Separar fatos, decisões, hipóteses e preferências.
2. Explicar o problema antes de apresentar a solução.
3. Registrar alternativas descartadas, não apenas a escolha final.
4. Evitar abstrações que não tenham uma responsabilidade clara.
5. Publicar apenas conteúdo sanitizado, sem código, nomes ou dados proprietários.

## Estado do conteúdo

As notas podem receber um destes estados:

- **semente** — hipótese inicial;
- **em cultivo** — texto em revisão e confronto com casos reais;
- **estável** — entendimento consolidado, ainda sujeito a evolução;
- **superado** — preservado como registro histórico, mas substituído por uma abordagem melhor.

---

[Site](https://brunoangst.com.br/) · [Perfil no GitHub](https://github.com/BrunoCesarAngst)
