# Programação Orientada a Objectos

1 - Escreve um programa em C# que aceite dois inteiros na linha de comandos e
imprima no ecrã cinco números aleatórios cujo valor se situe no intervalo
entre os dois inteiros dados. Usa para o efeito um objecto da classe [Random].

> [Soluções](../solucoes/03_poo/01.md)

---

2 - A classe [Stack] (_namespace_ [System.Collections]) implementa a estrutura
de dados [stack/pilha], na qual a última coisa a ser inserida é a primeira a
ser retirada. Objectos do tipo [Stack] podem ser instanciados com o construtor
simples [Stack()]. O método [Push()] coloca um objeto na pilha, enquanto o
método [Pop()] retira o último objeto lá colocado. O método [Contains()]
verifica se dado objeto existe na pilha.

Cria um programa em C# que apresente um menu ao utilizador com quatro opções:

1. Inserir _string_ na pilha
2. Remover _string_ da pilha, imprimindo a mesma no ecrã
3. Verificar se determinada _string_ existe na pilha
4. Sair

O menu deve ser apresentado em ciclo, e o programa só deve terminar quando o
utilizador selecionar a opção 4.

_Nota:_ A [stack/pilha] aqui referida é a estrutura de dados e não a
_stack_ dos programas onde são locadas as variáveis locais dos métodos e por
ai fora.

> [Soluções](../solucoes/03_poo/02.md)

---

3 - Dá uma vista de olhos na documentação da classe [Math] (_namespace_
[System]). É possível instanciar objetos desta classe? Porquê?

> [Soluções](../solucoes/03_poo/03.md)

---

4 - A classe [Queue] (_namespace_ [System.Collections]) implementa a estrutura
de dados [queue/fila], na qual a primeira coisa a ser inserida é a primeira a
ser retirada. Objectos do tipo [Queue] podem ser instanciados com o construtor
simples [Queue()]. O método [Enqueue()] coloca um objeto no fim da fila,
enquanto o método [Dequeue()] retira o primeiro objeto lá colocado. O método
[ToArray()] copia todos os elementos da fila para um _array_ e devolve esse
_array_.

Cria um programa em C# que apresente um menu ao utilizador com quatro opções:

1. Inserir _string_ na fila
2. Remover _string_ da fila, imprimindo a mesma no ecrã
3. Listar todas as _string_ existentes na fila
4. Sair

O menu deve ser apresentado em ciclo, e o programa só deve terminar quando o
utilizador selecionar a opção 4.

> [Soluções](../solucoes/03_poo/04.md)

---

5 - A classe `Line` tem os seguintes métodos:

```cs
// Cria uma nova instância de Line com as coordenadas indicadas
public Line(double x1, double y1, double x2, double y2);

// Indica se a linha atual cruza com a linha indicada no primeiro argumento
public bool Cross(Line otherLine);
```

Escreve um programa que solicite ao utilizador a informação necessária para
criar duas linhas e depois apresente no ecrã a indicação se as mesmas se
cruzam.

> [Soluções](../solucoes/03_poo/05.md)

---

6 - Cria uma classe chamada `NPC` com três atributos do tipo `float` (_energy_,
_damage_ e _speed_) e um atributo do tipo `NPCType`, sendo este último uma
enumeração com três valores: `Minion`, `Soldier` e `Boss`. A classe deve ter
um construtor para inicializar estes quatro atributos, e os seguintes métodos:

* `TakeHit()` - Diminui a energia do NPC para metade.
* `Die()` - Mata o NPC, colocando energia e velocidade a zero.
* `Faster()` - Aumenta velocidade em 10%.
* `Slower()` - Diminui velocidade em 10%.
* `Hit()` - NPC desfere golpe e este método retorna a potência do golpe, que é
igual a _damage_ vezes 1, 10 ou 100 caso o `NPCType` seja `Minion`, `Soldier`
ou `Boss`, respetivamente.

Além da classe `NPC`, apresenta também o código da enumeração `NPCType`, tendo
em conta que esta pode facilitar as contas do método `Hit()`.

Apresenta também uma classe `Program` com um único método estático `Main()`
para testar a classe `NPC` e os seus métodos.

