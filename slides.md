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

<v-clicks>

- Funciona como uma espécie de contrato a ser implementado em uma classe
- Determina as assinaturas dos métodos e quais atributos devem ser **obrigatoriamente** implementados
- Não há implementação de código
- Não pode ser instanciada

</v-clicks>

<!-- Após isso, mostrar exemplo de código  
Lembrar o André de falar sobre classes abstratas -->
---

# Herança

<v-clicks>

- É inerente à Classe, não ao objeto
- Permite especificação de classes
- Onde um objeto da superclasse é esperado, um objeto da subclasse pode ser passado

</v-clicks>

<!-- Thays

- Quando a classe A implementa a interface I, ela deve implementar todos os métodos declarados em I e possuir todos os atributos de I. 

- Quando a classe A herda da classe B, ela já herda todos os métodos e atributos públicos ou protegidos implementados na classe B.

-->

---
layout: quote
class: 'text-white' 
---

# ~~Poliformismo~~ Polimorfismo

&nbsp;

Polimorfismo é o princípio pelo qual duas ou mais classes derivadas de uma mesma superclasse podem invocar métodos que têm a mesma identificação (assinatura) mas comportamentos distintos, especializados para cada classe derivada, usando para tanto uma referência a um objeto do tipo da superclasse. [^1]

[^1]: [Programação orientada a objetos - DCA Unicamp](https://www.dca.fee.unicamp.br/cursos/PooJava/polimorf/index.html#:~:text=Polimorfismo%20%C3%A9%20o%20princ%C3%ADpio%20pelo,objeto%20do%20tipo%20da%20superclasse.)

<!-- 
Ressaltar que não é Poliformismo  
Explicar que significa "várias formas"  

Depois daqui exemplo de código  
Lembrar o André de falar sobre atributos protegidos em classes herdadas

Após isso, fazer uma pausa de 10 minutos -->
---

# SOLID

&nbsp;

É um acrônimo para 5 princípios.  
Nem todos são restritos à POO, mas é juntamente com ela que dão mais certo.  
É bom cumprir todos os 5 ao mesmo tempo!  

<v-clicks>

- Single Responsibility Principle
- Open/Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependency Inversion Principle

</v-clicks>

<!-- 
Ajudam a organizar código, melhorar legibilidade e facilitar manutenção  
São boas práticas
-->
---

# Single Responsibility Principle

<v-clicks>

- Diz que uma entidade (classe, método, função, etc) deve ter apenas uma única responsabilidade
- Implica que a entidade só deve possuir um motivo para ser alterada
- A entidade tende a fazer aquela coisa que ela faz de forma bem feita
- Garante diminuição de complexidade
- Ajuda na legibilidade
- Favorece a reutilização

</v-clicks>

<!-- 
Exemplo: Componentes React
-->
---

# Open/Closed Principle 

<v-clicks>

- Diz que entidades de software devem ser abertas para extensão, mas fechadas para modificação
- Permite que o código seja mais flexível
- Permite acrescentar comportamentos sem alterar as entidades existentes
- É mais simples de entender com exemplo prático, então vamos ver um

</v-clicks>

<!-- André fala essa parte  
Em seguida, um exemplo prático -->
---

# Liskov's Substitution Principle

<v-clicks>

- Diz que objetos em um programa devem ser substituíveis por instâncias de seus subtipos, sem alterar a funcionalidade do programa
- Os parâmetros de entrada dos métodos das subclasses não podem ser mais específicos
- Os valores de retorno dos métodos das subclasses não podem ser mais abrangentes

</v-clicks>

<!-- André fala essa parte  
Após aqui, um exemplo prático -->
---

# Interface Segregation Principle

<v-clicks>

- Diz que interfaces específicas são melhores do que uma única interface para todos os propósitos
- Diz que não se deve forçar a implementação de métodos que não serão utilizados
- Consiste em separar uma interface complexa em várias mais simples, que podem ser reutilizadas mais vezes
- Uma classe pode implementar várias interfaces, caso seja necessário

</v-clicks>

<!-- Thays -->
---

# Dependency Injection

<v-clicks>

- Não é um princípio
- Diz que as dependências devem ser passadas como parâmetro, ao invés de serem criadas diretamente dentro da entidade que as usa
  - Você pode manter um `valor padrão` para facilitar o uso

</v-clicks>

<!-- Thays -->
---

# Dependency Inversion Principle

<v-clicks>

- Diz que entidades de alto nível não devem depender de entidades de baixo nível. Ambos devem depender de abstrações
- Facilita a alteração das implementações concretas de dependências
- Facilita o uso de mocks nos testes

</v-clicks>

<!-- André 

Após isso, exemplo  
Lembrar o André de falar do valor padrão na injeção/inversão de dependências
-->

---
layout: fact
title: Encerramento
---

# Obrigueido!

<!-- É obrigueido mesmo
Referência: https://youtu.be/Lv0RmiLgRA4 -->
