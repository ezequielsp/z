# z

z is a JavaScript library to create HTML elements.

> A ideia básica é criar elementos no cliente
> dispensando o servidor de processar respostas em html. 
> Cada cliente é responsável por gerar sua interface com o usuário.
> Assim uma api fornece apenas os dados.

> The basic idea is to set the client information
> Eliminating the server to process responses in html.
> Each client is responsible for generating its user interface.
> Once an api provides only the data.


### Version
0.0.1

### Tech

É possível utilizar o método html do JQuery para fazer o mesmo e recentemente descobri
que o React também. Mas em nenhum dos dois casos a forma implementada me agradaram.
Não gostei da ideia de colocar tags html no retorno.

It's possible to use the jQuery method HTML to make the same, and recently, 
I figure it out that React do it also. 
I did not liked the idea of put HTML tags in the return.

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
var container = z.create('div', {'attr': {'id': 'container'}});

var div = z.create('div', {'text': "Hello John"});

z.append(container, div);
z.append(document.body, container);
```


* [React] - React is a JavaScript library for building user interfaces.
* [jQuery] - Method html


## Installation

Download and use.

```html
<!-- The core React library -->
<script src="path/to/file/z.min.js"></script>
```

## Creating Bootstrap Buttons

```js
var body = document.body;

var btn = z.create('button', {
  'attr': {'id': 'btn-edit', 
    'class': 'btn btn-success', 
    'type': 'button', 
    'onclick': "alert('Hello world!')",
    'data-reserv-id': 33
  },
  'text': 'Click Me!'
});

body.appendChild(btn);

var save = z.create('button', {
  'attr': {
    'class': 'btn btn-primary', 
    'type': 'button'
  },
  'text': 'Salvar'
});

body.appendChild(save);
```


### Todos

 - Write Tests
 - To implement hash Tables

License
----

MIT


**Free Software, Hell Yeah!**

### Kudos

* [Underscore] - All kudos.

   [React]: <https://facebook.github.io/react/>
   [jQuery]: <http://api.jquery.com/html/>
   [Underscore]: <http://underscorejs.org/>
   


