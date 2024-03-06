# Desafios de Programação

## questões

1. 91

2. **Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.**

IMPORTANTE:

Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;
```java

import java.util.Scanner;

public class _02 {
	public static void main(String[] args) {
		Scanner teclado = new Scanner(System.in);
		System.out.print("diz ai um número: ");
		int numero = teclado.nextInt();

		if (ehFibonacci(numero)) {
			System.out.println(numero + " pertence à sequência de Fibonacci.");
		} else {
			System.out.println(numero + " não pertence à sequência de Fibonacci.");
		}
	}

	public static boolean ehFibonacci(int n) {
		int a = 0;
		int b = 1;

		while (a <= n) {
			if (a == n) {
				return true;
			}
			int temp = a;
			a = b;
			b = temp + b;
		}
		return false;
	}
}
```

3. **Descubra a lógica e complete o próximo elemento:**

    a)9
   
    b)128
   
    c)49
   
    d)100
   
    e)13
   
    f)20

5. **Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.**

Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

    ligo o primeiro interruptor e deixo ligado por alguns minutos.
    desligo e ligo o segundo interruptor.
	
    entro na sala das lâmpadas
	
    a lâmpada que estiver acesa corresponderá ao segundo interruptor.
    a lâmpada que estiver apagada e quente correspondente ao primeiro interruptor.
    a lâmpada que estiver apagada e fria correspondente ao interruptor que não mexi.


5. **Escreva um programa que inverta os caracteres de um string.**
   IMPORTANTE:
      a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;
      b) Evite usar funções prontas, como, por exemplo, reverse;
```java
public class _05 {
	public static void main(String[] args) {
		String original = "vocês está bem ou fingindo está ?";

		char[] chars = original.toCharArray();

		int tamanho = chars.length;

		for (int i = 0; i < tamanho / 2; i++) {
			char temp = chars[i];
			chars[i] = chars[tamanho - i - 1];
			chars[tamanho - i - 1] = temp;
		}

		String invertida = new String(chars);

		System.out.println("resultado invertida: " + invertida);
	}
}
```
