<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Curiosidades do Mundo</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        /* O CSS estava comentado. Para que o site tenha um visual, ele precisa estar ativo. */
        body { font-family: Arial, sans-serif; line-height: 1.6; margin: 0; padding: 0; background-color: #f4f4f4; color: #333; }
        header { background-color: #333; color: #fff; padding: 1rem 0; text-align: center; }
        header h1 { margin: 0; }
        header p { margin-top: 0.5rem; }
        nav { background-color: #444; padding: 0.5rem 0; text-align: center; }
        nav a { color: #fff; text-decoration: none; padding: 0.5rem 1rem; display: inline-block; }
        nav a:hover { background-color: #555; }
        .container { max-width: 960px; margin: 20px auto; padding: 0 20px; background-color: #fff; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        section { padding: 20px 0; border-bottom: 1px solid #eee; }
        section:last-of-type { border-bottom: none; }
        h2 { color: #333; }
        .curiosidade { margin-bottom: 15px; padding: 10px; border-left: 5px solid #007bff; background-color: #e9f7ff; }
        .curiosidade strong { color: #0056b3; }
        footer { text-align: center; padding: 20px; background-color: #333; color: #fff; margin-top: 20px; }
    </style>
</head>
<body>

<header>
    <h1>Curiosidades do Mundo</h1>
    <p>Descubra fatos incríveis sobre o nosso planeta, o universo e muito mais.</p>
    <nav>
        <a href="#sobre">Sobre</a>
        <a href="#natureza">Natureza</a>
        <a href="#espaco">Espaço</a>
        <a href="#historia">História</a>
        <a href="#corpo">Corpo Humano</a>
        <a href="#lugares">Lugares</a>
    </nav>
</header>

<div class="container">
    <section id="sobre">
        <h2>Sobre o Site</h2>
        <p>Este site reúne curiosidades interessantes e divertidas sobre o mundo em que vivemos.
        Use as seções abaixo para explorar diferentes temas e aprender algo novo em poucos minutos.</p>
    </section>

    <section id="natureza">
        <h2>Natureza e Animais</h2>
        <div class="curiosidade">
            <strong>Polvos com três corações:</strong>
            <p>Os polvos possuem três corações e seu sangue é azul por causa de uma proteína rica em cobre chamada hemocianina.</p>
        </div>
        <div class="curiosidade">
            <strong>Girafas silenciosas:</strong>
            <p>As girafas raramente emitem sons audíveis. Durante muito tempo acreditou-se que elas eram praticamente “mudas”.</p>
        </div>
    </section>

    <section id="espaco">
        <h2>Espaço e Universo</h2>
        <div class="curiosidade">
            <strong>Um dia em Vênus:</strong>
            <p>Em Vênus, um dia é mais longo do que um ano. O planeta leva mais tempo para girar em torno de si mesmo do que para dar uma volta completa ao redor do Sol.</p>
        </div>
        <div class="curiosidade">
            <strong>Silêncio no espaço:</strong>
            <p>No espaço, o som não se propaga como na Terra, porque não há ar (um meio material) para as ondas sonoras viajarem.</p>
        </div>
    </section>

    <section id="historia">
        <h2>História e Civilizações</h2>
        <div class="curiosidade">
            <strong>Cleópatra e o iPhone:</strong>
            <p>Cleópatra viveu mais perto da invenção do iPhone do que da construção das pirâmides de Gizé, que são milhares de anos mais antigas.</p>
        </div>
        <div class="curiosidade">
            <strong>Sal como pagamento:</strong>
            <p>Na Antiguidade e na Idade Média, o sal era tão valioso que podia ser usado como forma de pagamento.
            A palavra “salário” vem dessa prática.</p>
        </div>
    </section>

    <section id="corpo">
        <h2>Corpo Humano</h2>
        <div class="curiosidade">
            <strong>Ossos em mudança:</strong>
            <p>Um bebê nasce com mais de 270 ossos, mas muitos se fundem com o tempo. Na idade adulta, restam cerca de 206.</p>
        </div>
        <div class="curiosidade">
            <strong>Impressões únicas:</strong>
            <p>Assim como as digitais, a língua de cada pessoa também possui um padrão único de rugas e marcas.</p>
        </div>
    </section>

    <section id="lugares">
        <h2>Lugares Incríveis</h2>
        <div class="curiosidade">
            <strong>O maior deserto:</strong>
            <p>O maior deserto do mundo é a Antártida. Apesar de ser coberta de gelo, é extremamente seca e quase não chove.</p>
        </div>
        <div class="curiosidade">
            <strong>Sol da meia-noite:</strong>
            <p>Em algumas regiões próximas ao Círculo Polar Ártico, como no norte da Noruega, o sol não se põe durante semanas no verão.</p>
        </div>
    </section>
</div>

<footer>
    <p>© 2026 - Curiosidades do Mundo. Todos os direitos reservados.</p>
</footer>

<script>
    document.addEventListener('DOMContentLoaded', function() {
        // 1. Rolagem Suave para os Links de Navegação
        document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault(); // Impede o comportamento padrão do link (pulo instantaneo)

                const targetId = this.getAttribute('href'); // Pega o ID da seção (ex: "#natureza")
                const targetElement = document.querySelector(targetId); // Encontra o elemento correspondente

                if (targetElement) {
                    // Rola para o elemento com um comportamento suave
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });

        // 2. Atualização Dinâmica do Ano no Rodapé
        const footerYearParagraph = document.querySelector('footer p');
        if (footerYearParagraph) {
            const currentYear = new Date().getFullYear();
            // CORREÇÃO: A linha abaixo estava apenas fazendo o replace, mas não atribuía o novo valor de volta ao innerHTML.
            // Agora, ela atribui o valor corrigido.
            footerYearParagraph.innerHTML = footerYearParagraph.innerHTML.replace(/© \d{4}/, `© ${currentYear}`);
        }
    });
</script>
</body>
</html>

 
