# Padrao-Memento

-Intenção:

O padrão Memento é usado para restaurar o estado de um objeto a um estado anterior. O padrão de memento se enquadra na categoria de padrão comportamental.

-Implementação:

O padrão Memento é útil quando você precisa fornecer um mecanismo de desfazer em seus aplicativos, quando o estado interno de um objeto pode precisar ser restaurado em um estágio posterior. Usando a serialização junto com esse padrão, é fácil preservar o estado do objeto e trazê-lo de volta mais tarde.

-Descrição:

Abaixo, segue cada um dos participantes desse padrão. O Originator é o objeto que sabe como salvar a si mesmo: a classe que você deseja tornar com estado. O Caretaker é aquele objeto que lida quando e por que o Originator precisa se salvar ou se restaurar. O Memento contém as informações sobre o estado do Originator e não pode ser modificado pelo Caretaker.

-Estrutura:

![alt text](https://dzone.com/sites/all/files/memento_pattern.PNG)


-Participantes de design

O padrão memento tem três participantes.

- Originator - é o objeto que sabe como criar e salvar seu estado para o futuro. Ele fornece os métodos createMemento () e restore (memento).

- Caretaker - executa uma operação no Originator enquanto tem a possibilidade de fazer rollback. Ele mantém o controle de várias lembranças. A classe Caretaker se refere à classe Originator para salvar (createMemento ()) e restaurar (restaurar (memento)) o estado interno do originator.

- Memento - a caixa de segurança que é escrita e lida pelo Originator e conduzida pelo Caretaker. Em princípio, um memento deve estar em um objeto imutável para que ninguém possa alterar seu estado depois de criado.

-Código de exemplo
