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
- Dar boa tarde/boa noite ao pessoal
- Agradecer pela presença
- Comentar sobre o tema da masterclass
- Deixar as apresentações para o próximo slide
-->


---
layout: two-cols
title: Quem somos
---

# André Vicente

- Analista de currículo na Trybe

::right::


# Thays Costa

- Analista de currículo na Trybe

---
layout: quote
class: 'text-white'
---

# Definição

Programação orientada a objetos é um paradigma de programação baseado no conceito de "objetos", que podem conter dados na forma de campos, também conhecidos como atributos, e códigos, na forma de procedimentos, também conhecidos como métodos. [^1]

[^1]: [Programação orientada a objetos - Wikipedia](https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_orientada_a_objetos)

---
layout: image-right
image: ./images/forest.jpg
---

# História

---
layout: two-cols
title: Classes e Objetos
---

# Classes

<v-clicks>

- Dão forma aos objetos
- São abstratas
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

---

# Atributos e métodos

<v-clicks>

- Atributos são variáveis dentro do contexto de uma classe/objeto
- Métodos são funções dentro do contexto de uma classe/objeto

</v-clicks>

---


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

--- 

# Objetos

---

# Pilares

---

# Encapsulamento

---

# Abstração

---

# Herança

---

# Polimorfismo

---

# Exemplos

---

# SOLID

---

# Single Responsibility Principle

---

# Open/Closed Principle 

---

# Liskov's Substitution Principle

---

# Interface Segregation Principle

---

# Dependency Injection

---

# Dependency Inversion Principle

---

# Exemplos

---

# Fontes

---

# Encerramento

