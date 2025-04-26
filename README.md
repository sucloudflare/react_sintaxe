# Meu Projeto React

Este é um exemplo de como usar componentes React com diversos exemplos de funcionalidades e conceitos básicos.

## Função simples retornando um título

```jsx
function App() {
  return <h1>Seja bem-vindo ao meu app React 🚀</h1>;
}

```
## Contador usando useState

```
jsx
Copiar
Editar
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <h2>Contador: {count}</h2>
      <button onClick={() => setCount(count + 1)}>Adicionar</button>
    </div>
  );
}

```
## Componente com props
```
jsx
Copiar
Editar
function Welcome({ name }) {
  return <h2>Olá, {name}!</h2>;
}
```
## Chamando um componente passando props
```
jsx
Copiar
Editar
function App() {
  return <Welcome name="Maria" />;
}
```
## Listando itens com map

```
jsx
Copiar
Editar
const frutas = ['Banana', 'Maçã', 'Laranja'];

function ListaFrutas() {
  return (
    <ul>
      {frutas.map((fruta, index) => (
        <li key={index}>{fruta}</li>
      ))}
    </ul>
  );
}
```
## Botão com função de alerta

```
jsx
Copiar
Editar
function BotaoAlerta() {
  const clicar = () => alert('Você clicou!');
  
  return <button onClick={clicar}>Clique aqui</button>;
}
```
## useEffect para ação no carregamento

```
jsx
Copiar
Editar
import { useEffect } from 'react';

function Mensagem() {
  useEffect(() => {
    console.log('Componente montado!');
  }, []);
  
  return <p>Veja o console 🔥</p>;
}

```
## Função de saudação baseada na hora
```
jsx
Copiar
Editar
const saudacao = (hora) => {
  if (hora < 12) return 'Bom dia';
  if (hora < 18) return 'Boa tarde';
  return 'Boa noite';
};
```
## Componente usando children
```
jsx
Copiar
Editar
function Caixa({ children }) {
  return <div className="caixa">{children}</div>;
}
```
## Componente de produto com nome e preço
```
jsx
Copiar
Editar
function Produto({ nome, preco }) {
  return (
    <div>
      <h3>{nome}</h3>
      <p>Preço: R$ {preco}</p>
    </div>
  );
}
```
## Formulario controlado com useState
```
jsx
Copiar
Editar
const [texto, setTexto] = useState('');

function Formulario() {
  return (
    <form>
      <input 
        type="text" 
        value={texto}
        onChange={(e) => setTexto(e.target.value)}
      />
      <p>Você digitou: {texto}</p>
    </form>
  );
}
```
## Avatar com estilização inline
```
jsx
Copiar
Editar
function Avatar({ src, alt }) {
  return <img src={src} alt={alt} style={{ width: '100px', borderRadius: '50%' }} />;
}
```
## Status usando operador ternário
```
jsx
Copiar
Editar
const status = true;

function Status() {
  return (
    <div>
      {status ? <p>✅ Online</p> : <p>❌ Offline</p>}
    </div>
  );
}
```

