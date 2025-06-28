**Pseudoclasses** são os *estados* de um *elemento*. Basicamente eles são ativados após uma certa ação ou condição for cumprida, dependendo da pseudoclasse usada.
Alguns exemplos de pseudoclasses:

[Hover] -> Ativa ao passar o mouse em cima do mesmo.

[Visited] -> Usado em links, ativa quando o link ja foi visitado.

[Active] -> Ativa ao ser clicado.

```pseudoclass
a::hover{
	font-size: 3em;
}
```

## Pseudoelementos

**Pseudoelementos** são estilos que podem ser postos entre conteúdos, criando meio que um padrão para aquela tag.

```pseudoelement
a::before{
	content: '\1F517'
}
a::after {
	content: '<'
}
```

Isso faz com que essas setas sejam posicionadas, respectivamente, **ANTES** de um link e **DEPOIS** de um link. Elas podem parecer algo do html (conteúdo) mas ele é usado mais para decorar o conteúdo do que adicionar conteúdo em sí.