# Exemplos de Componentes em React

Este repositório contém vários exemplos de componentes e funcionalidades em React.

## 1. Função simples retornando um título

```jsx
function App() {
  return <h1>Seja bem-vindo ao meu app React 🚀</h1>;
}
2. Contador usando useState
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
3. Componente com props
jsx
Copiar
Editar
function Welcome({ name }) {
  return <h2>Olá, {name}!</h2>;
}

function App() {
  return <Welcome name="Maria" />;
}
4. Listando itens com map
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
5. Botão com função de alerta
jsx
Copiar
Editar
function BotaoAlerta() {
  const clicar = () => alert('Você clicou!');
  
  return <button onClick={clicar}>Clique aqui</button>;
}
6. useEffect para ação no carregamento
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
7. Função de saudação baseada na hora
jsx
Copiar
Editar
const saudacao = (hora) => {
  if (hora < 12) return 'Bom dia';
  if (hora < 18) return 'Boa tarde';
  return 'Boa noite';
};
8. Componente usando children
jsx
Copiar
Editar
function Caixa({ children }) {
  return <div className="caixa">{children}</div>;
}
9. Componente de produto com nome e preço
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
10. Formulário controlado com useState
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
11. Avatar com estilização inline
jsx
Copiar
Editar
function Avatar({ src, alt }) {
  return <img src={src} alt={alt} style={{ width: '100px', borderRadius: '50%' }} />;
}
12. Status usando operador ternário
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
13. Card com título e conteúdo
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
14. Botão chamando função com parâmetro
jsx
Copiar
Editar
const handleClick = (nome) => {
  alert(`Olá, ${nome}!`);
};

function BotaoPersonalizado() {
  return <button onClick={() => handleClick('Lucas')}>Saudar</button>;
}
15. Lista de tarefas com map
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
16. Importação de imagem
jsx
Copiar
Editar
import logo from './logo.svg';

function Logo() {
  return <img src={logo} alt="Logo" />;
}
17. Estilização inline de botão
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
18. Footer simples
jsx
Copiar
Editar
function Footer() {
  return <footer>© 2025 - Meu Projeto React</footer>;
}
19. Saudação condicional
jsx
Copiar
Editar
function SaudacaoDinamica({ nome }) {
  return nome ? <h1>Bem-vindo, {nome}!</h1> : <h1>Olá, visitante!</h1>;
}
20. Exemplo de switch-case em JSX
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
21. Custom Hook de contagem
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
22. Componente com defaultProps
jsx
Copiar
Editar
function Saudacao({ nome }) {
  return <h1>Bem-vindo, {nome}!</h1>;
}

Saudacao.defaultProps = {
  nome: 'Visitante'
};
23. Eventos de formulário com useState
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
24. useContext para tema
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
25. Componente com array de objetos
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
26. Carregamento condicional com ternário
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
27. Classe CSS aplicada a um botão
jsx
Copiar
Editar
function Botao() {
  return <button className="btn-primary">Clique-me</button>;
}
28. Atualizando o título da página
jsx
Copiar
Editar
useEffect(() => {
  document.title = 'Novo título da página';
}, []);
29. Componente com estilo dinâmico
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
30. Componente de navegação simples
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
31. Componente com funções assíncronas
jsx
Copiar
Editar
const fetchData = async () => {
  const res = await fetch('https://api.exemplo.com');
  const data = await res.json();
  console.log(data);
};
32. Componentes aninhados
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
33. Componente com renderização condicional
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
34. Slider de imagens
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
Esses são alguns exemplos de código básico em React, com funcionalidades como estado, props, efeitos colaterais, e muito mais. Experimente e personalize conforme necessário!

nginx
Copiar
Editar

Isso deve fornecer um bom ponto de partida para o seu README!
