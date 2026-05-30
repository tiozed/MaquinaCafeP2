# MaquinaCafeP2
# Avaliação P2 - Linguagem de Programação - Prof. Bruno Zolotareff

## Nomes
Davi Sanchez Nogueira /
Kaua dos Santos Silva

# Máquina de Café com POO

# Resposta da Pergunta

No desenvolvimento da Máquina de Café utilizando Java e Programação Orientada a Objetos (POO), foram aplicados os três principais pilares da orientação a objetos: Encapsulamento, Herança e Polimorfismo.

1. Encapsulamento

O encapsulamento foi utilizado na classe abstrata Drink, onde os atributos sabor e valor foram declarados como privados (private). Dessa forma, o acesso direto aos dados é protegido, sendo realizado apenas por meio dos métodos públicos getSabor(), setSabor(), getValor() e setValor().

Essa prática garante maior segurança e controle sobre os dados da aplicação, evitando alterações indevidas nos atributos.

2. Herança

A herança foi aplicada quando a classe Cafe estendeu a classe abstrata Drink.

public class Cafe extends Drink

Com isso, a classe Cafe herdou todos os atributos e métodos da classe Drink, reutilizando código e evitando duplicação. Os atributos sabor e valor, bem como seus métodos de acesso, passaram a fazer parte da classe Cafe.

3. Abstração

A abstração foi implementada por meio da classe abstrata Drink.

public abstract class Drink

A classe Drink representa um conceito genérico de bebida, contendo apenas as características essenciais que todas as bebidas possuem, como sabor e valor. Ela não precisa ser instanciada diretamente, servindo apenas como base para outras classes mais específicas, como a classe Cafe.

4. Polimorfismo

Embora o código atual não utilize polimorfismo diretamente, ele poderia ser implementado criando outras classes concretas derivadas de Drink, como:

public class Cha extends Drink
public class Chocolate extends Drink

Dessa forma, seria possível criar uma referência do tipo Drink apontando para diferentes objetos:

Drink bebida1 = new Cafe("Café Tradicional", 1.30);
Drink bebida2 = new Cha("Chá Verde", 2.00);
Drink bebida3 = new Chocolate("Chocolate Quente", 3.50);

Nesse caso, a mesma variável do tipo Drink poderia armazenar objetos de diferentes classes, caracterizando o polimorfismo.

Classe com características de duas ou mais classes concretas

Em Java não existe herança múltipla entre classes. Para obter características de várias classes, utiliza-se herança juntamente com interfaces.

Exemplo:

    public interface Quente {
    void aquecer();
    }

    public interface Doce {
    void adicionarAcucar();
    }

    public class CafeEspecial extends Drink implements Quente, Doce {
    
    public CafeEspecial(String sabor, double valor) {
        super(sabor, valor);
    }

    @Override
    public void aquecer() {
        System.out.println("Aquecendo bebida...");
    }

    @Override
    public void adicionarAcucar() {
        System.out.println("Adicionando açúcar...");
    }
}

Nesse exemplo, a classe CafeEspecial possui características de mais de uma estrutura por meio das interfaces, demonstrando uma aplicação prática do polimorfismo e da reutilização de código.

Conclusão

A aplicação da Máquina de Café utilizou os conceitos fundamentais da Programação Orientada a Objetos. A abstração foi representada pela classe abstrata Drink, a herança pela extensão realizada pela classe Cafe, o encapsulamento pela proteção dos atributos privados e o polimorfismo pode ser implementado por meio de novas bebidas derivadas de Drink, tornando o sistema mais flexível, organizado e fácil de manter.
