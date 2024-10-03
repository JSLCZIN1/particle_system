A biblioteca particle_system é uma implementação simples e eficiente para gerenciar efeitos de partículas em jogos criados com LÖVE 2D. Projetada para ser fácil de usar e integrar, esta biblioteca permite a criação de sistemas de partículas que podem ser emitidos em locais específicos, proporcionando uma forma visual atraente de representar fenômenos como explosões, fumaça, fogo, e muito mais.

Funcionalidades

Emissão de Partículas: Permite emitir múltiplas partículas a partir de uma posição específica com uma taxa de emissão ajustável.

Atualização de Partículas: Gerencia a atualização do estado das partículas ao longo do tempo, levando em consideração sua idade e tempo de vida.

Desenho de Partículas: Renderiza partículas na tela, com uma opção de transparência baseada na idade da partícula, criando um efeito de desvanecimento natural.

Personalização: Facilita ajustes na taxa de emissão, tamanho das partículas e tempo de vida, permitindo que os desenvolvedores adaptem o comportamento das partículas conforme necessário.


Estrutura

A biblioteca é composta por uma única classe ParticleSystem, que inclui métodos para criar um novo sistema de partículas, emitir partículas, atualizar seu estado e desenhá-las na tela. A estrutura modular permite fácil integração em qualquer projeto que utilize o framework LÖVE 2D.

Como Usar

1. Importar a Biblioteca:

local ParticleSystem = require("lib.particle_system")


2. Criar um Novo Sistema de Partículas:

local ps = ParticleSystem.new(x, y) -- x e y são as coordenadas de emissão


3. Emitir Partículas:

ps:emit()


4. Atualizar e Desenhar: No loop de atualização e renderização do jogo:

ps:update(dt)
ps:draw()



Exemplo de Uso

function love.mousepressed(x, y, button)
    if button == 1 then
        ps.x = x
        ps:emit() -- Emite partículas ao clicar
    end
end


