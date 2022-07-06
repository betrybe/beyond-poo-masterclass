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
aspectRatio: '21/9'
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

Contadora de formação e programadora formada pela Trybe na turma 07, é uma entusiasta da participação feminina na área da tecnologia e apaixonada por livros, quadrinhos e heavy metal. Hoje é Analista de Currículo na Trybe.

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

<!-- Comentar que POO não é a solução para todos os problemas.  
Existem lugares para outros paradigmas. -->

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

<!-- Após isso, mostrar código de exemplo sobre a sintaxe básica de criação de classes e de objetos -->
---

# Atributos e métodos

<v-clicks>

- Atributos são variáveis dentro do contexto de uma classe/objeto
- Métodos são funções dentro do contexto de uma classe/objeto

</v-clicks>

---

# Método construtor

&nbsp;

O método construtor é o responsável por fazer a inicialização dos objetos.  
Nele ocorrem todos os passos para que o nosso objeto seja criado com sucesso.

<!-- Após isso, mostrar código de exemplo sobre atributos, métodos e método construtor -->
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
Comentar brevemente sobre cada um deles

Privado só pode ser lido/alterado dentro da classe que o define  
Protegido é tipo o privado, mas funciona nas subclasses, só que não pode ser acessado pelas instâncias

-->

---

# Abstração

&nbsp;

A abstração é a capacidade de criar uma forma simples de interagir com os objetos sem precisar entender como ele faz as coisas.  

Se trata do código que usa sua classe não precisar saber como ela funciona, para que ela possa mudar sem interferir nele.

<!-- 
Por exemplo um método `enviar` dentro de um objeto da classe `email` pode ser chamado passando a mensagem e a pessoa destinatária, e você não precisa saber como esse e-mail é enviado.  
Tudo o que você precisa fazer é chamar o método correto com os parâmetros corretos.  
Um ponto muito importante a ser ressaltado é que a abstração não é feita pensada necessariamente para a pessoa que vai utilizar a classe, mas para o código que vai utilizá-la.  
Se seu código fora da classe `email` precisa entender detalhes de funcionamento do protocolo SMTP para enviar o email, você não está criando as abstrações da forma correta, por mais que você saiba usar o SMTP.  

-->
---

# Interfaces

- Funciona como uma espécie de contrato a ser implementado em uma classe;
- Determina as assinaturas dos métodos e quais atributos devem ser **obrigatoriamente** implementados;
- Não há implementação de código;
- Não pode ser instanciada;
- A palavra-chave `implements` marca a implementação de uma interface por uma classe.

</v-clicks>

<!-- Após isso, mostrar exemplo de código -->
---

# Herança

<v-clicks>

- É inerente à Classe, não ao objeto;
- Permite especificação de classes;
- Onde um objeto da superclasse é esperado, um objeto da subclasse pode ser passado;
- A palavra-chave `extends` marca a utilização da Herança.

</v-clicks>

<!-- Thays

- Quando a classe A implementa a interface I, ela deve implementar todos os métodos declarados em I e possuir todos os atributos de I. 

- Quando a classe A herda da classe B, ela já herda todos os métodos e atributos públicos ou protegidos implementados na classe B.

-->
---

# ~~Poliformismo~~ Polimorfismo

<!-- 
Depois daqui exemplo de código
Lembrar o André de falar sobre atributos protegidos em classes herdadas

Após isso, fazer uma pausa de 10 minutos -->
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
