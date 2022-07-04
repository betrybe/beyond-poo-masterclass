---
theme: seriph
background: ./images/buildings.jpg
class: 'text-center'
highlighter: shiki
lineNumbers: true
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

- Analista de currículo na Trybe
- Analista de Sistemas
- Adora Python, animes


::right::


# Thays Costa

<img src="images/thays.jpg" class="h-40 mb-5 rounded shadow" />

- Analista de currículo na Trybe
- Beyonder
- Adora back-end, dormir e gatos

---
layout: quote
class: 'text-white'
---

# Definição

Programação orientada a objetos é um paradigma de programação baseado no conceito de "objetos", que podem conter dados na forma de campos, também conhecidos como atributos, e códigos, na forma de procedimentos, também conhecidos como métodos. [^1]

[^1]: [Programação orientada a objetos - Wikipedia](https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_orientada_a_objetos)

<!-- Thays -->
---
layout: image-right
image: ./images/forest.jpg
---

# História

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

<style>
 .slidev-code {
  margin-right: 10px;
}
</style>

<!-- Thays -->
--- 

# Objetos

<!-- André -->
---

# Pilares

<!-- Thays -->
---

# Encapsulamento

<!-- Thays -->
---

# Abstração

<!-- André -->
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
