<h1>Descrição da Biblioteca particle_system</h1>

<p>A biblioteca <strong>particle_system</strong> é uma implementação simples e eficiente para gerenciar efeitos de partículas em jogos criados com LÖVE 2D. Projetada para ser fácil de usar e integrar, esta biblioteca permite a criação de sistemas de partículas que podem ser emitidos em locais específicos, proporcionando uma forma visual atraente de representar fenômenos como explosões, fumaça, fogo, e muito mais.</p>

<h2>Funcionalidades</h2>
<ul>
    <li><strong>Emissão de Partículas:</strong> Permite emitir múltiplas partículas a partir de uma posição específica com uma taxa de emissão ajustável.</li>
    <li><strong>Atualização de Partículas:</strong> Gerencia a atualização do estado das partículas ao longo do tempo, levando em consideração sua idade e tempo de vida.</li>
    <li><strong>Desenho de Partículas:</strong> Renderiza partículas na tela, com uma opção de transparência baseada na idade da partícula, criando um efeito de desvanecimento natural.</li>
    <li><strong>Personalização:</strong> Facilita ajustes na taxa de emissão, tamanho das partículas e tempo de vida, permitindo que os desenvolvedores adaptem o comportamento das partículas conforme necessário.</li>
</ul>

<h2>Estrutura</h2>
<p>A biblioteca é composta por uma única classe <strong>ParticleSystem</strong>, que inclui métodos para criar um novo sistema de partículas, emitir partículas, atualizar seu estado e desenhá-las na tela. A estrutura modular permite fácil integração em qualquer projeto que utilize o framework LÖVE 2D.</p>

<h2>Como Usar</h2>
<ol>
    <li><strong>Importar a Biblioteca:</strong>
        <pre><code>local ParticleSystem = require("lib.particle_system")</code></pre>
    </li>
    <li><strong>Criar um Novo Sistema de Partículas:</strong>
        <pre><code>local ps = ParticleSystem.new(x, y) -- x e y são as coordenadas de emissão</code></pre>
    </li>
    <li><strong>Emitir Partículas:</strong>
        <pre><code>ps:emit()</code></pre>
    </li>
    <li><strong>Atualizar e Desenhar:</strong> No loop de atualização e renderização do jogo:
        <pre><code>ps:update(dt)
ps:draw()</code></pre>
    </li>
</ol>

<h2>Exemplo de Uso</h2>
<pre><code>function love.mousepressed(x, y, button)
    if button == 1 then
        ps.x = x
        ps:emit() -- Emite partículas ao clicar
    end
end</code></pre>