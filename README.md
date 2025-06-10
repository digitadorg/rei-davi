<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kit Rei Davi: 1500 Atividades Bíblicas | Transforme o Ensino Infantil</title>
    <!-- Fontes Google para um visual impactante e legível -->
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@500;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        /* Estilos globais para um visual limpo e contrastante */
        body {
            font-family: 'Roboto', sans-serif; /* Fonte para o corpo do texto, legível */
            margin: 0;
            padding-top: 60px; /* Adicionado padding-top para compensar a barra de progresso fixa */
            background-color: #F0F2F5; /* Fundo off-white mais moderno */
            color: #343A40; /* Cor do texto principal, um cinza escuro */
            line-height: 1.7; /* Espaçamento de linha aprimorado */
            scroll-behavior: smooth; /* Rolagem suave para âncoras */
            overflow-x: hidden; /* Evita scroll horizontal */
        }

        .container {
            max-width: 1080px; /* Container um pouco mais largo */
            margin: 0 auto;
            padding: 0 30px; /* Mais padding nas laterais */
        }

        /* Seção do cabeçalho - AGORA ROLA COM A PÁGINA */
        header {
            background-color: #FFFFFF; /* Branco puro */
            padding: 30px 0; /* Mais padding */
            text-align: center;
            border-bottom: 5px solid #1E88E5; /* Linha azul vibrante mais grossa */
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1); /* Sombra mais visível */
            z-index: 999; /* Z-index para que a barra de progresso fique acima */
        }

        header .logo-text {
            font-family: 'Oswald', sans-serif; /* Fonte para o logo, impactante */
            font-size: 3.8em; /* Logo maior */
            color: #FFC107; /* Amarelo vibrante para o logo */
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 4px; /* Mais espaçamento para o "Ultra Black" */
            font-weight: 700;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.2); /* Sombra de texto mais forte */
        }

        header h1 {
            font-family: 'Roboto', sans-serif;
            font-size: 1.8em; /* Subtítulo maior */
            color: #6C757D; /* Cinza médio */
            margin: 0;
            font-weight: 500; /* Mais encorpado */
        }

        /* Cores de destaque para palavras-chave */
        .color-primary { color: #1E88E5; font-weight: 700; } /* Azul Vibrante */
        .color-secondary { color: #FFC107; font-weight: 700; } /* Amarelo Vibrante */
        .color-accent { color: #28A745; font-weight: 700; } /* Verde para sucesso */
        .color-danger { color: #DC3545; font-weight: 700; } /* Vermelho para alerta/problema */
        .text-bold { font-weight: 700; } /* Apenas negrito */

        /* Seção principal de destaque (Hero Section) */
        .hero {
            background-image: linear-gradient(to bottom, #E3F2FD 0%, #F8F9FA 100%); /* Degradê mais suave */
            color: #343A40;
            padding: 100px 0; /* Mais padding */
            text-align: center;
            border-bottom: 3px dashed #90CAF9; /* Linha pontilhada suave */
            position: relative;
            overflow: hidden; /* Para garantir que os elementos de fundo não transbordem */
        }

        /* Efeitos de fundo gamificados para o Hero */
        .hero::before, .hero::after {
            content: '';
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: pulse 10s infinite ease-out;
        }
        .hero::before {
            width: 300px;
            height: 300px;
            top: -50px;
            left: -50px;
            animation-delay: 0s;
        }
        .hero::after {
            width: 200px;
            height: 200px;
            bottom: -30px;
            right: -30px;
            animation-delay: 2s;
        }

        @keyframes pulse {
            0% { transform: scale(0.8); opacity: 0.5; }
            50% { transform: scale(1.2); opacity: 0.2; }
            100% { transform: scale(0.8); opacity: 0.5; }
        }


        .hero h2 {
            font-family: 'Oswald', sans-serif;
            font-size: 4.5em; /* Grande e impactante */
            margin-bottom: 30px;
            line-height: 1.1;
            text-transform: uppercase;
            color: #1E88E5; /* Azul vibrante */
            text-shadow: 3px 3px 8px rgba(0,0,0,0.2); /* Sombra de texto mais forte */
        }

        .hero p {
            font-size: 1.5em; /* Texto maior */
            max-width: 850px;
            margin: 0 auto 60px auto; /* Mais espaçamento */
            font-weight: 300; /* Leve para introdução */
            color: #495057; /* Cinza escuro */
        }

        /* Botão de Chamada para Ação (CTA) */
        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #FFD700, #FFA500); /* Degradê dourado */
            color: #4B0082; /* Roxo profundo para contraste "ultra black" */
            padding: 22px 45px; /* Botão ainda maior */
            font-size: 2.2em; /* Botão gigante */
            font-weight: 800; /* Extra bold */
            text-decoration: none;
            border-radius: 70px; /* Cantos super arredondados */
            transition: all 0.4s ease; /* Transições mais suaves */
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.35); /* Sombra mais proeminente */
            letter-spacing: 2px;
            text-transform: uppercase;
            border: 3px solid #FFD700; /* Borda para contraste */
            cursor: pointer;
            position: relative;
            z-index: 1;
            overflow: hidden;
        }

        .cta-button::before { /* Efeito de brilho */
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: all 0.7s ease;
        }

        .cta-button:hover::before {
            left: 100%;
        }

        .cta-button:hover {
            background: linear-gradient(135deg, #FFA500, #FFD700); /* Inverte o degradê no hover */
            transform: translateY(-8px) scale(1.03); /* Efeito de "pulo" e leve aumento */
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.45); /* Sombra mais intensa */
        }

        /* Seções de conteúdo geral */
        .section {
            padding: 80px 0; /* Mais padding */
            text-align: center;
            background-color: #FFFFFF; /* Fundo branco para seções */
            margin-bottom: 40px; /* Espaço entre seções */
            box-shadow: 0 5px 20px rgba(0,0,0,0.05); /* Sombra más visível para destacar a seção */
            border-radius: 12px; /* Cantos arredondados na seção */
            overflow: hidden; /* Para elementos de fundo */
            position: relative;
        }

        .section:nth-of-type(even) { /* Para alternar cores de fundo das seções */
            background-color: #F8F9FA;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08); /* Sombra um pouco más forte para seções alternadas */
        }

        .section h3 {
            font-family: 'Oswald', sans-serif;
            font-size: 3.8em; /* Títulos de seção mayores */
            color: #1E88E5; /* Azul vibrante */
            margin-bottom: 55px;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative; /* Para o underline animado */
            display: inline-block;
            padding-bottom: 15px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }

        .section h3::after { /* Underline animado (Elementor-like) */
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            bottom: 0;
            width: 100px; /* Tamanho do underline */
            height: 6px; /* Más grosso */
            background-color: #FFC107; /* Amarelo */
            border-radius: 3px;
        }

        /* Grid de funcionalidades/itens do kit (Cards) */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); /* Min-width um pouco mayor */
            gap: 40px; /* Más espaçamento */
            margin-top: 60px;
        }

        .feature-item {
            background-color: #FFFFFF;
            padding: 40px; /* Más padding */
            border-radius: 20px; /* Cantos más arredondados */
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15); /* Sombra más visível e suave */
            text-align: left;
            transition: transform 0.4s ease, box-shadow 0.4s ease, background-color 0.4s ease;
            border: 2px solid #E0E0E0; /* Borda suave */
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .feature-item::before { /* Efeito de fundo no card */
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(30, 136, 229, 0.05), transparent);
            opacity: 0;
            transition: opacity 0.4s ease;
            z-index: -1;
        }

        .feature-item:hover::before {
            opacity: 1;
        }

        .feature-item:hover {
            transform: translateY(-12px); /* Efeito de "levitação" más pronunciado */
            box-shadow: 0 18px 40px rgba(0, 0, 0, 0.25); /* Sombra más intensa no hover */
            background-color: #FDFDFD;
        }

        .feature-item h4 {
            font-family: 'Oswald', sans-serif; /* Título do card com fonte impactante */
            color: #1E88E5; /* Azul vibrante */
            font-size: 2em; /* Título do card mayor */
            margin-bottom: 20px;
            font-weight: 600; /* Um pouco más encorpado */
            text-transform: uppercase;
        }

        .feature-item p {
            font-size: 1.15em; /* Texto do card mayor */
            color: #495057;
            font-weight: 300; /* Leve */
        }

        /* Seção de Ofertas (novo) */
        .offers-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 35px; /* Espaçamento entre as caixas de oferta */
            margin-top: 60px;
        }

        .price-box { /* Estilos base para ambas as caixas */
            background-color: #FFFDE7; /* Amarelo muito claro, quase branco */
            padding: 45px; /* Ajustado para melhor visual com flexbox */
            border-radius: 25px; /* Cantos arredondados */
            box-shadow: 0 12px 35px rgba(0, 0, 0, 0.2); /* Sombra forte */
            text-align: center;
            position: relative;
            overflow: hidden;
            flex: 1 1 45%; /* Permite que as caixas ocupem metade da largura e quebrem em telas menores */
            max-width: 500px; /* Limite de largura para não ficarem muito grandes */
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            border: 3px solid transparent; /* Borda inicial transparente */
            z-index: 1;
        }

        .price-box:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.35);
        }

        .price-box h4 { /* Título dentro da caixa de preço */
            font-family: 'Oswald', sans-serif;
            font-size: 2.5em; /* Título mayor */
            margin-bottom: 30px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }

        .price-box .old-price {
            text-decoration: line-through;
            font-size: 1.7em; /* Ajustado */
            color: #DC3545;
            font-weight: 700;
            margin-bottom: 8px;
        }

        .price-box .new-price {
            font-family: 'Oswald', sans-serif;
            font-size: 5.8em; /* Ajustado */
            font-weight: 700;
            margin: 15px 0 25px 0;
            line-height: 1;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
        }

        .price-box .new-price span {
            font-size: 0.5em;
            vertical-align: super;
        }

        .price-box .symbolic-value {
            font-weight: 500;
            color: #495057;
            margin-bottom: 35px;
            font-size: 1.2em;
        }

        /* Estilos específicos para a Oferta Normal */
        .normal-offer {
            border-color: #90CAF9; /* Borda azul clara para a oferta normal */
            background-image: linear-gradient(to top right, #E3F2FD, #FFFFFF); /* Degradê sutil */
        }
        .normal-offer h4 {
            color: #1E88E5; /* Azul para o título da normal */
        }
        .normal-offer .new-price {
            color: #1E88E5; /* Azul para o preço da normal */
        }
        .normal-offer .cta-button {
            background: linear-gradient(135deg, #FFC107, #FFD54F); /* Amarelo para o botão da normal */
            color: #212529;
            font-size: 1.6em; /* Aumentado */
            padding: 18px 30px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
        }
        .normal-offer .cta-button:hover {
            background: linear-gradient(135deg, #FFD54F, #FFC107);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }
        .normal-offer ul { /* Lista de itens para a oferta normal */
            list-style: none;
            padding: 0;
            margin-top: 30px;
            text-align: left;
            font-size: 1em;
            color: #555;
        }
        .normal-offer ul li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        .normal-offer ul li::before {
            content: '✅'; /* Ícone de check */
            margin-right: 12px;
            color: #28A745;
            font-size: 1.2em;
        }


        /* Estilos específicos para a Super Oferta */
        .super-offer {
            border-color: #28A745; /* Borda verde forte para a super oferta */
            background-image: linear-gradient(to top right, #E6F3EA, #FFFFFF); /* Degradê sutil */
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4); /* Sombra más intensa e proeminente */
            transform: scale(1.05); /* Destaca a super oferta */
            z-index: 2; /* Garante que fique em cima */
        }
        .super-offer:hover {
             transform: translateY(-15px) scale(1.08); /* Más destaque no hover */
        }
        .super-offer h4 {
            color: #28A745; /* Verde para o título da super */
            font-size: 2.8em; /* Título mayor */
        }
        .super-offer .new-price {
            color: #28A745; /* Verde para o preço da super */
            font-size: 6.5em; /* Preço mayor */
        }
        .super-offer .symbolic-value {
            font-size: 1.4em;
            font-weight: 700;
            color: #1A5229;
        }
        .super-offer .cta-button {
            background: linear-gradient(135deg, #28A745, #4CAF50); /* Degradê verde para o botão da super */
            color: #FFFFFF;
            font-size: 2em; /* Botão ainda mayor */
            padding: 20px 40px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }
        .super-offer .cta-button:hover {
            background: linear-gradient(135deg, #4CAF50, #28A745);
            box-shadow: 0 10px 25px rgba(0,0,0,0.4);
        }
        .super-offer::before { /* Fita de "Oferta" (Elementor-like) para a super oferta */
            content: "SUPER OFERTA!";
            position: absolute;
            top: 25px; /* Ajustado */
            left: -60px; /* Ajustado */
            background-color: #DC3545; /* Vermelho */
            color: #FFFFFF;
            padding: 10px 70px; /* Más padding */
            font-family: 'Oswald', sans-serif;
            font-size: 1.2em; /* Aumentado */
            font-weight: 700;
            transform: rotate(-45deg);
            z-index: 10;
            box-shadow: 0 3px 8px rgba(0,0,0,0.3);
        }
        .super-offer ul {
            list-style: none;
            padding: 0;
            margin-top: 35px;
            text-align: left;
            font-size: 1.15em;
            color: #333;
        }
        .super-offer ul li {
            margin-bottom: 12px;
            display: flex;
            align-items: flex-start;
        }
        .super-offer ul li::before {
            content: '✅';
            margin-right: 15px;
            color: #28A745;
            font-size: 1.3em;
        }


        /* Lista de informações/FAQ */
        .info-list {
            list-style: none;
            padding: 0;
            text-align: left;
            max-width: 700px;
            margin: 60px auto;
        }

        .info-list li {
            background-color: #FFFFFF;
            padding: 25px 35px;
            margin-bottom: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 18px rgba(0, 0, 0, 0.08);
            display: flex;
            align-items: flex-start;
            font-size: 1.3em;
            border: 1px solid #E9ECEF;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .info-list li:hover {
            transform: translateX(15px);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.12);
        }

        .info-list li strong {
            flex-shrink: 0;
            margin-right: 20px;
            color: #1E88E5;
            font-weight: 700;
        }
        .info-list li p {
            margin: 0;
            font-size: 1em;
            color: #495057;
            display: none;
            padding-top: 10px;
            transition: max-height 0.3s ease-out;
            overflow: hidden;
            max-height: 0;
        }
        .info-list li.open p {
            display: block;
            max-height: 200px;
        }


        .info-list li .icon {
            font-size: 2em;
            margin-right: 20px;
            flex-shrink: 0;
            transition: transform 0.3s ease;
        }
        .info-list li.open .icon.arrow {
            transform: rotate(90deg);
        }
        .info-list li .icon.red { color: #DC3545; }
        .info-list li .icon.green { color: #28A745; }
        .info-list li .icon.arrow {
            color: #1E88E5;
            font-size: 1.5em;
            margin-right: 10px;
        }


        /* Estilos para a galeria de imagens */
        .image-gallery {
            display: flex; /* Usar flexbox para o carrossel */
            overflow-x: scroll; /* Habilitar rolagem horizontal */
            scroll-snap-type: x mandatory; /* Habilitar ajuste de rolagem */
            -webkit-overflow-scrolling: touch; /* Rolagem suave em iOS */
            gap: 20px; /* Espaçamento entre as imagens */
            margin-top: 60px;
            padding-bottom: 20px; /* Espaço para a barra de rolagem se visível */
            justify-content: flex-start; /* Alinha o início das imagens à esquerda */
        }

        .image-gallery::-webkit-scrollbar {
            height: 8px; /* Altura da barra de rolagem */
        }

        .image-gallery::-webkit-scrollbar-thumb {
            background-color: #1E88E5; /* Cor do "polegar" da barra de rolagem */
            border-radius: 10px;
        }

        .image-gallery::-webkit-scrollbar-track {
            background-color: #CFD8DC; /* Cor da trilha da barra de rolagem */
            border-radius: 10px;
        }

        .image-gallery img {
            flex-shrink: 0; /* Impede que as imagens encolham */
            width: 90%; /* Ajuste para mostrar parte da próxima imagem */
            max-width: 400px; /* Largura máxima para desktop */
            height: auto;
            border-radius: 15px;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
            scroll-snap-align: center; /* Ajusta a imagem ao centro ao parar de rolar */
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .image-gallery img:hover {
            transform: scale(1.02); /* Efeito de zoom leve, remove giro para carrossel */
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.25);
        }


        /* Estilos para depoimentos */
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .testimonial-item {
            background-color: #FFFFFF;
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            text-align: left;
            border: 2px solid #E0E0E0;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .testimonial-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.25);
        }

        .testimonial-item p {
            font-style: italic;
            margin-bottom: 20px;
            color: #555;
            font-size: 1.1em;
            line-height: 1.8;
        }

        .testimonial-item .author {
            font-weight: 700;
            color: #1E88E5;
            font-size: 1.2em;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Seção de Conquistas (Gamificado) */
        .achievements-section {
            background-color: #F0F2F5;
            padding: 80px 0;
            text-align: center;
            border-top: 3px dashed #FFC107;
        }

        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 35px;
            margin-top: 60px;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
        }

        .achievement-item {
            background-color: #FFFFFF;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 180px;
            border: 2px solid #E0E0E0;
            transition: transform 0.4s ease, box-shadow 0.4s ease, background-color 0.4s ease;
            position: relative;
            overflow: hidden;
        }
        .achievement-item::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background-color: rgba(255, 215, 0, 0.1);
            transition: transform 0.5s ease-out, opacity 0.5s ease-out;
            opacity: 0;
            z-index: 0;
        }
        .achievement-item:hover::before {
            transform: translate(-50%, -50%) scale(1.2);
            opacity: 1;
        }

        .achievement-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.2);
            background-color: #FDFDFD;
        }

        .achievement-item .icon-wrapper {
            width: 80px;
            height: 80px;
            background-color: #E3F2FD;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            box-shadow: inset 0 0 8px rgba(0,0,0,0.15);
            position: relative;
            z-index: 1;
        }
        .achievement-item .icon-wrapper svg {
            width: 45px;
            height: 45px;
            fill: #1E88E5;
            transition: fill 0.3s ease;
        }
        .achievement-item:hover .icon-wrapper svg {
            fill: #FFC107;
        }
        .achievement-item .title {
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            color: #1E88E5;
            font-size: 1.25em;
            text-align: center;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Barra de Progresso (NOVO) */
        .progress-bar-container {
            position: fixed; /* Fixa a barra no topo */
            top: 0;
            left: 0;
            width: 100%; /* Ocupa toda a largura */
            background-color: transparent; /* Fundo transparente para o container */
            height: 60px; /* Mais alta e chamativa */
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1001; /* Garante que fique acima de tudo */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2); /* Sombra para a barra inteira, como um elemento flutuante */
        }

        .progress-bar-inner {
            background-color: #CFD8DC; /* Cinza claro para o track interno */
            height: 25px; /* Altura da trilha interna */
            width: 90%; /* Ocupa a maior parte da largura do container */
            border-radius: 12px;
            overflow: hidden;
            box-shadow: inset 0 1px 5px rgba(0,0,0,0.2);
            position: relative;
        }

        /* Barra de Progresso - PREENCHIMENTO DINÂMICO */
        .progress-bar-fill {
            height: 100%;
            width: 0%; /* Começa em zero para animação */
            border-radius: 12px;
            /* background será definido por JS para transição de cores */
            display: flex;
            align-items: center;
            justify-content: flex-end;
            padding-right: 10px; /* Mais padding */
            box-sizing: border-box;
            color: #FFFFFF; /* Texto branco para melhor contraste no verde */
            font-weight: 800; /* Extra bold */
            font-size: 0.9em; /* Maior */
            text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
            transition: width 0.5s ease-out, background 0.5s ease-out; /* Transição para cor também */
            position: relative;
            overflow: hidden;
        }
        .progress-bar-fill::after { /* Efeito de brilho animado na barra */
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 50%;
            height: 100%;
            background: rgba(255,255,255,0.3);
            transform: skewX(-20deg);
            animation: progress-shine 3s infinite linear;
            animation-delay: 0.5s; /* Atraso para aparecer após o preenchimento */
        }
        @keyframes progress-shine {
            0% { left: -100%; }
            100% { left: 150%; }
        }

        .progress-bar-label {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            color: #FFFFFF; /* Branco para o texto do label principal */
            font-weight: 700;
            font-size: 1.1em; /* Maior */
            line-height: 25px; /* Centraliza verticalmente */
            text-shadow: 0 1px 2px rgba(0,0,0,0.1);
        }

        /* Rodapé */
        footer {
            background-color: #212529; /* Fundo preto/carvão bem escuro */
            color: #F8F9FA; /* Texto claro */
            padding: 60px 0; /* Más padding */
            text-align: center;
            font-size: 1.05em; /* Texto mayor */
            margin-top: 80px;
            border-top: 5px solid #1E88E5; /* Linha de destaque azul */
            box-shadow: 0 -5px 15px rgba(0, 0, 0, 0.2);
        }

        footer p {
            margin: 0;
            font-weight: 300;
        }

        /* Classes para animação on scroll (aparecer ao rolar) */
        .animated-section {
            opacity: 0;
            transform: translateY(50px);
            transition: opacity 1s ease-out, transform 1s ease-out;
        }
        .animated-section.is-visible {
            opacity: 1;
            transform: translateY(0);
        }


        /* Responsividade otimizada */
        @media (max-width: 992px) {
            body { padding-top: 70px; } /* Ajusta padding para telas menores */
            .container {
                padding: 0 20px;
            }
            .hero h2 {
                font-size: 3.5em;
            }
            .hero p {
                font-size: 1.3em;
            }
            .cta-button {
                font-size: 1.8em;
                padding: 18px 35px;
            }
            .section h3 {
                font-size: 2.8em;
            }
            .features-grid {
                grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            }
            .feature-item {
                padding: 30px;
            }
            .offers-container {
                flex-direction: column; /* Colunas em telas menores */
                align-items: center;
            }
            .price-box {
                flex: 1 1 90%; /* Ocupa quase toda a largura em telas menores */
                max-width: 500px; /* Limite para não ficar muito largo */
            }
            .price-box .new-price {
                font-size: 4em; /* Ajuste para o preço em telas menores */
            }
            .price-box::before {
                font-size: 0.9em;
                padding: 6px 50px;
            }
            .super-offer {
                transform: scale(1); /* Remove o destaque inicial em telas menores */
            }
            .super-offer:hover {
                transform: translateY(-10px) scale(1.03); /* Ajusta o hover */
            }
            .info-list li {
                font-size: 1.1em;
                padding: 18px 25px;
            }
            .image-gallery {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            }
            .testimonial-grid {
                grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            }
            .achievements-grid {
                grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
                gap: 25px;
            }
            .achievement-item {
                min-height: 160px;
            }
            .achievement-item .icon-wrapper {
                width: 65px;
                height: 65px;
            }
            .achievement-item .icon-wrapper svg {
                width: 38px;
                height: 38px;
            }
            .progress-bar-container {
                height: 50px;
            }
            .progress-bar-inner {
                height: 22px;
            }
            .progress-bar-label {
                font-size: 0.9em;
                line-height: 22px;
            }
        }

        @media (max-width: 768px) {
            body { padding-top: 60px; } /* Ajusta padding para telas menores */
            header .logo-text {
                font-size: 3em;
            }
            header h1 {
                font-size: 1.4em;
            }
            .hero h2 {
                font-size: 3em;
            }
            .hero p {
                font-size: 1.2em;
                margin-bottom: 40px;
            }
            .cta-button {
                font-size: 1.6em;
                padding: 16px 30px;
            }
            .section {
                padding: 60px 0;
            }
            .section h3 {
                font-size: 2.5em;
                margin-bottom: 35px;
            }
            .features-grid {
                grid-template-columns: 1fr; /* Uma coluna em telas menores */
                gap: 25px;
            }
            .feature-item h4 {
                font-size: 1.6em;
            }
            .feature-item p {
                font-size: 1.05em;
            }
            .price-box {
                padding: 35px; /* Ajustado */
            }
            .price-box .new-price {
                font-size: 3.5em; /* Ajustado */
            }
            .normal-offer .cta-button, .super-offer .cta-button {
                font-size: 1.4em;
                padding: 14px 25px;
            }
            .super-offer h4 {
                font-size: 2.2em;
            }
            .super-offer .new-price {
                font-size: 4.5em;
            }
            .info-list li {
                font-size: 1.1em;
                padding: 16px 20px;
            }
            .image-gallery {
                grid-template-columns: 1fr;
            }
            .testimonial-grid {
                grid-template-columns: 1fr;
            }
            .achievements-grid {
                grid-template-columns: repeat(2, 1fr); /* 2 colunas em mobile */
            }
        }

        @media (max-width: 480px) {
            body { padding-top: 50px; } /* Ajusta padding para telas menores */
            header .logo-text {
                font-size: 2.5em;
                letter-spacing: 2px;
            }
            header h1 {
                font-size: 1.2em;
            }
            .hero h2 {
                font-size: 2.5em;
            }
            .hero p {
                font-size: 1em;
            }
            .cta-button {
                font-size: 1.3em;
                padding: 14px 25px;
            }
            .section h3 {
                font-size: 2em;
                margin-bottom: 30px;
            }
            .price-box .new-price {
                font-size: 3em; /* Ajustado */
            }
            .price-box::before {
                font-size: 0.8em;
                padding: 5px 40px;
                top: 15px;
                left: -60px;
            }
            .info-list li {
                font-size: 1em;
                padding: 14px 18px;
            }
            .achievements-grid {
                grid-template-columns: 1fr;
            }
            .progress-bar-container {
                height: 40px;
            }
            .progress-bar-inner {
                height: 18px;
            }
            .progress-bar-label {
                font-size: 0.8em;
                line-height: 18px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <div class="logo-text">ESPERANÇA KIDS</div>
            <h1>Sua Jornada Épica Começa Aqui: <span class="color-primary">Mestre da EBD</span>!</h1>
        </div>
    </header>

    <main>
        <div class="progress-bar-container" id="progress-bar">
            <div class="progress-bar-inner">
                <div class="progress-bar-fill" style="width: 0%;"></div>
            </div>
            <span class="progress-bar-label">Fase 1: Reconhecimento de Terreno (0%)</span>
        </div>

        <section class="hero animated-section">
            <div class="container">
                <h2>Sua EBD em <span class="color-danger">Alerta Vermelho</span>? A <span class="color-secondary">Missão Começa Agora</span>!</h2>
                <p>Ei, líder. Pai. Professor. A gente sabe o que você sente. Aquela sensação de que o <span class="text-bold">tempo está contra você</span>, escorrendo como areia pelos dedos. Aquele <span class="color-danger">frio na espinha</span> ao ver os olhos das crianças vidrados no celular, mas vazios quando você tenta falar da Bíblia. <span class="text-bold">A verdade nua e crua é:</span> você está <span class="color-danger">exausto</span> de se virar nos trinta, buscando materiais que nunca preenchem o vazio, que não acendem a chama. E a <span class="color-danger">culpa</span>? Ah, a culpa de sentir que não está fazendo o suficiente para fixar a Palavra de Deus nos corações dos pequenos...</p>
                <a href="#proximo-desafio" class="cta-button">INICIAR MISSÃO ALPHA!</a>
            </div>
        </section>

        <section class="section animated-section" id="proximo-desafio">
            <div class="container">
                <h3>Desafios do <span class="text-bold">Kit Rei Davi</span>: Conquiste a Atenção!</h3>
                <p style="font-size: 1.15em; max-width: 700px; margin: 0 auto 50px; font-weight: 300;">A gente mergulhou fundo no caos e desenterrou o que realmente funciona. O <span class="text-bold">Kit Rei Davi: 1500 Atividades Bíblicas Ilustradas e PRONTAS PARA IMPRIMIR!</span> Isso não é um e-book qualquer; é a sua <span class="color-primary">arma secreta</span>, a sua equipe de resgate, o <span class="color-primary">golpe final</span> contra o desinteresse e a falta de tempo. É o <span class="color-primary">mecanismo definitivo</span> para que as crianças <span class="color-accent">amem</span> a Bíblia e <span class="color-accent">vivam</span> a fé.</p>

                <div class="features-grid">
                    <div class="feature-item">
                        <h4>Desafio 1: Histórias que Incendeiam a Alma</h4>
                        <p>Nada de contos de ninar. Textos que prendem a <span class="text-bold">atenção</span>, com lições que se gravam para sempre. Suas crianças não vão apenas ouvir; elas vão <span class="color-accent"><strong>sentir</strong> a Palavra</span>!</p>
                    </div>
                    <div class="feature-item">
                        <h4>Desafio 2: Desenhos para Colorir que Liberam a Criatividade (e a Fé!)</h4>
                        <p>Diga adeus aos rabiscos sem vida. Cada página é uma <span class="color-secondary">missão artística</span> que aprofunda o <span class="text-bold">entendimento</span> e a <span class="text-bold">memorização</span> de passagens essenciais.</p>
                    </div>
                    <div class="feature-item">
                        <h4>Desafio 3: Jogos Interativos que Vão Transformar a Bíblia em Vício Saudável</h4>
                        <p><span class="color-primary">Cruzadinhas</span>, <span class="color-primary">caça-palavras</span>, <span class="color-primary">desafios cerebrais</span>... A diversão vai ser tanta que a molecada vai <span class="color-accent">pedir por mais Bíblia</span>!</p>
                    </div>
                    <div class="feature-item">
                        <h4>Desafio 4: Atividades por Tema, Pra Blindar a Fé da Próxima Geração</h4>
                        <p><span class="color-accent">Oração</span>, <span class="color-accent">fé</span>, <span class="color-accent">amor</span>, <span class="color-accent">obediência</span>... Tudo organizado para você construir uma <span class="text-bold">base sólida</span>, sem deixar brechas para a dúvida ou o tédio.</p>
                    </div>
                </div>
                <p style="margin-top: 50px; font-size: 1.2em; color: #495057; font-weight: 500;">Tudo ilustrado e <span class="color-secondary"><strong>pronto pra entrar em ação</strong></span>, feito sob medida para a turma toda, dos mais novinhos aos quase adolescentes! Você nunca mais vai se sentir despreparado(a).</p>
                <a href="#provas" class="cta-button">AVANÇAR PARA A PRÓXIMA FASE!</a>
            </div>
        </section>

        <!-- Nova seção para mostrar o material por dentro -->
        <section class="section animated-section" id="provas">
            <div class="container">
                <h3>Campo de Treinamento: Veja o Arsenal em Ação!</h3>
                <p style="font-size: 1.15em; max-width: 700px; margin: 0 auto 40px; font-weight: 300;">Prepare-se para o <span class="text-bold">campo de batalha do ensino</span>! Dê uma espiada no que espera por você e pelas crianças. Atividades <span class="color-accent">vibrantes</span>, criadas com <span class="color-secondary">carinho e propósito</span>!</p>
                <div class="image-gallery">
                    <!-- Imagem do material 1 -->
                    <img src="https://i.postimg.cc/5j6j4k7b/image-bae674.jpg" alt="Criança colorindo uma atividade bíblica de labirinto." onerror="this.onerror=null;this.src='https://placehold.co/400x300/e0e0e0/555555?text=IMAGEM+DO+MATERIAL+1';" />
                    <!-- Imagem do material 2 -->
                    <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749581785/crian%C3%A7a_escrevendo_qovysn.png" alt="Criança escrevendo em atividade bíblica." onerror="this.onerror=null;this.src='https://placehold.co/400x300/e0e0e0/555555?text=IMAGEM+DO+MATERIAL+2';" />
                    <!-- Imagem do material 3 -->
                    <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749581784/Captura_de_tela_2025-06-10_155601_wq8ml9.png" alt="Mais atividades do Kit Rei Davi." onerror="this.onerror=null;this.src='https://placehold.co/400x300/e0e0e0/555555?text=IMAGEM+DO+MATERIAL+3';" />
                    <!-- Nova imagem adicionada aqui, como a 4ª imagem do carrossel -->
                    <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749583213/crian%C3%A7a_sentada_vendo_o_material_dkaqnt.png" alt="Criança sentada vendo o material do Kit Rei Davi." onerror="this.onerror=null;this.src='https://placehold.co/400x300/e0e0e0/555555?text=NOVA+IMAGEM+4';" />
                </div>
                <a href="#relatorios" class="cta-button">CONFERIR RELATÓRIOS DE SUCESSO!</a>
            </div>
        </section>

        <!-- Nova seção para depoimentos (testemunhos) -->
        <section class="section animated-section" id="relatorios">
            <div class="container">
                <h3>Registro de Sucesso: Relatórios de Missão Concluída!</h3>
                <p style="font-size: 1.15em; max-width: 700px; margin: 0 auto 40px; font-weight: 300;">Não acredite apenas na nossa palavra. Veja o que <span class="text-bold">líderes e pais reais</span> que já entraram nessa <span class="color-primary">missão</span> estão dizendo sobre a <span class="color-accent">transformação</span> que o Kit trouxe!</p>
                <div class="testimonial-grid">
                    <div class="testimonial-item">
                        <p>"Oii, agradeço muito pela contribuição, que Deus lhe abençoe cada vez mais! Vcs são benção pra minha vida, vou imprimir e fazer com os meus filhinhos"</p>
                        <div class="author">- Aliado Satisfeito via Comunicação Secreta</div>
                        <!-- Depoimento do WhatsApp -->
                        <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749577956/depoimento_no_wpp_oq7w8x.png" alt="Screenshot de depoimento de cliente via WhatsApp" style="max-width: 100%; height: auto; border-radius: 8px; margin-top: 15px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onerror="this.onerror=null;this.src='https://placehold.co/300x200/e0e0e0/555555?text=DEPOIMENTO+DE+CLIENTE';" />
                    </div>
                    <!-- Imagem movida do carrossel para depoimentos -->
                    <div class="testimonial-item">
                        <p>Nosso material é um divisor de águas! Ver a alegria e o foco das crianças nas atividades bíblicas é a nossa maior recompensa. Um verdadeiro tesouro para o ensino!</p>
                        <div class="author">- Experiência real com o Kit Rei Davi</div>
                        <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749579311/Captura_de_tela_2025-06-10_151448_xdtqbu.png" alt="Mais atividades do Kit Rei Davi em uso." style="max-width: 100%; height: auto; border-radius: 8px; margin-top: 15px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onerror="this.onerror=null;this.src='https://placehold.co/300x200/e0e0e0/555555?text=DEPOIMENTO+VISUAL+1';" />
                    </div>
                    <!-- Segunda imagem movida do carrossel para depoimentos -->
                    <div class="testimonial-item">
                        <p>Atenção Total! As crianças estão amando. O Kit Rei Davi trouxe um novo fôlego para nossas aulas, com atividades que prendem a atenção e geram resultados visíveis. Recomendamos de olhos fechados!</p>
                        <div class="author">- Mestre da EBD Satisfeito</div>
                        <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749579042/Captura_de_tela_2025-06-10_151000_szs6mm.png" alt="Material do Kit Rei Davi em uso, mostrando engajamento." style="max-width: 100%; height: auto; border-radius: 8px; margin-top: 15px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onerror="this.onerror=null;this.src='https://placehold.co/300x200/e0e0e0/555555?text=DEPOIMENTO+VISUAL+2';" />
                    </div>
                    <!-- Nova imagem adicionada aos depoimentos (mantida) -->
                    <div class="testimonial-item">
                        <p>Este material é um verdadeiro achado! Facilitou muito meu planejamento e as crianças aprenderam de forma divertida e eficaz. A fé cresce a cada atividade!</p>
                        <div class="author">- Líder de Crianças Inspirado</div>
                        <img src="https://res.cloudinary.com/dwkddzdqs/image/upload/v1749579850/Captura_de_tela_2025-06-10_152355_jut78u.png" alt="Crianças com o Kit Rei Davi, felizes e engajadas." style="max-width: 100%; height: auto; border-radius: 8px; margin-top: 15px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);" onerror="this.onerror=null;this.src='https://placehold.co/300x200/e0e0e0/555555?text=DEPOIMENTO+VISUAL+3';" />
                    </div>
                </div>
                <a href="#conquistas" class="cta-button">VER CONQUISTAS DESBLOQUEADAS!</a>
            </div>
        </section>

        <!-- Nova seção de Conquistas/Progresso -->
        <section class="section achievements-section animated-section" id="conquistas">
            <div class="container">
                <h3>Sua Jornada de Mestre Bíblico: <span class="color-accent">Conquistas Desbloqueadas</span>!</h3>
                <p style="font-size: 1.15em; max-width: 700px; margin: 0 auto 40px; font-weight: 300;">Cada passo com o <span class="text-bold">Kit Rei Davi</span> é uma <span class="color-accent">vitória</span>. Prepare-se para <span class="color-primary">desbloquear um novo nível</span> de ensino!</p>
                <div class="achievements-grid">
                    <div class="achievement-item">
                        <div class="icon-wrapper">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>
                        </div>
                        <div class="title">Nível 1: Super Professor</div>
                    </div>
                    <div class="achievement-item">
                        <div class="icon-wrapper">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg>
                        </div>
                        <div class="title">Crianças Engajadas</div>
                    </div>
                    <div class="achievement-item">
                        <div class="icon-wrapper">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.7-7 8.94V12H5V6.3l7-3.11v7.8z"/></svg>
                        </div>
                        <div class="title">Fé Blindada</div>
                    </div>
                    <div class="achievement-item">
                        <div class="icon-wrapper">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21 12 17.27 18.18 21l-1.64-7.03L22 9.24zM12 15.4l-3.76 2.27 1-4.28-3.32-2.88 4.38-.38L12 6.1l1.71 4.04 4.38.38-3.32 2.88 1 4.28L12 15.4z"/></svg>
                        </div>
                        <div class="title">Tempo Otimizado</div>
                    </div>
                </div>
                <a href="#garanta" class="cta-button">PRONTO PARA O PRÓXIMO NÍVEL?</a>
            </div>
        </section>


        <section class="section animated-section" id="garanta">
            <div class="container">
                <h3>Sua Jornada de Mestre: Escolha Seu Pacote de Poder!</h3>
                <p style="font-size: 1.15em; max-width: 700px; font-weight: 300; margin: 0 auto 40px;">Preparado para <span class="color-primary">escalar o ensino bíblico</span>? Temos <span class="text-bold">duas opções brutais</span> para você, cada uma um <span class="color-accent">nível de poder</span>!</p>

                <div class="offers-container">

                    <!-- OFERTA NORMAL (R$3,90) -->
                    <div class="price-box normal-offer">
                        <h4>Pacote TÁTICO: A Base da Sua Missão!</h4>
                        <p class="old-price">De R$ 49,90... Por apenas</p>
                        <p class="new-price">R$ 13,<span>00</span>!</p>
                        <p class="symbolic-value">Sua porta de entrada para a <span class="color-primary">revolução na EBD</span>!</p>
                        <a href="#" class="cta-button">RECRUTE-SE AGORA!</a>
                        <ul>
                            <li>1500 Atividades Bíblicas Ilustradas (Prontas para Imprimir!)</li>
                            <li>Histórias Bíblicas Cativantes</li>
                            <li>Desenhos para Colorir</li>
                            <li>Jogos Interativos e Educativos</li>
                            <li>Atividades por Tema</li>
                        </ul>
                    </div>

                    <!-- SUPER OFERTA (R$37,00) -->
                    <div class="price-box super-offer">
                        <h4>Pacote ELITE: Domine o Campo de Batalha!</h4>
                        <p class="old-price">De R$ 127,90... Por apenas</p>
                        <p class="new-price">R$ 37,<span>00</span>!</p>
                        <p class="symbolic-value">O <span class="color-accent">investimento estratégico</span> para <span class="color-primary">dominar o campo de batalha</span>!</p>
                        <a href="#" class="cta-button">ACESSO IMEDIATO!</a>
                        <ul>
                            <li><strong>Tudo do Pacote TÁTICO</strong></li>
                            <li><strong>BÔNUS EXCLUSIVO 1:</strong> Kit de Historinhas Bíblicas Completas (Conteúdo narrativo extra para suas missões!)</li>
                            <li><strong>BÔNUS EXCLUSIVO 2:</strong> Mega Pack de Atividades para Colorir (Dezenas de novas páginas para desafios criativos!)</li>
                            <li>Acesso Vitalício e Atualizações Futuras!</li>
                        </ul>
                    </div>

                </div>
            </div>
        </section>

        <section class="section animated-section">
            <div class="container">
                <h3>Manual de Operações: Pronto para o Desdobramento?</h3>
                <p style="font-size: 1.15em; max-width: 700px; margin: 0 auto 40px; font-weight: 300;">Todas as suas dúvidas sobre o Kit Rei Davi, respondidas para você iniciar sua missão com total confiança!</p>
                <ul class="info-list">
                    <li onclick="toggleFaq(this)">
                        <span class="icon arrow">▶</span>
                        <strong>É impresso?</strong>
                        <p>Negativo, Mestre! O Kit Rei Davi é um produto <span class="text-bold">100% digital</span> em formato PDF. Isso significa que você recebe o material instantaneamente, pode <span class="color-accent">imprimir quantas vezes quiser</span> (e quando quiser!), adaptando-se perfeitamente às suas necessidades. Chega de esperar por entregas ou pagar frete!</p>
                    </li>
                    <li onclick="toggleFaq(this)">
                        <span class="icon arrow">▶</span>
                        <strong>Como recebo o arsenal?</strong>
                        <p>Sua missão começa sem atrasos! Após a confirmação do pagamento, você receberá o acesso <span class="color-accent"><strong>IMEDIATO</strong></span> ao Kit Rei Davi diretamente no seu e-mail ou via WhatsApp. Tudo organizado em um link seguro para download. Simples assim, em poucos cliques você estará com seu arsenal em mãos!</p>
                    </li>
                    <li onclick="toggleFaq(this)">
                        <span class="icon arrow">▶</span>
                        <strong>Posso usar na igreja, EBD, ou em casa?</strong>
                        <p>Absolutamente! O Kit Rei Davi é um material <span class="text-bold">versátil</span>, criado para ser seu melhor aliado em qualquer cenário de ensino bíblico infantil. É ideal para: <span class="color-accent">EBD (Escola Bíblica Dominical)</span>, <span class="color-accent">Culto Infantil</span>, <span class="color-accent">Discipulados</span>, aulas em pequenos grupos ou para enriquecer o <span class="color-accent">ensino da Palavra de Deus em casa</span> com seus próprios filhos. Ele foi projetado para <span class="text-bold">engajar as crianças</span> e facilitar a sua vida, não importa onde a missão aconteça!</p>
                    </li>
                    <li onclick="toggleFaq(this)">
                        <span class="icon arrow">▶</span>
                        <strong>Para quais idades o material é recomendado?</strong>
                        <p>O Kit Rei Davi foi cuidadosamente desenvolvido para abranger <span class="color-accent">diversas faixas etárias</span> dentro do público infantil. Com 1500 atividades, você encontrará desde desenhos simples para os mais novos (3-6 anos), até cruzadinhas, caça-palavras e atividades temáticas mais elaboradas para crianças em idade escolar (7-12 anos). Isso garante que você sempre terá o material certo para o nível de compreensão de cada criança.</p>
                    </li>
                    <li onclick="toggleFaq(this)">
                        <span class="icon arrow">▶</span>
                        <strong>Preciso de algo especial para usar o material?</strong>
                        <p>Não, Mestre! Você só precisa de um computador, tablet ou celular para acessar os arquivos em PDF. Para imprimir, qualquer impressora doméstica ou copiadora funciona. As atividades são <span class="color-accent">prontas para usar</span>, sem a necessidade de softwares complexos ou materiais caros. Simplicidade é a nossa arma secreta para sua eficiência!</p>
                    </li>
                </ul>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Esperança Kids. Todos os direitos reservados. Não nos responsabilizamos por surtos de criatividade e super-heróis da EBD.</p>
        </div>
    </footer>

    <script>
        // Helper function to interpolate between two colors (RGB values)
        function interpolateColor(color1, color2, factor) {
            const result = color1.slice(); // Copy array
            for (let i = 0; i < 3; i++) {
                result[i] = Math.round(result[i] + factor * (color2[i] - color1[i]));
            }
            return `rgb(${result[0]}, ${result[1]}, ${result[2]})`;
        }

        // Convert hex to RGB array
        function hexToRgb(hex) {
            const bigint = parseInt(hex.slice(1), 16);
            const r = (bigint >> 16) & 255;
            const g = (bigint >> 8) & 255;
            const b = bigint & 255;
            return [r, g, b];
        }

        // Define main colors for interpolation
        const colorRed = hexToRgb('#DC3545');   // Vermelho inicial
        const colorYellow = hexToRgb('#FFC107'); // Amarelo intermediário
        const colorGreen = hexToRgb('#28A745');  // Verde final

        // Função para atualizar a barra de progresso e o rótulo com base na rolagem
        function updateProgressBarOnScroll() {
            const progressBarFill = document.querySelector('.progress-bar-fill');
            const progressBarLabel = document.querySelector('.progress-bar-label');
            const sections = document.querySelectorAll('section');

            const totalHeight = document.documentElement.scrollHeight - window.innerHeight;
            const scrollPosition = window.scrollY;

            let scrollPercentage = (scrollPosition / totalHeight) * 100;
            scrollPercentage = Math.min(100, Math.max(0, scrollPercentage));

            // Atualiza a largura da barra de preenchimento
            progressBarFill.style.width = scrollPercentage + '%';

            // Lógica de transição de cor da barra de preenchimento
            let currentColor;
            if (scrollPercentage <= 30) {
                // Transiciona de vermelho para amarelo nos primeiros 30%
                currentColor = interpolateColor(colorRed, colorYellow, scrollPercentage / 30);
            } else if (scrollPercentage > 30 && scrollPercentage <= 85) {
                // Transiciona de amarelo para verde nos próximos 55% (até 85%)
                const factor = (scrollPercentage - 30) / 55; // (85 - 30 = 55)
                currentColor = interpolateColor(colorYellow, colorGreen, factor);
            } else {
                // Permanece verde nos últimos 15% (após 85%)
                currentColor = colorGreen;
            }
            progressBarFill.style.background = currentColor;


            // Lógica para o texto do rótulo da barra de progresso
            let currentLabel = 'Fase 1: Reconhecimento de Terreno';
            let currentPercentageDisplayed = Math.round(scrollPercentage);

            if (scrollPercentage > 15 && scrollPercentage <= 40) {
                currentLabel = 'Fase 2: Imersão no Arsenal';
            } else if (scrollPercentage > 40 && scrollPercentage <= 65) {
                currentLabel = 'Fase 3: Análise de Batalha';
            } else if (scrollPercentage > 65 && scrollPercentage <= 85) {
                currentLabel = 'Fase 4: Verificando Relatórios';
            } else if (scrollPercentage > 85 && scrollPercentage < 100) {
                currentLabel = 'Fase 5: Conquistas Desbloqueadas!';
            } else if (scrollPercentage >= 100) {
                currentLabel = 'Fase Final: Escolha Seu Arsenal!';
            }

            progressBarLabel.textContent = currentLabel + ` (${currentPercentageDisplayed}%)`;
        }

        // Função para expandir/recolher o FAQ
        function toggleFaq(element) {
            element.classList.toggle('open');
            const paragraph = element.querySelector('p');
            const icon = element.querySelector('.icon.arrow');

            if (element.classList.contains('open')) {
                paragraph.style.maxHeight = paragraph.scrollHeight + "px"; // Expande para o tamanho real
                icon.style.transform = "rotate(90deg)"; // Gira a seta
            } else {
                paragraph.style.maxHeight = "0"; // Recolhe
                icon.style.transform = "rotate(0deg)"; // Volta a seta
            }
        }

        // Observador de Interseção para animações de rolagem
        const observerOptions = {
            root: null, /* viewport */
            rootMargin: '0px',
            threshold: 0.1 /* 10% do elemento visível */
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                    /* observer.unobserve(entry.target); /* Para animar apenas uma vez */
                } else {
                    /* entry.target.classList.remove('is-visible'); /* Para animar toda vez que entra/sai */
                }
            });
        }, observerOptions);

        document.querySelectorAll('.animated-section').forEach(section => {
            observer.observe(section);
        });


        // Adiciona o listener de scroll ao carregar a página
        window.addEventListener('scroll', updateProgressBarOnScroll);

        // Inicializa a barra de progresso no carregamento inicial da página
        window.onload = function() {
            updateProgressBarOnScroll(); // Chama para definir o estado inicial
            // Adiciona um pequeno atraso para as animações iniciais aparecerem
            setTimeout(() => {
                document.querySelector('.hero').classList.add('is-visible');
            }, 100);
        };
    </script>
</body>
</html>
