<h1>Portfólio Pessoal com Grid Layout e Material-UI</h1>

  <p>Este projeto é um portfólio pessoal desenvolvido utilizando <strong>Next.js</strong> e <strong>Material-UI</strong>. Ele faz uso do sistema de <span class="highlight">Grid</span> para organizar os componentes de maneira responsiva, além de apresentar um layout moderno com cards interativos para exibir os projetos.</p>

  <h2>Explicação do Sistema Grid</h2>
  <p>O <strong>Grid Layout</strong> é um sistema bidimensional de layout em CSS que permite organizar os elementos de uma página em linhas e colunas, proporcionando uma estrutura limpa e eficiente. Ele é essencial para criar designs responsivos e adaptáveis a diferentes tamanhos de tela.</p>

  <h3>Por que o Grid é importante?</h3>
  <ul>
    <li><strong>Responsividade:</strong> O Grid permite que os elementos da interface se ajustem automaticamente ao tamanho da tela, desde dispositivos móveis até grandes monitores.</li>
    <li><strong>Flexibilidade:</strong> Ele facilita a criação de layouts complexos com poucos elementos CSS.</li>
    <li><strong>Organização:</strong> Fornece uma maneira clara e lógica de estruturar conteúdo em uma página web, separando visualmente seções e elementos.</li>
  </ul>

  <h2>Uso no Projeto</h2>
  <p>Neste projeto, o <strong>Grid</strong> é utilizado para criar um layout de cartões de projetos responsivos. Cada cartão exibe uma imagem e detalhes do projeto, e o sistema de grid ajusta a quantidade de colunas com base no tamanho da tela do usuário.</p>

  <h2>Explicação do Código</h2>
  <p>Aqui está uma explicação detalhada do código que compõe a página principal do portfólio:</p>

  <div class="code-block">
    <pre><code>&lt;Layout&gt; &#123;&#47;&#42; Componente de layout que envolve toda a página &#42;&#47;&#125;
  &lt;Container 
    sx=&#123;&#123; 
      mt: 4, 
      color: 'white', 
      padding: '8rem', &#47;&#47; Padding interno para espaçamento
      backgroundColor: '#1c1c1c', &#47;&#47; Cor de fundo do container
      borderRadius: '8px', &#47;&#47; Bordas arredondadas
      textAlign: 'center' &#47;&#47; Texto centralizado
    &#125;&#125;
  &gt;
    &lt;Typography variant="h4" sx=&#123;&#123; mb: 2, fontWeight: 'bold' &#125;&#125;&gt;
      Bem-vindo ao meu portfólio!
    &lt;&#47;Typography&gt;

   &lt;Image
      src="/a.jpg" &#47;&#47; Caminho da imagem no diretório público
      alt="Minha Foto"
      width=&#123;200&#125;
      height=&#123;200&#125;
      style=&#123;&#123; borderRadius: '50%', marginBottom: '1.5rem' &#125;&#125;
    &#47;&gt;

   &lt;Typography variant="body1" sx=&#123;&#123; fontSize: '1.5rem', mb: 4 &#125;&#125;&gt;
      Olá, sou Edson Bruno, desenvolvedor full stack apaixonado por criar soluções incríveis.
    &lt;&#47;Typography&gt;

  &lt;Grid container spacing=&#123;4&#125;&gt;
      &#123;projects.map((project, index) =&gt; (
        &lt;Grid item xs=&#123;12&#125; md=&#123;4&#125; key=&#123;index&#125;&gt;
          &lt;Card 
            sx=&#123;&#123; 
              backgroundColor: '#292929', 
              color: 'white', 
              '&amp;:hover': &#123;
                transform: 'scale(1.05)',
                transition: 'transform 0.3s ease-in-out'
              &#125; 
            &#125;&#125;
          &gt;
            &lt;CardMedia
              component="img"
              height="140"
              image=&#123;project.image&#125;
              alt=&#123;project.title&#125;
            &#47;&gt;
            
   &lt;CardContent&gt;
              &lt;Typography gutterBottom variant="h5" component="div"&gt;
                &#123;project.icon&#125; &#123;project.title&#125;
              &lt;&#47;Typography&gt;
              &lt;Typography variant="body2" color="white"&gt;
                Descrição breve sobre &#123;project.title&#125;.
              &lt;&#47;Typography&gt;
            &lt;&#47;CardContent&gt;
          &lt;&#47;Card&gt;
        &lt;&#47;Grid&gt;
      ))&#125;
    &lt;&#47;Grid&gt;
  &lt;&#47;Container&gt;
