# Decisões arquiteturais precisam sobreviver ao código

**Estado:** estável  
**Tema:** arquitetura, documentação e governança

Código registra a solução escolhida, mas raramente preserva o problema original, as alternativas avaliadas e as restrições que tornaram aquela escolha razoável.

Quando esse contexto desaparece, decisões antigas parecem arbitrárias. A equipe volta a discutir o mesmo tema ou remove uma restrição sem perceber o risco que ela controlava.

## O que uma decisão precisa registrar

Uma decisão técnica relevante deve responder, no mínimo:

1. Qual problema está sendo resolvido?
2. Quais forças e restrições influenciam a escolha?
3. Quais alternativas foram consideradas?
4. Qual opção foi adotada?
5. Quais consequências são aceitas?
6. O que invalidaria essa decisão no futuro?

## Estrutura mínima

```md
# ADR-XXX — Título da decisão

Status: proposta | aceita | substituída | revogada
Data: AAAA-MM-DD

## Contexto

## Decisão

## Alternativas consideradas

## Consequências

## Critérios de revisão
```

## Fato, hipótese e decisão não são equivalentes

Um documento técnico perde valor quando mistura categorias diferentes:

- **fato:** comportamento observado ou contrato existente;
- **hipótese:** explicação ainda não confirmada;
- **decisão:** escolha normativa adotada;
- **preferência:** caminho desejado, mas não obrigatório;
- **pendência:** trabalho necessário ainda não concluído.

Nomear essas categorias reduz ambiguidades e impede que uma proposta seja tratada como contrato.

## Uma ADR não substitui o código

A documentação deve indicar intenção e consequências. O código, os testes e os contratos executáveis continuam sendo a verificação concreta.

Uma boa decisão costuma possuir quatro representações alinhadas:

```text
ADR → contrato → implementação → teste
```

Quando uma delas diverge, existe dívida de governança.

## Revogação é parte do sistema

Decisões não precisam ser eternas. Precisam ser rastreáveis.

Ao substituir uma decisão:

- preserve o registro anterior;
- marque seu estado como substituído ou revogado;
- indique a nova decisão;
- explique qual premissa mudou;
- ajuste contratos e testes afetados.

## Regra prática

Documente decisões quando o custo de esquecê-las for maior do que o custo de registrá-las.

Isso normalmente inclui:

- contratos entre sistemas;
- modelos de estado;
- persistência e migração;
- compatibilidade;
- segurança;
- limites entre módulos;
- estratégias de publicação e reversão;
- decisões que restringem possibilidades futuras.

---

Arquitetura não é apenas a estrutura do software. É o conjunto de decisões que preserva a capacidade de evoluí-lo conscientemente.
