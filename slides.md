---
theme: seriph
background: ./images/buildings.jpg
class: 'text-center'
highlighter: shiki
lineNumbers: false
info: |
  Slide para a apresentação da masterclass de POO para a rede Beyond Trybe
drawings:
  persist: false
css: unocss
---

# POO Masterclass

Entendendo melhor a Programação Orientada a Objetos

<!--
André
- Dar boa noite ao pessoal
- Agradecer pela presença
- Comentar sobre o tema da masterclass
- Deixar as apresentações para o próximo slide
-->

---
layout: two-cols
title: Quem somos
---

# André Vicente

<img src="images/andre.jpg" class="h-40 mb-5 rounded shadow" />

André Vicente é Técnico em Eletrônica, Analista de Sistemas e quase Engenheiro de Computação. Adora programar e ensinar programação. Adora animes também. Não tem horas vagas, mas de vez em quando perde umas partidas CS:GO. Hoje é Analista de Currículo na Trybe.


::right::


# Thays Costa

<img src="images/thays.jpg" class="h-40 mb-5 rounded shadow" />

Contadora de formação e programadora formada pela Trybe na turma 07, é uma entusiasta da participação feminina na área da tecnologia e apaixonada por livros, quadrinhos e heavy metal.

<style>
 .slidev-layout {
  margin-right: 10px;
}
</style>

---
layout: quote
class: 'text-white'
---

# Definição

&nbsp;

Programação orientada a objetos é um paradigma de programação baseado no conceito de "objetos", que podem conter dados na forma de campos, também conhecidos como atributos, e códigos, na forma de procedimentos, também conhecidos como métodos. [^1]

[^1]: [Programação orientada a objetos - Wikipedia](https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_orientada_a_objetos)

<!-- Thays -->
---
layout: image-right
image: ./images/forest.jpg
---

# História

&nbsp;

<!-- Fica por último -->
<!-- Falar que é um paradigma, e nem todo mundo/todo projeto precisa seguir -->
<!-- André -->

---
layout: two-cols
title: Classes e Objetos
---

# Classes

<v-clicks>

- Dão forma aos objetos
- São abstratas
  - 💡Isso não tem a ver com "classes abstratas", que serão vistas mais à frente
- Definem atributos e comportamentos
- É o caso genérico
- Exemplo: Classe Pessoa

</v-clicks>

::right::

# Objetos

<v-clicks>

- São instâncias da classe
- São concretos
- Possuem valores diferentes nos atributos
- É o caso específico
- Exemplo: André, que é uma pessoa

</v-clicks>

<!-- André -->
---

# Atributos e métodos

<v-clicks>

- Atributos são variáveis dentro do contexto de uma classe/objeto
- Métodos são funções dentro do contexto de uma classe/objeto

</v-clicks>

<!-- André -->
---

# Método construtor

&nbsp;

O método construtor é o responsável por fazer a inicialização dos objetos.  
Nele ocorrem todos os passos para que o nosso objeto seja criado com sucesso.

<!-- Thays -->
---
layout: two-cols
title: Classes
---

# Classes em Python

```python {all|3,5,7}
# Utiliza-se a palavra reservada `class` seguida
# do nome da classe para criá-la
class Person:
    # Método "construtor"
    def __init__(self):
        # Não faz nada
        pass 
```

::right::

# Classes em TypeScript

```typescript {all|3,5,7-8}
// Utiliza-se a palavra reservada `class` seguida
// do nome da classe para criá-la, seguida de chaves
class Person {
    // Método construtor
    constructor() {
        // Não faz nada
    }
}
```

<!-- Thays -->
--- 
layout: two-cols
title: Objetos
--- 

# Objetos em Python

```python
class Person:
    def __init__(self, name: str, age: int):
        self.name = name
        self.age = age

    def saudação(self, message: str):
        print(f"{self.name}: {message}")


andre = Person("André", 23)
thays = Person("Thays", 30)

print(andre.name) # Saída: André
thays.saudação("Olar!") # Saída: Thays: Olar!
```

::right::

# Objetos em TS

