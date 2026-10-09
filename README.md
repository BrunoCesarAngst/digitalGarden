# Jardim Digital de Engenharia

Um espaço público de Bruno César Angst para registrar raciocínios, decisões e estudos sobre construção de software.

Este repositório reúne estudos de caso e notas de engenharia. Parte do conteúdo parte de experiências profissionais e apresenta apenas raciocínios generalizáveis, sem expor código, dados ou detalhes internos de empresas. Outros textos registram investigações e aprendizado.

> Complexidade não deve ser escondida. Deve ser modelada, explicada e controlada.

## Comece pelos estudos de caso

| Estudo | O que permite avaliar | Natureza |
| --- | --- | --- |
| [Design System empresarial](case-studies/design-system-empresarial.md) | Componentes reutilizáveis, estados de interface, contratos e manutenção | Experiência profissional relatada, sem código proprietário |
| [Automação segura de revisão](case-studies/automacao-segura-de-revisao.md) | Isolamento de worktrees, autorização e rastreabilidade | Estudo técnico de uma camada de apoio ao desenvolvimento |
| [Editor visual de regras](case-studies/editor-visual-de-regras.md) | Modelagem de domínio, estados, contratos e interação | Estudo de caso sanitizado |

**Como ler:** são relatos de decisões e competências, não demos executáveis, certificações de resultado ou divulgação de produtos empresariais.

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
