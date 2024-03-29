# Lista_de_exercicios

# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como `` esta aqui com `  `` ou

````javascript
//esta aqui com ```
let a = 'olá';
let b = 10;
print(a);
````

- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove.

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

**a) Imprime os números pares de 1 a 10.** &larr;

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

---

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar().

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

**A) let carro = new Carro("Toyota");** &larr;

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

---

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

**A) 18** &larr;

B) 16

C) 14

D) 12

---

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`? \
**Resposta:**

**A)** ![Uma imagem](assets/ex04_1.PNG)

---

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca? \
**Resposta:**

**A)** ![Uma imagem](assets/ex05_1.PNG)

---

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

**A) "Olá, meu nome é João. Olá, meu nome é Maria."** &larr;

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

---

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:

- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:

- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

**Resposta:**

```
// Cria a classe "Animal" com os atributos "nome" e "idade"
class Animal {
	constructor(nome, idade) {
		this.nome = nome;
		this.idade = idade;
	}

	//Cria o método "descrever()", o qual imprime no console uma descrição contendo o nome e a idade do animal
	descrever() {
		console.log(`Este animal é um ${this.nome} e possui ${this.idade} anos.`);
	}
}

// Cria dois objetos da classe Animal, um chamado cachorro e outro chamado gato, com 2 e 3 anos, respectivamente
var cachorro = new Animal('cachorro', '2');
var gato = new Animal('gato', '3');

// Chama o método descrever() para o cachorro e para o gato
cachorro.descrever();
gato.descrever();
```

---

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:

- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):

- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:

- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:

- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

**Resposta:**

```
// Cria a classe "Animal" com os atributos "nome" e "idade"
class Animal {
	constructor(nome, idade) {
		this.nome = nome;
		this.idade = idade;
	}

	//Cria o método "descrever()", o qual imprime no console uma descrição contendo o nome e a idade do animal
	descrever() {
		console.log(`Este animal é um ${this.nome} e possui ${this.idade} anos.`);
	}
}

// Cria a classe "Gato" que herda os atributos de "Animal", adicionando o atributo "cor"
class Gato extends Animal {
	constructor(nome, idade, cor) {
		super();
		this.nome = nome;
		this.idade = idade;
		this.cor = cor;
	}

    // Cria o método "descrever()" com uma modificação exclusiva para os gatos
    descrever(){
        console.log(`Este animal é um ${this.nome} ${this.cor} e possui ${this.idade} anos.`)
    }

    //Cria o método "miar()" para os gatos, o qual imprime no console um miado
	miar() {
		console.log(`Miau`);
	}
}

// Cria objetos da classe // Cria dois objetos, um da classe Animal, chamado cachorro com 2 anos, e outro da classe Gato, chamado gato, com 3 anos e da cor laranja
var cachorro = new Animal('cachorro', '2');
var gato = new Gato('gato', '3', 'laranja');

// Chama os métodos descrever para o cachorro e para o gato
cachorro.descrever();
gato.descrever();

// Chama o método miar para o gato
gato.miar();

```

---

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:

- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:

- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:

- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:

- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

**Resposta:**
```
// Cria a classe "SomadorDeNotas" com o atributo "total", o qual armazenará a soma das notas
class SomadorDeNotas {
	constructor() {
		this.total = 0;
	}

	// Cria o método "adicionarNota", o qual soma a nota inserida ao total
	adicionarNota(nota) {
		this.total += nota;
	}

	// Cria o método "verTotal", o qual imprime no console a soma total de todas as notas
	verTotal() {
		console.log(this.total);
	}
}

// Cria um objeto da classe SomadorDeNotas
var somador = new SomadorDeNotas();

// Chama o método adicionarNota, passando vários valores para ele
somador.adicionarNota(10);
somador.adicionarNota(8);
somador.adicionarNota(6);

// Chama o método verTotal
somador.verTotal();
```

---

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:

- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):

- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:

- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

**Resposta:**

```
// Cria a classe "Funcionario"
class Funcionario {
	constructor(nome, idade) {
		this.nome = nome; // Salva o atributo "nome" do funcionário
		this.idade = idade; // Salva o atributo "idade" do funcionário
		this.salarioBase = 0; // Cria o atributo relativo ao salário do funcionário
	}

	calcularSalario() {} //Cria o método para calcular o salário do funcionário
}

// Cria uma classe filha de "Funcionario", a classe "Professor"
class Professor extends Funcionario {
	constructor(nome, idade, disciplina, preçoHoraAula, horasDeAula) {
		super(); // Faz "Professor" herdar os atributos de "Funcionario"
		this.nome = nome;
		this.idade = idade;
		this.salarioBase;

		// Informações exclusivas dos professores
		this.disciplina = disciplina; // Salva a "disciplina que o professor ensina"
		this.preçoHoraAula = preçoHoraAula; // Preço que o professor cobra por uma hora de aula
		this.horasDeAula = horasDeAula; // Quantas horas de aula o professor faz por mês
	}

    // Cria o método de calcular salário do professor
	calcularSalario() {
		// Calcula o salário base do professor, multiplicando quantas aulas ele faz por mês pelo preço da hora de cada uma delas
		this.salarioBase = this.preçoHoraAula * this.horasDeAula;
	}
}

// Cria os professores
var professor1 = new Professor('Anderson', '42', 'Matemática', '30', '160');
var professor2 = new Professor('Bernardo', '42', 'Geografia', '40', '120');

// Calcula o salário dos professores
professor1.calcularSalario();
professor2.calcularSalario();

// Mostra no console o salário base dos professores
console.log(professor1.salarioBase);
console.log(professor2.salarioBase);

```
