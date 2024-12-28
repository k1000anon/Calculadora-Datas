<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chat P2P</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        #chat-container {
            width: 500px;
            height: 400px;
            border: 1px solid #ccc;
            display: flex;
            flex-direction: column;
        }
        #messages {
            flex-grow: 1;
            overflow-y: auto;
            padding: 10px;
            background-color: #fff;
            margin-bottom: 10px;
            border-bottom: 1px solid #ccc;
        }
        #input-container {
            display: flex;
        }
        input[type="text"] {
            width: 80%;
            padding: 10px;
            font-size: 16px;
        }
        button {
            padding: 10px;
            font-size: 16px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <h1>Chat P2P</h1>
    <div id="chat-container">
        <div id="messages"></div>
        <div id="input-container">
            <input type="text" id="messageInput" placeholder="Digite uma mensagem..." />
            <button onclick="sendMessage()">Enviar</button>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/peerjs@1.3.1/dist/peerjs.min.js"></script>
    <script>
        let peer;  // Será atribuído após a inserção do ID
        let conn;  // Variável para armazenar a conexão com o outro peer

        // Função para inicializar o Peer com um ID personalizado
        function initializePeer() {
            const customId = prompt("Digite um ID para o seu peer:");
            if (customId) {
                // Cria o peer com o ID personalizado
                peer = new Peer(customId);
                
                // Evento 'open' quando o peer está pronto
                peer.on('open', function(id) {
                    document.getElementById('messages').innerHTML += `<div><strong>Seu ID:</strong> ${id}</div>`;
                });

                peer.on('connection', function(connection) {
                    conn = connection;
                    conn.on('data', function(data) {
                        displayMessage(data, 'Outro Usuário');
                    });
                });
            } else {
                alert("ID inválido. Por favor, forneça um ID.");
            }
        }

        // Conexão com outro peer
        function connectToPeer() {
            const peerId = prompt('Digite o ID do outro usuário:');
            if (peerId && peer) {
                conn = peer.connect(peerId);
                conn.on('open', function() {
                    conn.on('data', function(data) {
                        displayMessage(data, 'Outro Usuário');
                    });
                });
            }
        }

        // Enviar mensagem
        function sendMessage() {
            const messageInput = document.getElementById('messageInput');
            const message = messageInput.value.trim();
            if (message && conn) {
                conn.send(message); // Envia a mensagem sem criptografia
                displayMessage(message, 'Você');
                messageInput.value = ''; // Limpa o campo de entrada
            } else {
                alert('Conecte-se a outro peer antes de enviar a mensagem');
            }
        }

        // Exibe a mensagem na tela
        function displayMessage(message, fromUser) {
            const messagesDiv = document.getElementById('messages');
            const newMessage = document.createElement('div');
            newMessage.textContent = `${fromUser}: ${message}`;
            messagesDiv.appendChild(newMessage);
            messagesDiv.scrollTop = messagesDiv.scrollHeight;  // Rola para o fundo
        }

        // Adiciona a opção de conectar a outro peer
        document.addEventListener('DOMContentLoaded', () => {
            // Chama a função para inicializar o Peer com um ID personalizado
            initializePeer();

            // Adiciona botão para conexão
            const button = document.createElement('button');
            button.textContent = 'Conectar a outro peer';
            button.onclick = connectToPeer;
            document.body.appendChild(button);
        });
    </script>
</body>
</html>
