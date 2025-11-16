# 📘 Desafio: Programação Orientada a Objetos (POO) em Java  
**Um estudo aprofundado sobre os pilares da Orientação a Objetos aplicado na prática**

Este repositório faz parte do desafio **“Desmistificando a Programação Orientada a Objetos”**, onde o objetivo é explorar e aplicar os pilares fundamentais da POO utilizando Java.  
Aqui, você encontrará explicações detalhadas, exemplos de código, abstrações reais e evoluções feitas sobre o repositório original.

---

## 🧠 Sobre o Desafio

O objetivo deste desafio é **praticar e compreender profundamente** os quatro pilares da Programação Orientada a Objetos:

- **Abstração**  
- **Encapsulamento**  
- **Herança**  
- **Polimorfismo**

A proposta é pegar um problema real, transformá-lo em classes, objetos e comportamentos, e evoluir a solução conforme sua imaginação permitir.

Além disso, o desafio incentiva o uso de **Fork** no repositório original — o que já foi feito — para facilitar a organização das evoluções.

---

# 🧩 Conceitos Fundamentais da POO

Abaixo você encontra cada pilar da POO explicado com clareza, acompanhado de exemplos reais em Java para facilitar seu entendimento.

---

## 🔹 1. Abstração  

A abstração consiste em **identificar elementos essenciais** do mundo real e representá-los como objetos.  
É transformar algo complexo em um modelo simples.

### ✔ Exemplo em Java:

```java
public abstract class Veiculo {
    private String modelo;
    private int ano;

    public Veiculo(String modelo, int ano) {
        this.modelo = modelo;
        this.ano = ano;
    }

    public abstract void mover();
}



``````

Aqui a classe Veiculo captura apenas o essencial: modelo, ano e o comportamento de se mover.

🔹 2. Encapsulamento

Encapsular é proteger os dados internos e permitir o acesso controlado através de métodos.

✔ Exemplo:

````
public class ContaBancaria {
    private double saldo;

    public ContaBancaria(double saldoInicial) {
        this.saldo = saldoInicial;
    }

    public void depositar(double valor) {
        this.saldo += valor;
    }

    public double getSaldo() {
        return saldo;
    }
}

````
A variável saldo é privada para evitar manipulação direta.

🔹 3. Herança

Herança permite que uma classe “filha” herde atributos e métodos de uma classe “pai”.

✔ Exemplo:

``````

public class Carro extends Veiculo {
    public Carro(String modelo, int ano) {
        super(modelo, ano);
    }

    @Override
    public void mover() {
        System.out.println("O carro está se movendo.");
    }
}

``````
A classe Carro herda tudo de Veiculo e ainda sobrescreve o método mover().

🔹 4. Polimorfismo

Um mesmo método pode se comportar de diferentes maneiras dependendo do objeto.

✔ Exemplo:

``````

public class Moto extends Veiculo {
    public Moto(String modelo, int ano) {
        super(modelo, ano);
    }

    @Override
    public void mover() {
        System.out.println("A moto está acelerando.");
    }
}
``````
E usando polimorfismo:

````

Veiculo v1 = new Carro("Civic", 2020);
Veiculo v2 = new Moto("Hornet", 2012);

v1.mover(); // O carro está se movendo.
v2.mover(); // A moto está acelerando.

````



