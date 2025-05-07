
<.h1> -> Exemplo de título</.h1>
	<.h1>: Abertura de tag.
	Exemplo de título: Conteúdo.
	</.h1>: Fechadura de tag.


<.p1> -> Exemplo de Parágrafo <./p1>


<.div> ->Tag usada para agrupar blocos de elementos e aplicar CSS neles.


## Imagem em HTML
<.img src="foto.png" alt="Exemplo de foto">
	<img: Abertura de tag.
	src=: Parâmetro.
	"Exemplo de foto": Valor
	PS: em source (src), pode-se usar CTRL + SPACE para procurar a imagem que deseja.



Como mudar o ícone na guia
	Na parte de head, acima do titulo, escreva:
	"link", e então selecione a opção "favicon"
	na parte " href="" ", entre as aspas, aperte CTRL + SPACE e selecione seu ícone.
	para converter imagens para ícones, use o site [ícones](https://favicon.io/favicon-converter/)



[hr] -> Linha horizontal.

[br] -> Quebra de linha. (também funciona com imagens)

<!-- --> -> Comentários.

&.lt; e &.gt; -> Less Than (<) e Greater Than (>).

Tabela de Símbolos especiais:
	![[Pasted image 20241221111532.png]]

Emojis -> Para colocar emojis em html, SEMPRE comece com: &#x (x MÍNUSCULO)
em frente ao comando coloque o código do emoji, site: [Emojis](https://emojipedia.org)

O HTML possui uma hierarquia de títulos, onde h1 é o nível maior (normalmente o título), até o h6 (Conforme os tópicos são separados).

lorem -> tag usada para criar um texto qualquer, útil para testes.


## Como ENVELOPAR uma tag:
Selecione o que quer envelopar com o mouse
pressione CTRL + SHIFT + P
Emmet: Wrap with Abbreviation
Após confirmar, digite a tag (SEM os sinais <>)





## Formatação de Texto
São as várias tags usadas para dar algum valor especial para um texto:

[mark] -> Marcar uma parte do texto, como se fosse um marca texto.

[small] -> Letras miúdas de um contrato.

[del] -> Marca um texto como excluído, ele pode ser lido mas não é mais considerado.

[ins] -> Um texto com ênfase e indica que ele foi adicionado depois.

[sup] -> "subir" o texto, ex: x²

[sub] -> "descer" o texto, um exemplo seria elementos da tabela periódica, como o H2O

[code] -> Fonte "mono-espaçada", ela é ótima para ler códigos.

[pre] -> Considera as tabulações e quebras de linha de um texto, muito bom ao combinar com a tag [code].
ex:
	<pre>

			<code>
		num = int(input("Digite um número"))
	
		if num % 2 == 0:
	
			print(f'O número {num} é 'PAR')
	
		else:
	
			print(f'O número {num} é IMPAR')
		print('fim do programa')

		</code>

	</pre>


[q] -> semântica usadas para citações SIMPLES, de uma única linha.

[blockquote cite=""] -> É usado para citações com quebra de linha, além do comando "cite", que permite o uso de um link para o livro ou algo do tipo que direciona ao que estamos falando, mesmo que não mude nada visualmente, a parte interna do site vai saber quem está sendo referenciado.

[abbr] title="" -> Abreviações, em title, coloque o significado de sua abreviação, ex: HTML (HyperText Markup Language).

[bdo] -> Inversão de texto.












## Listas
[ol] -> Listas ordenadas.
	[li] para identificar cada item da lista.
	Parâmetro type: Mudar o tipo de contagem. (1, A, a, I, i)
	Parâmetro start: Mudar onde que começa a contagem. 
	**PS: NÃO IMPORTA O TIPO, O START SEMPRE É NUMÉRICO.**
	-
	**PS 2**: Se for necessário envelopar múltiplos itens (li), envelope todos eles de uma vez, escreva o [li] e depois use o *[*] (fica assim li*).
	-
	Ex: <.ol type="A" start="3">

[ul] -> Listas não ordenadas, ou seja, não são numeradas.
	[type=""] -> Mudar a forma da lista (circle, disc, square)

Se quiser editar mais de um comando ao mesmo tempo, você pode segurar ALT e clicar onde deseja fazer as mudanças.


[dl] -> Lista de Definições. É como se fosse um dicionário:
	Primeiro você coloca o termo: <.dt> (Definition Term)
	E depois a definição de tal termo: <.dd> (Definition Description)









## TRABALHANDO COM LINKS
[a] -> são chamados de âncoras, são usados na criação de hyperlinks.
	O principal parâmetro é o "href" (referência a hipertexto), que é onde fica o link.
	Outros parâmetros importantes são:
	[hreflang=""] -> Indica o principal idioma do site que está sendo referenciado. Isso permite que o navegador e os softwares lidem com a tradução automática por exemplo.
	-
	[target=""] -> Altera onde o site indicado vai abrir, o mesmo contém os seguintes valores:
		blank -> abre o link em uma nova janela em branco
		self -> Abre o link na janela atual (padrão)
		top -> desfaz os frames e abre o destino no navegador completo
		parent -> similar ao top, referência à janela mãe 
	-
	[rel=""] -> (relativo a) -> Indica qual "caminho" o link irá seguir
		external: link externo.
		next: Próxima página de um link interno.
		prev: Página anterior de um link interno.
	-
	Como navegar entre links internos em pastas diferentes? 
		href="./" -> própria pasta
		href="../" -> pasta anterior
		Para entrar em pastas é só usar CTRL + SPACE no href.
	-
	Como fazer links com download?
		Mesma coisa que o link normal, aperta CTRL + SPACE e seleciona o arquivo.
		O atributo "type" especifica o tipo do documento
		Para saber todos os types: [Types](https://www.iana.org/assignments/media-types/media-types.xhtml)
		O "download" especifica que o "target" será baixado quando clicado, e possui a opção de mudar o nome do download.
	-
	[title=""] -> Ele aparece quando você passa o mouse em cima do link







## IMAGENS DINÂMICAS
[picture] -> É o comando usado para criar imagens dinâmicas, ou seja, imagens que alteram de tamanho conforme o tamanho da tela ou dispositivo.
	<.source media> -> o padrão é o min, mas usaremos o [max-width], a imagem muda de tamanho conforme o tamanho específicado, se o site ficar menor que 1050 pixels, use a imagem média, por exemplo.  O min é o inverso disso, ele começa com uma imagem pequena e aumenta conforme o tamanho da tela.
	[srcset] é a imagem, o CTRL + SPACE não funciona aqui, então é preciso escrever manualmente o caminho, ex: "imagens/foto-g.png"
	[type] é o tipo de imagem, png, jpeg, etc.


## REPRODUÇÃO DE ÁUDIO
Podemos simplesmente usar o [audio] com [source] [type],  junto com o parâmetro [controls] (para fazer a ferramenta do áudio aparecer) e o [preload], em que o parâmetro recomendado é o "metadata", pois ele mostra as minutagens do áudio mas sem baixa-lo por completo, só se o usuário quiser ouvi-lo. 
ex: <.audio src="midia/audio.mp3" controls preload="metadata"
mas se quiser colocar varios tipos de fonte, podemos:
	-
	Usar o [audio] com o preload e controls
	colocar as tags [source], e alterar o type conforme o tipo do arquivo. Os tipos são: MP3, OGG e WAV.

## Vídeos
Formatos disponíveis: MP4, M4V, WEBM, OGV (os mais populares são MP4 e M4V).
	Para fazer vídeos podemos simplesmente usar a tag [video] e CTRL + SPACE.
	O vídeo provavelmente virá gigante na tela, mude o tamanho com o parâmetro [width]
	-
	Não esqueça do [controls], ele é necessário para que haja interação com o vídeo.
	-
	Similar a imagens dinâmicas, crie uma tag video e dentro dela coloque todas as [sources] que estiver usando. MP4, M4V, WEBM, etc... O mais recomendado é o M4V.
	-
	use o parâmetro [poster] na tag video, é onde fica a thumb.
	-
	Parâmetro [loop], loopar o vídeo.
	-
	Vídeos hospedados localmente com essa tag, podem e vão usar MUITO tráfego.



## Classes
Podemos criar ids e classes:
	Para criar ids, escreva [id=]"(nome do id)" dentro de uma tag.
	-
	Para criar classes, do mesmo jeito que anteriormente, escreva [.] e o nome da classe e aperte enter. Desse jeito a classe será criada e então será vinculada ao lugar que se encontra.



## Grouping Tags
Tags semânticas para organizar suas caixas.
	-
	Todos eles são vistos como divs, mas além de ser melhor para os mecanismos de buscas, é mais organizado.
	Elas são divs "especiais", divs semânticas. Elas são chamadas de **Grouping Tags**.
	-
	**Tags sem semântica:**
	[div] -> block
	[span] -> inline
	-
	**Tags com semântica:**
	[header] -> Cabeçalho.
	[nav] -> navegação, links, menu.
	-
	[main] -> Conteúdo principal.
	[footed] -> Rodapé.
	[section] -> Seção.
	[article] -> Artigo.
	[aside] -> Conteúdo relacionado ao artigo. (ex: Autor)

## Como posicionar suas Grouping Tags
Coloca as Tags direito por favor
	O [header] é o cabeçalho, normalmente lá ficam o Banner, logo, formulário de pesquisa, ícones e menu de navegação.
	-
	[nav] Agrupa o conjunto de links de navegação do site.
	-
	[main] É onde fica o conjunto principal da página.
	-
	[aside] Ficam informações relacionadas ao link principal.
	-
	[footer] É o rodapé do site, ele pode conter informações de autoria, direitos autorais, contato, mapa do site, links e documentos relacionados.
	-
	PS: Não faz merda, nav fica fora do header.
	-
	É possível ter mais de um [h1] em um site, por exemplo o título principal de um site no header e o título principal da matéria no main, ambos são aptos a usar o h1.





