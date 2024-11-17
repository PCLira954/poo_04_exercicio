                        Exercício 04 P.O.O

1. Assinale verdadeiro ou falso:
(F) Objetos são modelos para classes;
(F) Atributos de uma classe devem ser obrigatoriamente inicializados para que as
classes compilem;
(V) Uma variável declarada dentro de um método deve ser inicializada para que a
classe seja compilável;
(F) Uma variável que seja uma classe declarada em um método é automaticamente
inicializada com undefined;
(V) Construtores são rotinas especiais que servem para inicializar e configurar os
objetos no momento da instanciação;
(V) Construtores não possuem tipo de retorno e podem ou não ter parâmetros;
(V) Uma classe pode ter várias instâncias.

2. Suponha uma classe Hotel que sirva apenas para guardar a quantidade de
solicitações de reservas feitas conforme abaixo:
class Hotel {
quantReservas : number;
adicionarReserva() : void {
this.quantReservas++;
}
}
Podemos afirmar que haverá um problema de compilação, pois a variável inteira não
foi inicializada previamente? Justifique.

RESPOSTA: Sim, haverá um problema de compilação. Pois a linguagem exige a inicialização explícita de atributos.

3. Ainda sobre a classe do exemplo anterior, considere o código abaixo:
let hotel : Hotel = new Hotel(2);
console.log(hotel.quantReservas);
Adicione o construtor que aceite um parâmetro inteiro e faça a inicialização do atributo
quantReservas.

RESPOSTA: 
class Hotel {
    quantReservas: number
   
    constructor(quantReservas: number) {
        this.quantReservas = quantReservas    }

    adicionarReserva(): void {
        this.quantReservas++
    }
}

let hotel: Hotel = new Hotel(2)
console.log(hotel.quantReservas)



4. Considere a classe Radio e as instruções que fazem seu uso abaixo:
class Radio {
volume : number;
constructor(volume : number) {
this.volume = volume;

}
}
let r : Radio = new Radio();
r.volume = 10;
Justifique o erro de compilação e proponha uma solução.

RESPOSTA: Está sendo enviado dois valores para o atributo Volume, um pelo construtor e outro pelo r.volume = 10.
Uma solução para propor é recomendar somente um dos meios para atribuir o valor.

5. Considerando o uso da classe Conta apresentada em aula e seu uso abaixo:
let c1: Conta = new Conta("1",100);
let c2: Conta = new Conta("2",100);
let c3: Conta;
c1 = c2;
c3 = c1;
c1.sacar(10);
c1.transferir(c2,50);
console.log(c1.consultarSaldo());
console.log(c2.consultarSaldo());
console.log(c3.consultarSaldo());
a. Qual o resultado dos dois "prints"? Justifique sua resposta.
RESPOSTA: Resultado é 90. Todas as variáveis apontam para o objeto de c2, e como o novo valor de c2 é 90, esse valor tbm é atribuído a c1 e c2.

b. O que acontece com o objeto para o qual a referência c1 apontava?
RESPOSTA: Agora nenhuma variável aponta para ele, e depois de um tempo ele será apagado da memória.
