# Padrões de Projeto
Repositório com exemplos práticos em C++ dos padrões Factory Method, Decorator e Observer, baseados no Refactoring Guru.

## Factory Method - factorymethod.cpp

O padrão Factory Method é útil quando você tem uma classe (Creator) que precisa criar objetos de uma família de classes relacionadas (Product), mas deseja delegar a responsabilidade de instanciar objetos específicos para subclasses dessa classe.

### Problema Resolvido:

O problema principal resolvido pelo Factory Method é permitir a criação de objetos sem precisar conhecer suas classes concretas em tempo de compilação. Isso é particularmente útil quando o código precisa trabalhar com uma variedade de objetos que compartilham uma interface comum, mas cujas implementações específicas variam.

### Solução:

A solução proposta pelo Factory Method é definir um método na classe base (Creator) que as subclasses podem implementar para criar instâncias de suas próprias classes de produto (Product). Dessa forma, a classe base define a interface para a criação de objetos, mas as subclasses podem decidir qual classe concreta instanciar.

### Funcionamento:

O funcionamento geral do Factory Method é permitir que subclasses decidam qual classe concreta de produto criar. O cliente trabalha com a interface do criador, garantindo que ele possa criar produtos sem conhecer a implementação específica de cada produto. Isso promove o princípio da inversão de dependência, onde módulos de alto nível não dependem de módulos de baixo nível, mas sim de abstrações.

## Decorator - decorator.cpp


O padrão Decorator é utilizado para adicionar funcionalidades a objetos individuais de forma dinâmica e flexível, sem a necessidade de modificar a estrutura da classe base.

### Problema Resolvido:

O Decorator resolve o problema de estender o comportamento de objetos de forma modular, sem a necessidade de criar subclasses para cada combinação possível de funcionalidades. Isso é especialmente útil quando se tem um conjunto de funcionalidades que podem ser combinadas de diversas maneiras.

### Solução:

A solução proposta pelo padrão Decorator é criar uma série de classes que seguem a mesma interface da classe base (Component), onde cada classe adiciona uma funcionalidade específica sem alterar a interface original. Essas classes podem ser combinadas de forma dinâmica para adicionar ou remover funcionalidades conforme necessário.

### Funcionamento:
O funcionamento geral é que os decoradores podem ser empilhados para adicionar funcionalidades adicionais a um objeto Component base. Cada decorador envolve o objeto Component anterior, permitindo que o comportamento seja modificado de forma dinâmica e flexível.

Esse padrão permite estender o comportamento de objetos individualmente, sem precisar criar subclasses para cada combinação possível de funcionalidades, promovendo assim a reutilização de código e a separação de preocupações.

## Observer - observer.cpp

O padrão Observer é utilizado para criar um mecanismo de assinatura, permitindo que objetos interessados (observadores) sejam notificados automaticamente quando ocorrem mudanças no estado de um objeto que estão observando (o sujeito). Esse padrão resolve o problema de garantir uma comunicação eficiente e desacoplada entre objetos, onde diversos observadores precisam ser atualizados quando o estado do sujeito é modificado, sem que o sujeito tenha que conhecer os detalhes de implementação de cada observador.

### Funcionamento do Padrão:

Sujeito (Subject): É o objeto que é observado. Ele mantém uma lista de observadores e fornece métodos para que os observadores se registrem (Attach()) e sejam removidos (Detach()) da lista. Além disso, ele notifica todos os observadores registrados quando ocorrem mudanças no seu estado, chamando o método Notify().

Observador (Observer): É o objeto que observa o sujeito. Ele se registra no sujeito para receber notificações sobre mudanças de estado. Quando o sujeito notifica os observadores, cada observador atualiza seu estado ou realiza qualquer ação necessária com base nas informações recebidas.
