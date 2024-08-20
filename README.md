Aplicativo em Kotlin, utilizando Compose para UI para aprendizado com IA e prompts inteligentes.

-> Gerando estratégia de arquitetura usando o Ideamap.ai
![image](https://github.com/user-attachments/assets/0475fb72-6c03-4b29-b1e4-7b9ee12e39a8)

Prompt Público após treinamento: 
        "Como um especialista de desenvolvimento mobile android, 
        no cargo de engenheiro de software de uma grande empresa,
        me ofereça uma lista de ferramentas, técnicas e padrões de projeto utilizados nos projetos mais modernos de android 
        que definirá a arquitetura do meu app."

ChatGPT said:
      "Como engenheiro de software especializado em desenvolvimento mobile Android em uma grande empresa, 
      você provavelmente precisará trabalhar com arquiteturas escaláveis, modulares e de fácil manutenção. 
      Para definir a arquitetura de um aplicativo Android moderno, é essencial considerar uma combinação de ferramentas, técnicas e padrões de projeto. 
      Aqui está uma lista que pode te guiar:

1. Arquitetura
MVVM (Model-View-ViewModel): O padrão MVVM é amplamente utilizado em Android por seu suporte nativo através da biblioteca Jetpack. Ele separa a lógica de apresentação (ViewModel) da lógica de negócios e dados (Model), promovendo modularidade e testabilidade.
Clean Architecture: Propõe uma separação clara de responsabilidades, organizando o código em camadas (Data, Domain, Presentation). Isso facilita a manutenção e evolução do projeto, além de permitir o uso de injeção de dependências e testes isolados.
MVI (Model-View-Intent): Cada vez mais utilizado em aplicações que precisam de estados imutáveis e previsíveis, principalmente em apps mais complexos. Ele é uma variante mais reativa do MVVM.
2. Injeção de Dependências
Dagger/Hilt: Dagger é o padrão de fato para injeção de dependências no Android, mas Hilt, que é baseado no Dagger, simplifica sua configuração e uso. Ele oferece uma abordagem mais simples e otimizada para injeção em componentes como Activity, Fragment, ViewModel e Worker.
Koin: Para projetos que preferem um framework de injeção de dependências mais leve e sem a complexidade de anotações e geração de código do Dagger, Koin oferece uma alternativa baseada em DSL Kotlin.
3. Gerenciamento de Estado
LiveData & ViewModel: LiveData é parte do Jetpack e é usado para manter e observar estados de UI de forma segura ao ciclo de vida do Android. Junto com ViewModel, é fundamental para implementar o padrão MVVM.
StateFlow e SharedFlow: Alternativa moderna ao LiveData, baseada em Kotlin coroutines. Proporciona controle mais refinado sobre fluxo de dados e gerenciamento de estado de forma reativa.
Redux-like (Unidirectional Data Flow): Frameworks como MVI permitem uma arquitetura reativa com fluxo de dados unidirecional, garantindo que o estado da UI seja sempre previsível.
4. Persistência de Dados
Room: Parte do Jetpack, Room é o ORM oficial do Android para persistência local usando SQLite. Ele simplifica o trabalho com bancos de dados ao fornecer abstrações e suporte à validação em tempo de compilação.
DataStore: Substitui o SharedPreferences, oferecendo uma maneira moderna e segura para armazenar dados simples em chave-valor ou com Proto DataStore (para dados estruturados).
Realm/SQLDelight: Para necessidades específicas de performance ou flexibilidade, essas alternativas ao Room podem ser escolhidas, com foco em sincronização em tempo real ou esquemas fortemente tipados.
5. Network
Retrofit + OkHttp: Retrofit é a escolha mais comum para lidar com requisições HTTP. Juntamente com OkHttp, oferece suporte para integração com APIs RESTful, serialização com Gson ou Moshi, e interceptação de requisições.
Ktor: Uma alternativa moderna ao Retrofit, Ktor é um framework assíncrono e multiplataforma para requisições HTTP, que se integra perfeitamente com coroutines.
6. Coroutines e Multithreading
Kotlin Coroutines: Coroutines são amplamente utilizadas para gerenciar código assíncrono de maneira mais legível e eficiente, evitando callbacks e complexidade excessiva no código.
RxJava/RxKotlin: Embora Coroutines estejam se tornando o padrão, RxJava ainda é uma escolha poderosa para aplicações que requerem operações reativas complexas.
7. UI e Interação
Jetpack Compose: A nova abordagem declarativa da UI do Android que substitui o XML tradicional. Jetpack Compose oferece uma maneira moderna e mais eficiente de construir interfaces de usuário, integrando-se nativamente com ViewModels e gerenciando estados de forma declarativa.
Material Design Components: Para garantir uma UI consistente com as diretrizes de design do Google, usar a biblioteca de Material Design é crucial. Ela fornece componentes prontos para uso, como botões, barras de navegação, entre outros.
8. Navegação
Jetpack Navigation Component: Simplifica a implementação de navegação entre telas, gerenciamento de back stack, e passagem de dados entre fragments ou activities. Oferece suporte para navegação declarativa com o arquivo nav_graph.xml.
Deeplink Handling: Para lidar com navegação via links profundos, o Navigation Component também oferece suporte robusto, facilitando a integração com links externos.
9. Teste
JUnit + Espresso: Para testes unitários e de UI, essas são ferramentas padrão para Android.
Mockito/KotlinMock: Ferramentas de mocking para criar dublês de teste e verificar interações com dependências.
Robolectric: Para testes unitários que simulam o comportamento de componentes Android em tempo de execução.
Compose Testing: Para Jetpack Compose, existem APIs específicas para testes de UI, como composeTestRule, que permitem simular e verificar a interface declarativa.
10. Monitoramento e Analytics
Firebase Crashlytics: Para monitoramento de falhas e problemas de estabilidade em produção.
Firebase Analytics: Para coleta de métricas de uso do app.
LeakCanary: Uma ferramenta útil para detectar vazamentos de memória durante o desenvolvimento.
11. CI/CD
GitHub Actions/Bitrise/CircleCI: Para integração contínua e entrega contínua, essas ferramentas permitem automação de testes, builds, e deploys de forma eficiente.
Fastlane: Automatiza processos de deployment, como envio de builds para o Google Play.
12. Modularização
Modularização de Aplicativos: Dividir o projeto em módulos (como core, features, data, etc.) permite escalabilidade e paralelização do trabalho. Isso melhora o tempo de build e facilita o desenvolvimento colaborativo.
Dynamic Feature Modules: Utilizados para otimizar o tamanho do APK e permitir que funcionalidades sejam carregadas sob demanda.
13. Bibliotecas Auxiliares
Timber: Para logging mais eficiente e flexível em substituição ao Log nativo do Android.
Coil/Glide/Picasso: Bibliotecas para carregamento de imagens otimizadas.
WorkManager: Gerenciamento de tarefas em segundo plano com suporte a restrições como conectividade, bateria, etc.
Essa combinação de ferramentas e padrões vai te ajudar a construir aplicativos robustos, escaláveis e que seguem as melhores práticas de desenvolvimento no ecossistema Android moderno."





Project Owner Marlena Martins e Desenvolvedor Mobile Flávio Sapucaia.

obs: As estratégias, alterações, decisões e documentações, estão sendo desenvolvidas e apresentadas em um rascunho de projeto criado nesta mesma plataforma com o objetivo apenas de estudo no link abaixo:
https://github.com/users/MarlenaMartins1533/projects/1

obs: É permitido o estudo e evolução desse projeto; contudo não é permitido a cópia e uso comercial do código nem do projeto.
É possível replicar os passos do projeto com alterações utilizando as plataformas de IA's e prompts mais elaborados, para criação de um projeto/modelo próprio mais útil para sua proposta ou ferramenta comercial. 
Faça o seu com passos simples, siga a WIKI...