> [Soluções](../solucoes/03_poo/06.md)
---

7 - Cria uma classe chamada `CharChecker` com um único método de nome
`CharCheck()`. Este método recebe três argumentos: 1) uma _string_; 2) um
caráter `c`; e, 3) um inteiro `n`. O método retorna `true` caso a _string_
contenha o caráter `c` pelo menos `n` vezes seguidas.

Adiciona o método estático `Main()` à classe `CharChecker`. Este método deve: 1)
solicitar ao utilizador uma _string_; 2) solicitar ao utilizador o valor de
`c`; 3) solicitar ao utilizador o valor de `n`; 4) criar uma nova instância de
`CharChecker`; 5) invocar o respetivo método `CharCheck()` para verificar se o
`c` aparece mais de `n` vezes seguidas na _string_; e, 6) indicar no ecrã o
resultado.

> [Soluções](../solucoes/03_poo/07.md)

---

8 - Cria uma classe chamada `Checker` com um único método de nome `Check()`.
Este método recebe dois argumentos: 1) um _array_ bidimensional de `int`; e, 2)
um `int`. O método retorna `true` caso encontre uma linha (horizontal, vertical
ou diagonal) de quatro ou mais inteiros iguais ao 2º argumento, ou `false`
caso contrário.

Adiciona o método estático `Main()` à classe `Checker`. Este método deve: 1)
solicitar ao utilizador as dimensões do _array_; 2) solicitar ao utilizador os
valores do _array_; 3) solicitar ao utilizador o valor a procurar no
_array_; 4) criar uma nova instância de `Checker`; 5) invocar o respetivo
método `Check()` para verificar se o valor a procurar no _array_ aparece em
forma uma linha com comprimento igual ou maior a quatro; e, 6) indicar no ecrã
se essa linha existe ou não.

> [Soluções](../solucoes/03_poo/08.md)

---

9 - Cria uma classe chamada `Car` com três variáveis de instância, _speed_
(`float`), _weight_ (`float`) e _fuelType_ (enumeração `Fuel` com 4 valores
possíveis: `Gasoline`, `Diesel`, `LPG` e `Electric`). A classe deve ter ainda
uma variável de classe (estática) chamada _maxSpeed_ (`float`), com valor por
omissão igual a 220.0f. A classe deve ter um único construtor que aceita
argumentos para inicializar as variáveis  _weight_ e _fuelType_, inicializando
a variável _speed_ a zero. A classe deve ter os seguintes métodos:

* `Accelerate(float x)` - Aumenta a velocidade com o valor indicado na
  variável `x`, mas nunca acima de _maxSpeed_. Devolve a nova velocidade.
* `Break(float x)` - Diminui a velocidade com o valor indicado na variável `x`,
  mas nunca abaixo de zero. Devolve a nova velocidade.
* `GetSpeed()` - Retorna o valor atual da velocidade sem a alterar.
* `GetFuelType()` - Retorna o tipo de combustível.
* `GetWeight()` - Retorna o peso do carro.
* `GetMaxSpeed()` e `SetMaxSpeed()` - Métodos estáticos para obter e definir
  o valor da variável de classe `maxSpeed`.

Cria ainda uma classe chamada `TestCar` contendo um método estático `Main()`
para testar exaustivamente todos os métodos da classe `Car`.

> [Soluções](../solucoes/03_poo/09.md)

---

10 - Modifica todos os tipos criados no exercício anterior (`Car`, `Fuel` e
`TestCar`) de modo a que façam uso de propriedades e sintaxe de inicialização
de objetos com propriedades. Qual é a versão com menos código _boilerplate_?

> [Soluções](../solucoes/03_poo/10.md)

---

11 - Cria uma classe chamada `Dog`. Instâncias desta classe devem ter os
seguintes atributos:

* Peso (`double`)
* Altura (`double`)
* Cor (`string`)
* Saciação (`double` entre 0 e 1, que corresponde à percentagem de saciação)

Instâncias desta classe devem ter a seguinte funcionalidade:

