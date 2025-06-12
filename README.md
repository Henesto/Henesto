<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nosso Amor Desde a Escola</title>
    <style>
        :root {
            --rosa-claro: #fff0f6;
            --rosa-medio: #ffdeeb;
            --rosa-escuro: #d23669;
            --texto: #333344;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background-color: var(--rosa-claro);
            color: var(--texto);
            margin: 0;
            padding: 0;
            line-height: 1.8;
        }
        
        header {
            background: linear-gradient(135deg, var(--rosa-medio), var(--rosa-claro));
            padding: 40px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://i.imgur.com/5Z2QY9x.png') repeat;
            opacity: 0.05;
            pointer-events: none;
        }
        
        h1 {
            color: var(--rosa-escuro);
            font-size: 2.8em;
            margin-bottom: 10px;
            position: relative;
        }
        
        .subtitle {
            font-size: 1.2em;
            color: var(--texto);
            font-weight: 300;
            margin-bottom: 30px;
        }
        
        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 40px auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--rosa-medio);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
            border-radius: 3px;
        }
        
        .container {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
        }
        
        .container::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            right: -17px;
            background-color: white;
            border: 4px solid var(--rosa-escuro);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }
        
        .left {
            left: 0;
        }
        
        .right {
            left: 50%;
        }
        
        .left::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            right: 30px;
            border: medium solid var(--rosa-medio);
            border-width: 10px 0 10px 10px;
            border-color: transparent transparent transparent white;
        }
        
        .right::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            left: 30px;
            border: medium solid var(--rosa-medio);
            border-width: 10px 10px 10px 0;
            border-color: transparent white transparent transparent;
        }
        
        .right::after {
            left: -16px;
        }
        
        .content {
            padding: 20px 30px;
            background-color: white;
            position: relative;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 40px auto;
            max-width: 1200px;
            padding: 0 20px;
        }
        
        .gallery img {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }
        
        .gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
        }
        
        .music-player {
            margin: 40px auto;
            max-width: 560px;
            padding: 0 20px;
        }
        
        .quote {
            font-style: italic;
            font-size: 1.3em;
            text-align: center;
            max-width: 800px;
            margin: 50px auto;
            padding: 30px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            position: relative;
        }
        
        .quote::before, .quote::after {
            content: '"';
            font-size: 2em;
            color: var(--rosa-escuro);
            position: absolute;
        }
        
        .quote::before {
            top: 10px;
            left: 10px;
        }
        
        .quote::after {
            bottom: 10px;
            right: 10px;
        }
        
        .message-wall {
            max-width: 800px;
            margin: 40px auto;
            padding: 30px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .message-input {
            width: 100%;
            padding: 15px;
            border: 2px solid var(--rosa-medio);
            border-radius: 8px;
            margin-bottom: 15px;
            font-family: inherit;
            resize: vertical;
            min-height: 100px;
        }
        
        .btn {
            background-color: var(--rosa-escuro);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 1em;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #a52d52;
            transform: translateY(-2px);
        }
        
        .messages-container {
            margin-top: 30px;
        }
        
        .message {
            background-color: var(--rosa-claro);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 4px solid var(--rosa-escuro);
        }
        
        footer {
            text-align: center;
            padding: 30px;
            background-color: var(--rosa-medio);
            margin-top: 50px;
        }
        
        @media screen and (max-width: 768px) {
            .timeline::after {
                left: 31px;
            }
            
            .container {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .container::before {
                left: 60px;
                border: medium solid var(--rosa-medio);
                border-width: 10px 10px 10px 0;
                border-color: transparent white transparent transparent;
            }
            
            .left::after, .right::after {
                left: 15px;
            }
            
            .right {
                left: 0%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Nossa História</h1>
        <div class="subtitle">Do primeiro olhar na escola ao lar no meu coração</div>
    </header>
    
    <div class="music-player">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/nSDgHBxUbVQ?autoplay=1&controls=1&loop=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    
    <div class="quote">
        "Quando eu conheci você, você vivia mudando de casa em casa. Porém depois que nós casarmos, você sempre terá um lar no meu coração"
    </div>
    
    <div class="timeline">
        <div class="container left">
            <div class="content">
                <h2>08 de Julho de 2020</h2>
                <p>Nosso primeiro encontro na escola. Ainda lembro do seu sorriso tímido e da forma como seus olhos brilhavam quando falava sobre seus sonhos. Naquele dia, sem saber, plantamos a semente do que viria a ser o amor mais lindo da minha vida.</p>
            </div>
        </div>
        <div class="container right">
            <div class="content">
                <h2>06 de Novembro de 2022</h2>
                <p>O dia em que oficialmente nossas vidas se tornaram uma só. Cada promessa feita naquele altar ecoa em meu coração todos os dias. Você não é apenas minha esposa, é meu porto seguro, minha parceira em todas as aventuras.</p>
            </div>
        </div>
    </div>
    
    <div class="gallery">
        <!-- Fotos do álbum do Google Fotos -->
        <iframe src="https://photos.app.goo.gl/YhiVbuUy5Re8bh9t6" width="100%" height="600" frameborder="0" style="border:none;"></iframe>
        <!-- Nota: O embed do Google Fotos pode não funcionar perfeitamente. Alternativa: baixar as fotos e hospedar separadamente -->
    </div>
    
    <div class="message-wall">
        <h2 style="text-align: center; color: var(--rosa-escuro);">Mural de Mensagens</h2>
        <textarea class="message-input" placeholder="Deixe uma mensagem de amor..."></textarea>
        <button class="btn">Enviar Mensagem</button>
        
        <div class="messages-container">
            <!-- Mensagens aparecerão aqui -->
        </div>
    </div>
    
    <footer>
        <p>Feito com ❤️ para você, minha eterna paixão</p>
    </footer>
    
    <script>
        // Script para o mural de mensagens
        document.querySelector('.btn').addEventListener('click', function() {
            const messageInput = document.querySelector('.message-input');
            const message = messageInput.value.trim();
            
            if (message) {
                const messagesContainer = document.querySelector('.messages-container');
                const newMessage = document.createElement('div');
                newMessage.className = 'message';
                newMessage.textContent = message;
                messagesContainer.prepend(newMessage);
                
                messageInput.value = '';
            }
        });
        
        // Permitir enviar mensagem com Enter
        document.querySelector('.message-input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter' && !e.shiftKey) {
                e.preventDefault();
                document.querySelector('.btn').click();
            }
        });
    </script>
</body>
</html>
