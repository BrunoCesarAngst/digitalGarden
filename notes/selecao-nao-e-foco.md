# Seleção não é foco

**Estado:** estável  
**Tema:** arquitetura front-end, interação e acessibilidade

Em interfaces simples, seleção e foco frequentemente parecem a mesma coisa. Em editores visuais, árvores, tabelas avançadas e fluxos recursivos, tratá-los como um único estado produz inconsistências difíceis de corrigir.

## A distinção

**Seleção** responde:

> Qual entidade do domínio está ativa?

**Foco** responde:

> Em qual alvo interativo a próxima entrada será aplicada?

Um nó pode continuar selecionado enquanto o foco está em um campo, botão, editor embutido ou opção transitória pertencente a ele.

## O erro comum

Um desenho frequente mantém apenas algo como:

```ts
const noSelecionadoId = ref<string | null>(null)
```

Depois, tenta deduzir desse identificador:

- qual campo está ativo;
- se o usuário entrou no nó;
- se um editor está aberto;
- para onde `Escape` deve retornar;
- o que `Enter`, `Tab` ou as setas devem fazer.

O resultado é uma coleção crescente de booleanos e condicionais locais. Mouse e teclado passam a operar modelos diferentes da mesma interface.

## Modelo preferível

Use endereços tipados para o foco:

```ts
type AlvoFocado =
  | { tipo: 'arvore' }
  | { tipo: 'no'; noId: string }
  | { tipo: 'campo'; noId: string; campo: string }
  | { tipo: 'editor'; noId: string; campo: string }
  | { tipo: 'opcao'; noId: string; campo: string; indice: number }
```

A seleção permanece independente:

```ts
interface EstadoDeInteracao {
  noSelecionadoId: string | null
  alvoFocado: AlvoFocado
}
```

## Consequências positivas

- mouse e teclado atualizam o mesmo estado;
- transições ficam explícitas e testáveis;
- `Escape` pode subir um nível de interação;
- `Enter` pode aprofundar a interação;
- seleção visual não desaparece ao editar um campo;
- acessibilidade deixa de ser um remendo posterior;
- o comportamento não precisa ser reconstruído a partir do DOM.

## Regra prática

Quando uma interface contém níveis de interação, modele esses níveis como uma máquina de estados ou união discriminada. Não use a existência de um elemento no DOM como fonte de verdade funcional.

## Critério de validação

Uma implementação está coerente quando o mesmo fluxo pode ser descrito desta forma:

```text
árvore → nó → campo → editor → opção
```

E cada avanço ou retorno possui:

- evento de entrada;
- estado de origem;
- estado de destino;
- efeito colateral permitido;
- teste correspondente.

---

A interface se torna previsível quando seleção, foco, edição e persistência deixam de competir pelo mesmo estado.
