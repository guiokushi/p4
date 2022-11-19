# p4

Arvore DOM - arvore construida pelo navegador


Estados
Se nao inicializar o estado componente quando ele nasce não será possivel 
utiliza-lo no futuro
Estate X Props
Estate -> cuida de dados dentro do component 
Props -> cuida de dados fora do component

Commponentes controlados

Commponentes não controlados
não influencia os dados que são relevantes para a vida do componente

Source of truth
Fonte dos dados, onde eles estao armazenados
normalmente na arvore DOM

Linkando elemento html ao estado do componente
<InputText
 	value={this.state.termoDeBusca}
 	onChange={this.onTermoAlterado}
 />

Usuario digita -> elemento html armazena no value -> onchange executa e 
atualiza o estado do componente -> o estado do comp é alterado e o render executa
-> a propriedade value começa a mostrar o valor do estado do componente
Assim gera Single Source of truth(SSOT)

E gera um componente controlado

preventDefault() cancela o evento

.env - 
guarda as chaves de acesso 
define chaves de interesse
Chave de acesso é uma variavel de ambiente -> o valor pode mudar conforme a aplicação muda de estagios
É uma chave que nao queremos compartilhar
o dotenv configura os valores para que possam ser acessados sem ser explicitamente mencionados
Add the react-dotenv.whitelist property to package.json to specify which variables you need exposed

Elementos tem chave e o react utiliza elas para comparar os elementos ja criados com os que são necessarios construir e constroi apenas os que nao existiam

HOOKS
Para utilizar o estate era necessário criar uma classe
nao era possivel compartilhar elementos da classe
funções não tinham estado

diminui o codigo

REDUX
Biblioteca para armazenamento de estados
é utilizado ao mesmo tempo por todos os componentes
Store - container que armazena os estados
Actions - ações disparadas da app para a store criadas pela action creator
é a unica forma de acionar uma mudança de estados no store
Reducers- especificam como o estado aplicação vai mudar de acordo com a action enviada para o store

Como fucniona
User interface
Um componente gera uma interação

Um action creator é acionado e dispara uma ação para o store
essa ação tem um reducer que vai processa-la e fazer a alteração de estado no store

novo estado é disponibilizado

Os estados sao apenas leitura

alterações sao feitas por funções puras(reducers)

React Native




What Is ‘State’ in ReactJS?
The state is a built-in React object that is used to contain data or information about the component. A component’s state can change over time; whenever it changes, the component re-renders. The change in state can happen as a response to user action or system-generated events and these changes determine the behavior of the component and how it will render. 

The setState() Method
State can be updated in response to event handlers, server responses, or prop changes. This is done using the setState() method. The setState() method enqueues all of the updates made to the component state and instructs React to re-render the component and its children with the updated state.

Always use the setState() method to change the state object, since it will ensure that the component knows it’s been updated and calls the render() method.

