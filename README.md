# z

z is a JavaScript library to create HTML elements.

  - Type some Markdown on the left
  - See HTML in the right
  - Magic

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]

> A ideia básica é criar elementos no cliente
> dispensando o servidor de processar respostas em html. 
> Cada cliente é responsável por gerar sua interface com o usuário.
> Assim uma api fornece apenas os dados.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Version
1.0.0

### Tech

É possível utilizar o método html do JQuery para fazer o mesmo e recentemente descobri
que o React também. Mas em nenhum dos dois casos a forma implementada me agradaram.
Não gostei da ideia de colocar tags html no retorno.

It's possible to use the jQuery method HTML to make the same, and recently, I figure it out that React do it also. I did not liked the idea of put HTML tags in the return.

## Examples Jquery

```script
$( "#container" ).html( '<div>Hello John</div>' );
```

## Examples React

```js
var HelloMessage = React.createClass({
  render: function() {
    return <div>Hello {this.props.name}</div>;
  }
});

ReactDOM.render(
  <HelloMessage name="John" />,
  document.getElementById('container')
);
```
This example will render "Hello John" into a container on the page.

## Examples Z

```js
var div = z.create('div');
    div.val("Hello John");
  
z( "#container" ).append(div);
```

E se eu quisesse criar várias divs com textos diferentes, faria um metodo:

```js
var createDiv = function(class, text) {
    var div = z.create('div', [['className':class]]);
        div.val(text);
    
    return div;
}

var div = z.createDiv("otheCommentBox", "Hello, world! I am a Other CommentBox");
z( "div" ).append(div);
```


* [React] - React is a JavaScript library for building user interfaces.
* [jQuery] - Method html


## Installation

Download and use.

```html
<!-- The core React library -->
<script src="path/to/file/z.min.js"></script>
```


### Todos

 - Write Tests
 - To implement hash Tables

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [React]: <https://facebook.github.io/react/>
   [jQuery]: <http://api.jquery.com/html/>
   