&lt;&#47;Layout&gt;
</code></pre>
  </div>

  <h2>Componentes e Layout</h2>
  <ul>
    <li><strong>Layout:</strong> Componente que envolve a página e contém o menu, rodapé, ou qualquer outro conteúdo comum em todas as páginas do site.</li>
    <li><strong>Container:</strong> Elemento que centraliza o conteúdo com margens internas (padding) e estilizações como cor de fundo, bordas arredondadas, e alinhamento de texto.</li>
    <li><strong>Typography:</strong> Componente utilizado para exibir textos de forma estilizada, como o título principal (h4) e a apresentação (body1).</li>
    <li><strong>Image:</strong> Componente de imagem otimizada do Next.js para exibir a foto de perfil.</li>
    <li><strong>Grid:</strong> O sistema de grid é utilizado para criar um layout responsivo de três colunas para os cards de projetos. Cada coluna ajusta seu tamanho com base no tamanho da tela.</li>
    <ul>
      <li><strong>xs=&#123;12&#125;:</strong> O item ocupará a largura total da tela (100%) em dispositivos pequenos.</li>
      <li><strong>md=&#123;4&#125;:</strong> O item ocupará 1/3 da largura da tela em dispositivos médios ou maiores.</li>
    </ul>
    <li><strong>Card:</strong> Componente que encapsula a apresentação de cada projeto. O card inclui uma imagem, título, e uma breve descrição.</li>
    <li><strong>CardMedia:</strong> Exibe a imagem associada a cada projeto dentro do card.</li>
    <li><strong>CardContent:</strong> Área que contém o conteúdo textual dentro do card.</li>
  </ul>

  <h2>Efeitos e Interações</h2>
  <ul>
    <li><strong>Hover Effect:</strong> Os cards possuem um efeito de zoom suave ao passar o mouse, criando uma interação visual atrativa.</li>
    <li><strong>Responsividade:</strong> O uso de xs e md no Grid garante que os cartões fiquem organizados em uma coluna em telas pequenas e em três colunas em telas maiores.</li>
  </ul>

  <h2>Dependências</h2>
  <p>Certifique-se de que você tenha o <strong>Node.js</strong> instalado em seu sistema.</p>

  <h3>Dependências principais</h3>
  <ul>
    <li><strong>next:</strong> Framework React para renderização no lado do servidor</li>
    <li><strong>react:</strong> Biblioteca principal do React</li>
    <li><strong>react-dom:</strong> Biblioteca para manipulação do DOM com React</li>
    <li><strong>@mui/material:</strong> Componentes de UI baseados no Material Design</li>
    <li><strong>@mui/icons-material:</strong> Ícones do Material Design para React</li>
  </ul>

  <h2>Instalação</h2>
  <p>Siga as instruções abaixo para rodar o projeto:</p>

  <pre><code>git clone https://github.com/seu-usuario/portfolio-next.git
cd portfolio-next
npm install
npm run dev</code></pre>

  <p>Abra o navegador e acesse <a href="http://localhost:3000">http://localhost:3000</a>.</p>

  <h2>Conclusão</h2>
  <p>Este projeto demonstra como criar um portfólio moderno usando <strong>Next.js</strong>, <strong>Material-UI</strong>, e o sistema de <strong>Grid Layout</strong>. O Grid é uma ferramenta poderosa para criar layouts responsivos, garantindo que o design funcione bem em diferentes dispositivos.</p>