* Comer (no máximo até estar cheio/saciado)
* Fazer necessidades (no mínimo até estar vazio/cheio de fome)
* Ladrar (deve ser impresso o tipo de ladrar)
* Correr (deve ser devolvida a velocidade, igual a saciação * 100 / peso)

A classe deve ser implementada com as variáveis de instância, propriedades,
construtores e métodos necessários para atingir estes requisitos, usando as
melhores práticas para o efeito. Dentro do possível as propriedades devem ser
públicas com valores por omissão, auto-implementadas e com `set` privado
(_read-only_). Todos os nomes usados devem estar em inglês.

Cria também uma classe `Program` com um método `Main()` estático para testar
todas as funcionalidades da classe `Dog`.

As classes `Dog` e `Program` devem ser completamente documentadas com
comentários XML em inglês.

Este enunciado é propositadamente vago e os alunos devem complementar o
exercício da forma que acharem melhor, desde de que vá ao encontro do que é
pedido.

> [Soluções](../solucoes/03_poo/11.md)

---

12 - Cria uma classe estática chamada `Program` com um único método estático
`Main()`. Neste método devem ser solicitadas ao utilizador as coordenadas `x`,
`y` e `z` de um vetor 3D, devendo depois o método mostrar o comprimento do
vetor.

Para a resolução deste exercício é obrigatório usar um tipo anónimo, sem
variáveis intermédias, para guardar as coordenadas do vector.

> [Soluções](../solucoes/03_poo/12.md)

---

13 - Explica por palavras tuas o significado dos seguintes termos:

* Classe
* Objeto / instância
* Método
* Construtor
* Variável de instância
* Propriedade
* Variável de suporte
* Variável local
* _Overloading_
* Encapsulação

> [Soluções](../solucoes/03_poo/13.md)

---

14 - Indica duas das principais diferenças entre _structs_ e classes.

> [Soluções](../solucoes/03_poo/14.md)

---

15 - Em que parte da memória são colocadas as variáveis do tipo _struct_ quando
guardadas num _array_? Porquê?


As variáveis do tipo struct são colocadas na heap pois um array é um tipo de referência. Tipos de referência pertencem à heap.

> [Soluções](../solucoes/03_poo/15.md)


---

16 - Estuda, analisa e executa o projeto [16](03_poo/16). Considerando que as
_structs_ são tipos de valor, explica a razão de neste caso a alteração de
campos de uma _struct_ dentro de um método também se repercutir fora do método.

> [Soluções](../solucoes/03_poo/16.md)

---

17 - Explica porque razão as _structs_ não podem ter o valor `null`.


Os structs não podem ser Null pois são do tipo value (tipo de valor).

> [Soluções](../solucoes/03_poo/17.md)

---

18 - Explica o que são tipos imutáveis e quais são as vantagens dos mesmos. Dá
um exemplo (em código) de um tipo imutável.

> [Soluções](../solucoes/03_poo/18.md)

---

19 - Explica por palavras tuas o significado e/ou para que servem os seguintes
conceitos e _keywords_:

* Herança
* Classe base/superclasse
* Classe derivada/subclasse
* _Keyword_ `is`
* _Keyword_ `as`
* _Keyword_ `protected`
* _Keyword_ `sealed`
* _Keyword_ `partial`

> [Soluções](../solucoes/03_poo/19.md)

---

20 - Considera a seguinte classe e indica, justificando, se a mesma é
imutável ou não.

```cs
public class Map
{
    public float Width { get; }
    public float Height { get; }
    public int NumberOfBosses { get; }
    protected ulong highScore;
    protected string name;

    public Map(float width, float height, int numberOfBosses, ulong highScore, string name)
    {
        Width = width;
        Height = height;
        NumberOfBosses = numberOfBosses;
        this.highScore = highScore;
        this.name = name;
    }
}
```

> [Soluções](../solucoes/03_poo/20.md)

---

21 - _Exercício em construção_

<!--
Consira a seguinte classe e responde, justificando, às questões em baixo.