```typescript
class Person {
    public name: string;
    public age: number;

    constructor(name: string, age: number) {
        this.name = name;
        this.age = age;
    }

    saudação(message: string) {
        console.log(`${this.name}: ${message}`);
    }
}

const andre = new Person("André", 23);
const thays = new Person("Thays", 30);

console.log(thays.name); // Saída: Thays
andre.saudação("Hellou"); // Saída: André: Hellou
```

<!-- André 

Pontos a comentar:
- Construtor
- Atributos da instância
  - Nomes dos parâmetros do construtor não precisam ser iguais aos nomes dos atributos
- `self` e `this`
- Criação dos objetos
- Acesso aos atributos
- Acesso aos métodos

-->
---

# Pilares

&nbsp;

A Orientação a Objetos possui quatro pilares muito importantes:

<v-clicks>

- Abstração
- Encapsulamento
- Herança
- Polimorfismo

</v-clicks>

<!-- Thays -->
---

# Encapsulamento

&nbsp;

Garante que atributos ou métodos não sejam visíveis para fora da classe, fazendo com que não seja possível manipulá-los em outro lugar que não dentro dos métodos da própria classe.  

O encapsulamento utiliza os modificadores de visibilidade dos atributos e métodos para garantir que eles só poderão ser acessados nos locais corretos.  
Os modificadores podem variar de linguagem pra linguagem:

<v-clicks>

- public
- private
- protected
- readonly (no TypeScript)

</v-clicks>

<!-- Thays 

Os modificadores mais comuns são os 3 primeiros

-->

---
layout: two-cols
title: Encapsulamento - Exemplo
---

# Python

```python {3|4|5|all}
class Person:
    def __init__(self, name: str, age: int, height: int):
        self.name = name # público
        self._age = age # privado (convenção)
        self.__height = height # privado

    def print_height(self):
        print(self.__height)


andre = Person("André", 23, 176)
print(andre.name) # Saída: André
print(andre._age) # Saída: 23
andre.print_height() # Saída: 176
```

::right::

# Typescript

```typescript {none|3|4|5|all}
class Person{
    public name: string;
    private _age: number;
    protected _height: number;
    readonly heightTimesAge: number;

    constructor(name: string, age: number, height: number) {
        this.name = name;
        this._age = age;
        this._height = height;
        this.heightTimesAge = height * age;
    }

    printAge() {
        console.log(this._age)
    }
}

const thays = new Person("Thays", 30, 201)
console.log(thays.name) // Saída: Thays
thays.printAge() // Saída: 30
```

---

# Abstração

&nbsp;

A abstração é a capacidade de criar uma forma simples de interagir com os objetos sem precisar entender como ele faz as coisas.  

Se trata do código que usa sua classe não precisar saber como ela funciona, para que ela possa mudar sem interferir nele.

<!-- André

Por exemplo um método `enviar` dentro de um objeto da classe `email` pode ser chamado passando a mensagem e a pessoa destinatária, e você não precisa saber como esse e-mail é enviado.  
Tudo o que você precisa fazer é chamar o método correto com os parâmetros corretos.  
Um ponto muito importante a ser ressaltado é que a abstração não é feita pensada necessariamente para a pessoa que vai utilizar a classe, mas para o código que vai utilizá-la.  
Se seu código fora da classe `email` precisa entender detalhes de funcionamento do protocolo SMTP para enviar o email, você não está criando as abstrações da forma correta, por mais que você saiba usar o SMTP.  
   -->
---

# Interfaces

<!-- André -->
---

# Herança

<!-- Thays -->
---

# ~~Poliformismo~~ Polimorfismo

<!-- André -->
---

# Exemplos

---

# SOLID

<!-- Thays -->
---

# Single Responsibility Principle

<!-- Thays -->
---

# Open/Closed Principle 

<!-- André -->
---

# Liskov's Substitution Principle

<!-- André -->
---

# Interface Segregation Principle

<!-- Thays -->
---

# Dependency Injection

<!-- Thays -->
---

# Dependency Inversion Principle

<!-- André -->
---

# Exemplos

---

# Fontes

---
layout: fact
title: Encerramento
---

# Obrigueido!

<!-- É obrigueido mesmo
Referência: https://youtu.be/Lv0RmiLgRA4 -->