## Card com título e conteúdo
```
jsx
Copiar
Editar
function Card({ title, content }) {
  return (
    <section>
      <h2>{title}</h2>
      <p>{content}</p>
    </section>
  );
}
```
## Botão chamando função com parâmetro
```
jsx
Copiar
Editar
const handleClick = (nome) => {
  alert(`Olá, ${nome}!`);
};

function BotaoPersonalizado() {
  return <button onClick={() => handleClick('Lucas')}>Saudar</button>;
}
```
## Lista de tarefas com map
```
jsx
Copiar
Editar
function ListaTarefas({ tarefas }) {
  return (
    <ul>
      {tarefas.map((tarefa, index) => (
        <li key={index}>{tarefa}</li>
      ))}
    </ul>
  );
}
```
## Importação de imagem
```
jsx
Copiar
Editar
import logo from './logo.svg';

function Logo() {
  return <img src={logo} alt="Logo" />;
}
```
## Estilização inline de botão
```
jsx
Copiar
Editar
const estiloBotao = {
  backgroundColor: 'purple',
  color: 'white',
  padding: '10px',
  border: 'none',
  borderRadius: '5px'
};

function BotaoEstiloso() {
  return <button style={estiloBotao}>Botão Roxo</button>;
}
```
## Footer simples
```
jsx
Copiar
Editar
function Footer() {
  return <footer>© 2025 - Meu Projeto React</footer>;
}
```
## Saudação condicional
```
jsx
Copiar
Editar
function SaudacaoDinamica({ nome }) {
  return nome ? <h1>Bem-vindo, {nome}!</h1> : <h1>Olá, visitante!</h1>;
}
```
## Exemplo de switch-case em JSX
```
jsx
Copiar
Editar
function Mensagem({ tipo }) {
  switch (tipo) {
    case 'sucesso':
      return <p>✅ Sucesso!</p>;
    case 'erro':
      return <p>❌ Erro!</p>;
    default:
      return <p>⚙️ Em progresso...</p>;
  }
}
```
## Custom Hook de contagem
```
jsx
Copiar
Editar
import { useState } from 'react';

function useContador(inicial) {
  const [count, setCount] = useState(inicial);
  return {
    count,
    incrementar: () => setCount(count + 1),
    decrementar: () => setCount(count - 1),
  };
}
```
## Componente com defaultProps
```
jsx
Copiar
Editar
function Saudacao({ nome }) {
  return <h1>Bem-vindo, {nome}!</h1>;
}

Saudacao.defaultProps = {
  nome: 'Visitante'
};
```
## Eventos de formulário com useState
```
jsx
Copiar
Editar
const [email, setEmail] = useState('');

function Formulario() {
  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Enviado: ${email}`);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input 
        type="email" 
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      <button type="submit">Enviar</button>
    </form>
  );
}
```
## useContext para tema
```
jsx
Copiar
Editar
const TemaContext = React.createContext();

function TemaProvider({ children }) {
  const [tema, setTema] = useState('claro');
  return (
    <TemaContext.Provider value={{ tema, setTema }}>
      {children}
    </TemaContext.Provider>
  );
}
```
## Componente com array de objetos
```
jsx
Copiar
Editar
const usuarios = [
  { nome: 'Lucas', idade: 25 },
  { nome: 'Maria', idade: 30 },
];

function ListaUsuarios() {
  return (
    <ul>
      {usuarios.map((usuario, index) => (
        <li key={index}>
          {usuario.nome} - {usuario.idade} anos
        </li>
      ))}
    </ul>
  );
}
```
## Carregamento condicional com ternário
```
jsx
Copiar
Editar
const [carregando, setCarregando] = useState(true);

function Carregamento() {
  return (
    <div>
      {carregando ? <p>Carregando...</p> : <p>Conteúdo pronto!</p>}
    </div>
  );
}
```
## Classe CSS aplicada a um botão
```
jsx
Copiar
Editar
function Botao() {
  return <button className="btn-primary">Clique-me</button>;
}
```
## Atualizando o título da página
```
jsx
Copiar
Editar
useEffect(() => {
  document.title = 'Novo título da página';
}, []);
```
## Componente com estilo dinâmico
```
jsx
Copiar
Editar
function CaixaColorida({ cor }) {
  const estilo = {
    backgroundColor: cor,
    width: '100px',
    height: '100px'
  };
  return <div style={estilo}></div>;
}
```
## Componente de navegação simples
```
jsx
Copiar
Editar
function Navbar() {
  return (
    <nav>
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/sobre">Sobre</a></li>
        <li><a href="/contato">Contato</a></li>
      </ul>
    </nav>
  );
}
```
## Componente com funções assíncronas
```
jsx
Copiar
Editar
const fetchData = async () => {
  const res = await fetch('https://api.exemplo.com');
  const data = await res.json();
  console.log(data);
};
```
## Componentes aninhados
```
jsx
Copiar
Editar
function App() {
  return (
    <div>
      <h1>Bem-vindo ao meu App</h1>
      <Saudacao />
    </div>
  );
}

function Saudacao() {
  return <p>Saudações, amigo!</p>;
}
```
## Componente com renderização condicional
```
jsx
Copiar
Editar
function Usuario({ usuario }) {
  return usuario ? (
    <h1>Bem-vindo, {usuario.nome}!</h1>
  ) : (
    <h1>Por favor, faça login.</h1>
  );
}
```
## Slider de imagens
```
jsx
Copiar
Editar
const imagens = ['img1.jpg', 'img2.jpg', 'img3.jpg'];

function Slider() {
  const [indice, setIndice] = useState(0);
  
  return (
    <div>
      <img src={imagens[indice]} alt="Imagem" />
      <button onClick={() => setIndice((indice + 1) % imagens.length)}>Próxima</button>
    </div>
  );
}
```