```cs
using UnityEngine;

namespace MyGame
{
    public class TargetController : MonoBehaviour
    {

        public GameObject target;
        public float delay;

        private GameArea gameArea;

        private void Start()
        {
            gameArea = new GameArea();
            target = GameObject.FindWithTag("Target");
            SpawnTarget();
        }

        private void Update()
        {
            if ((target == null) && !IsInvoking("SpawnTarget"))
            {
                Invoke("SpawnTarget", delay);
            }
        }

        private void SpawnTarget()
        {
            Vector2 pos = gameArea.RandomPosition(0.9f);
            Instantiate(target, pos, Quaternion.identity);
        }
    }
}
```

* namespace
* Nome da classe, classe base e classe derivada
* Variáveis de instância
* propriedades
* métodos de instância
* uso de métodos herdados
* uso de métodos estáticos

> [Soluções](../solucoes/03_poo/21.md)
-->

---

<a name="ex22"></a>
22 - Considera o seguinte código:

```cs
public struct Bullet
{
    private float calibre;
    public float Calibre
    {
        get { return calibre; }
        set { if (value < 0.1f) calibre = 0.1f; else calibre = value; }
    }
}
public class Weapon
{
    public float Value { get; }
    public Weapon(float value) { Value = value; }
}
public class Gun : Weapon
{
    private Bullet[] bullets;
    public Gun(float value, int numBullets, float calibre) : base(value)
    {
        bullets = new Bullet[numBullets];
        for (int i = 0; i < numBullets; i++)
        {
            bullets[i] = new Bullet() { Calibre = calibre };
        }
    }
}
```

a) Escreve uma linha de código que: a) crie uma instância de `Gun` com valor
(`value`) 50.0 e três `Bullet`s de calibre 0.5; e, b) guarde essa instância
numa variável do tipo `Weapon`.

b) Adiciona uma propriedade à classe `Gun` chamada `NumberOfBullets`, só de
leitura, que retorne o número de `Bullet`s existentes numa instância de `Gun`.

> [Soluções](../solucoes/03_poo/22.md)

---

<a name="ex23"></a>
23 - Considera o seguinte código:

```cs
public struct Passenger
{
    private double weight;
    public double Weight
    {
        get { return weight; }
        set { if (value < 5) weight = 5; else weight = value; }
    }
}
public class Vehicle
{
    public double Value { get; }
    public Vehicle(double value) { Value = value; }
}
public class Car : Vehicle
{
    private Passenger[] passengers;
    public Car(double value, int numPassengers, float avgWeight) : base(value)
    {
        Random r = new Random();
        passengers = new Passenger[numPassengers];
        for (int i = 0; i < numPassengers; i++)
        {
            passengers[i] = new Passenger()
            {
                Weight = avgWeight + r.Next(-10, 10)
            };
        }
    }
}
```

a) Escreve uma linha de código que: a) crie uma instância de `Car` com valor
(`value`) 2550.0 e três `Passenger`s com peso médio (`avgWeight`) 70; e, b)
guarde essa instância numa variável do tipo `Vehicle`.

b) Adiciona um método à classe `Car` chamado `GetTotalWeight()` que retorne o
peso total dos passageiros numa instância de `Car`.

> [Soluções](../solucoes/03_poo/23.md)

---

[Stack]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.stack
[System]: https://docs.microsoft.com/pt-pt/dotnet/api/system
[System.Collections]: https://docs.microsoft.com/dotnet/api/system.collections
[stack/pilha]: https://en.wikipedia.org/wiki/Stack_(abstract_data_type)
[Stack()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.stack.-ctor#System_Collections_Stack__ctor
[Push()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.stack.push
[Pop()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.stack.pop
[Contains()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.stack.contains
[Random]: https://docs.microsoft.com/pt-pt/dotnet/api/system.random
[Math]: https://docs.microsoft.com/pt-pt/dotnet/api/system.math
[Queue]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.queue
[queue/fila]: https://en.wikipedia.org/wiki/Queue_(abstract_data_type)
[Queue()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.queue.-ctor#System_Collections_Queue__ctor
[Enqueue()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.queue.enqueue#System_Collections_Queue_Enqueue_System_Object_
[Dequeue()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.queue.dequeue#System_Collections_Queue_Dequeue
[ToArray()]: https://docs.microsoft.com/pt-pt/dotnet/api/system.collections.queue.toarray
