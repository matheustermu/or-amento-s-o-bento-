
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gerador de Orçamento - Posto de Molas São Bento</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #007bff; /* Azul primário */
            --secondary-color: #28a745; /* Verde para botões de sucesso */
            --danger-color: #dc3545; /* Vermelho para botões de remoção */
            --info-color: #17a2b8; /* Azul-ciano para salvar PDF */
            --bg-color: #f8f9fa; /* Fundo claro */
            --card-bg: #ffffff; /* Fundo dos cards */
            --text-color: #343a40; /* Cor de texto principal */
            --border-color: #e9ecef; /* Cor da borda */
            --shadow-light: rgba(0, 0, 0, 0.1);
            --shadow-medium: rgba(0, 0, 0, 0.15);
        }

        body {
            font-family: 'Roboto', Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 0;
            margin: 0;
            background-color: var(--bg-color);
            min-height: 100vh;
            width: 100vw;
            overflow-x: hidden;
            color: var(--text-color);
        }

        h1 {
            color: var(--primary-color);
            margin-top: 30px;
            margin-bottom: 25px;
            font-weight: 700;
            text-shadow: 1px 1px 2px var(--shadow-light);
        }

        .container {
            display: flex;
            gap: 25px;
            width: 90%; /* Um pouco mais de margem nas laterais */
            max-width: 1500px; /* Aumenta a largura máxima */
            margin-bottom: 30px;
            flex-grow: 1;
        }

        .form-section, .canvas-section {
            flex: 1;
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px var(--shadow-medium);
            transition: transform 0.3s ease-in-out;
        }

        .form-section:hover, .canvas-section:hover {
            transform: translateY(-5px);
        }

        canvas {
            border: 1px solid var(--border-color);
            background-color: #fcf9e7; /* Cor semelhante ao papel */
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: inset 0 0 5px rgba(0,0,0,0.05);
        }

        h2, h3 {
            color: var(--primary-color);
            margin-bottom: 20px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 5px;
            font-weight: 700;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-color);
            font-size: 0.95em;
        }

        input[type="text"],
        input[type="number"],
        input[type="email"],
        input[type="date"],
        select {
            width: calc(100% - 20px); /* Ajusta padding */
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            font-size: 1em;
            color: var(--text-color);
            background-color: var(--bg-color);
            box-shadow: inset 0 1px 3px var(--shadow-light);
            transition: border-color 0.3s ease;
        }

        input[type="text"]:focus,
        input[type="number"]:focus,
        input[type="email"]:focus,
        input[type="date"]:focus,
        select:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.25);
        }

        /* --- NOVOS ESTILOS PARA CAMPOS DE ADIÇÃO DE ITENS --- */
        .add-item-fields {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 20px;
            padding: 15px;
            border: 1px dashed var(--primary-color);
            border-radius: 8px;
            background-color: rgba(0, 123, 255, 0.05); /* Cor clara do tema */
        }
        .add-item-fields input {
            flex: 1;
            min-width: 90px;
            margin-bottom: 0;
            background-color: var(--card-bg); /* Input background in item fields */
        }
        .add-item-fields input[type="number"] {
            width: 90px;
            flex: none;
        }
        .add-item-fields input[type="text"].desc-input {
            flex: 4; /* Mais espaço para descrição */
            min-width: 150px;
        }

        /* --- ESTILOS PARA A LISTA DE ITENS --- */
        .item-list-container {
            margin-top: 15px;
            margin-bottom: 15px;
            border-radius: 8px;
            padding: 10px;
            background-color: var(--bg-color);
            border: 1px solid var(--border-color);
        }
        .item-display-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
            margin-bottom: 8px;
            background-color: var(--card-bg);
            border-radius: 6px;
            box-shadow: 0 2px 5px var(--shadow-light);
        }
        .item-display-row:last-child {
            margin-bottom: 0;
        }
        .item-display-row span {
            font-weight: 600;
            color: var(--text-color);
            flex-grow: 1;
            text-align: left;
            padding-right: 10px;
            font-size: 0.9em;
        }
        .item-display-row .remove-button {
            background-color: var(--danger-color);
            color: white;
            border: none;
            padding: 6px 12px;
            border-radius: 50%; /* Botão redondo */
            cursor: pointer;
            font-weight: bold;
            font-size: 0.9em;
            min-width: 30px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: background-color 0.2s ease, transform 0.2s ease;
        }
        .item-display-row .remove-button:hover {
            background-color: #c82333;
            transform: scale(1.05);
        }

        /* --- BOTÕES GERAIS --- */
        button {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 15px;
            width: 100%;
            font-size: 1.1em;
            font-weight: 700;
            transition: background-color 0.2s ease, transform 0.2s ease;
            box-shadow: 0 2px 4px var(--shadow-medium);
        }
        button:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }

        /* Totais */
        .totals-section {
            margin-top: 20px;
            padding-top: 15px;
            border-top: 2px dashed var(--border-color);
        }
        .totals-section div {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: bold;
            font-size: 1.1em;
            color: var(--text-color);
        }

        /* Grupo de campo de número de orçamento com botão */
        .orcamento-numero-group {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        .orcamento-numero-group input {
            margin-bottom: 0;
            flex-grow: 1;
        }
        .orcamento-numero-group button {
            width: auto;
            padding: 8px 15px;
            margin-left: 10px;
            margin-top: 0;
            background-color: var(--primary-color); /* Azul para o botão de incremento */
            box-shadow: none; /* Remove sombra para o pequeno botão */
        }
        .orcamento-numero-group button:hover {
            background-color: #0056b3;
            transform: none; /* Remove efeito de transform do botão pequeno */
        }

        /* Estilo para o botão de Salvar PDF */
        #savePdfButton {
            background-color: var(--info-color); /* Cor azul-ciano */
        }
        #savePdfButton:hover {
            background-color: #138496;
        }

        /* --- Media Queries para Responsividade --- */
        @media (max-width: 1024px) {
            .container {
                flex-direction: column;
                width: 95%;
            }
            .form-section, .canvas-section {
                flex: none;
                width: 100%;
            }
            .canvas-section {
                padding: 15px; /* Reduz padding para canvas em telas menores */
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 1.8em;
                margin-top: 20px;
                margin-bottom: 20px;
            }
            .form-section, .canvas-section {
                padding: 20px;
            }
            input[type="text"], input[type="number"], input[type="email"], input[type="date"], select, button {
                font-size: 0.95em;
                padding: 10px;
            }
            .add-item-fields input {
                min-width: 100%; /* Inputs em uma nova linha */
            }
            .add-item-fields input[type="number"], .add-item-fields input[type="text"].desc-input {
                 flex: 1; /* Permite que ocupem mais espaço */
                 width: 100%;
            }
        }

        /* --- Estilos para Impressão (PDF) - Otimizados para uma única página --- */
        @media print {
            /* Força o conteúdo a caber em uma página e remove margens padrão */
            @page {
                size: A4 portrait; /* Ou Letter portrait, dependendo da região */
                margin: 0; /* Remove todas as margens da página */
            }

            body {
                background-color: white !important;
                margin: 0;
                padding: 0;
                display: block; /* Volta para o display padrão para impressão */
                overflow: hidden; /* Remove barras de rolagem */
            }
            h1, .form-section, .add-item-fields, button, .item-list-container, .orcamento-numero-group {
                display: none !important; /* Oculta todo o formulário e botões */
            }
            .container {
                display: block; /* Volta para o display padrão */
                width: 100%; /* Ocupa a largura total da página */
                max-width: none;
                margin: 0;
                padding: 0;
            }
            .canvas-section {
                box-shadow: none !important; /* Remove sombras na impressão */
                padding: 0 !important;
                margin: 0 !important;
                background-color: white !important;
                display: block; /* Garante que o canvas section é visível */
                width: 100%; /* Ocupa a largura total da página disponível */
                height: 100vh; /* Tenta forçar a altura da viewport de impressão */
                overflow: hidden; /* Garante que nada transborde */
            }
            canvas {
                border: none !important; /* Remove borda do canvas na impressão */
                box-shadow: none !important;
                background-color: #fcf9e7 !important; /* Mantém a cor de fundo do "papel" */
                display: block;
                width: 100vw !important; /* Tenta usar a largura total da viewport de impressão */
                height: 100vh !important; /* Tenta usar a altura total da viewport de impressão */
                object-fit: contain; /* Redimensiona o canvas para caber na página sem cortar */
                page-break-after: avoid; /* Evita quebras de página depois do canvas */
                page-break-before: avoid; /* Evita quebras de página antes do canvas */
            }
        }
    </style>
</head>
<body>
    <h1>Gerador de Orçamento</h1>
    <div class="container">
        <div class="form-section">
            <h2>Dados do Orçamento</h2>

            <label for="numeroOrcamento">Nº Orçamento:</label>
            <div class="orcamento-numero-group">
                <input type="text" id="numeroOrcamento" value="2894" placeholder="Ex: 2894">
                <button onclick="incrementOrcamento()">+</button>
            </div>

            <label for="dataOrcamento">Data:</label>
            <input type="date" id="dataOrcamento" value="2025-07-16">

            <h3>Dados do Cliente</h3>
            <label for="nomeCliente">Nome:</label>
            <input type="text" id="nomeCliente" value="Transportadora Alfa Ltda." placeholder="Ex: João da Silva ou Empresa XYZ">

            <label for="enderecoCliente">Endereço:</label>
            <input type="text" id="enderecoCliente" value="Rua das Molas, 1500 - Indústria" placeholder="Ex: Rua Exemplo, 123 - Centro">

            <label for="cidadeCliente">Cidade:</label>
            <input type="text" id="cidadeCliente" value="Ponta Grossa" placeholder="Ex: Curitiba">

            <label for="ufCliente">UF:</label>
            <input type="text" id="ufCliente" value="PR" maxlength="2" placeholder="Ex: PR">

            <label for="emailCliente">E-mail:</label>
            <input type="email" id="emailCliente" value="contato@alfa.com.br" placeholder="Ex: cliente@email.com">

            <label for="telCliente">Telefone:</label>
            <input type="text" id="telCliente" value="(42) 99934-3158" placeholder="Ex: (42) 99999-9999">

            <h3>Dados do Veículo</h3>
            <label for="tipoVeiculo">Caminhão / Caminhonete:</label>
            <input type="text" id="tipoVeiculo" value="Caminhão Scania R450" placeholder="Ex: Scania P360 ou Ford Ranger">

            <label for="corVeiculo">Cor:</label>
            <input type="text" id="corVeiculo" value="Azul Metálico" placeholder="Ex: Branco ou Preto">

            <label for="placaVeiculo">Placa:</label>
            <input type="text" id="placaVeiculo" value="ABC1D20" placeholder="Ex: XYZ9E87">

            <label for="cidadeVeiculo">Cidade Veículo:</label>
            <input type="text" id="cidadeVeiculo" value="São Paulo" placeholder="Ex: São Paulo">

            <h3>Peças</h3>
            <div class="add-item-fields">
                <input type="number" id="newPecaQuant" value="2" min="0.1" step="0.1" placeholder="Quant. (Ex: 2)">
                <input type="text" id="newPecaUnid" value="UNID." placeholder="Unid. (Ex: UNID., MT, KG)">
                <input type="text" id="newPecaProduto" class="desc-input" value="Mola Dianteira - Semiacabada" placeholder="Descrição da Peça (Ex: Mola Parabólica)">
                <input type="number" id="newPecaPrecoUnit" value="280.50" min="0" step="0.01" placeholder="Preço Unit. (Ex: 150.00)">
            </div>
            <div id="pecasContainer" class="item-list-container">
            </div>
            <button onclick="addPeca()">Adicionar Peça</button>

            <h3>Serviços</h3>
            <div class="add-item-fields">
                <input type="number" id="newServicoQuant" value="1" min="0.1" step="0.1" placeholder="Quant. (Ex: 1)">
                <input type="text" id="newServicoProduto" class="desc-input" value="Alinhamento e Balanceamento Completo" placeholder="Descrição do Serviço (Ex: Troca de Amortecedores)">
                <input type="number" id="newServicoPreco" value="180.00" min="0" step="0.01" placeholder="Preço Total (Ex: 300.00)">
            </div>
            <div id="servicosContainer" class="item-list-container">
            </div>
            <button onclick="addServico()">Adicionar Serviço</button>

            <button id="savePdfButton" onclick="saveCanvasAsPdf()">Salvar PDF</button>
        </div>

        <div class="canvas-section">
            <canvas id="orcamentoCanvas" width="1000" height="1400"></canvas>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('orcamentoCanvas');
        const ctx = canvas.getContext('2d');
        const pecasContainer = document.getElementById('pecasContainer');
        const servicosContainer = document.getElementById('servicosContainer');

        // Referências para os novos campos de entrada de peças
        const newPecaQuantInput = document.getElementById('newPecaQuant');
        const newPecaUnidInput = document.getElementById('newPecaUnid');
        const newPecaProdutoInput = document.getElementById('newPecaProduto');
        const newPecaPrecoUnitInput = document.getElementById('newPecaPrecoUnit');

        // Referências para os novos campos de entrada de serviços
        const newServicoQuantInput = document.getElementById('newServicoQuant');
        const newServicoProdutoInput = document.getElementById('newServicoProduto');
        const newServicoPrecoInput = document.getElementById('newServicoPreco');


        // Dados iniciais para as peças - AGORA VAZIOS
        const initialPecas = [];

        // Dados iniciais para os serviços - AGORA VAZIOS
        const initialServicos = [];

        function formatCurrency(value) {
            return parseFloat(value).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        function renderPecas() {
            pecasContainer.innerHTML = ''; // Limpa os itens existentes
            initialPecas.forEach((item, index) => {
                const total = item.quant * item.precoUnit;
                const row = document.createElement('div');
                row.className = 'item-display-row';
                row.innerHTML = `
                    <span>${item.produto} - ${formatCurrency(total)}</span>
                    <button class="remove-button" onclick="removePeca(${index})">X</button>
                `;
                pecasContainer.appendChild(row);
            });
            drawCanvas(); // Sempre redesenha o canvas após atualizar a lista
        }

        function addPeca() {
            const quant = parseFloat(newPecaQuantInput.value);
            const unid = newPecaUnidInput.value.trim();
            const produto = newPecaProdutoInput.value.trim();
            const precoUnit = parseFloat(newPecaPrecoUnitInput.value);

            if (isNaN(quant) || quant <= 0 || !unid || !produto || isNaN(precoUnit) || precoUnit < 0) {
                alert("Por favor, preencha todos os campos da peça corretamente (Quantidade > 0, Preço Unitário >= 0).");
                return;
            }

            initialPecas.push({ quant: quant, unid: unid, produto: produto, precoUnit: precoUnit });
            renderPecas(); // Re-renderiza a lista de peças

            // Limpa os campos após adicionar
            newPecaQuantInput.value = "1";
            newPecaUnidInput.value = "UNID.";
            newPecaProdutoInput.value = "";
            newPecaPrecoUnitInput.value = "0.00";
        }

        function removePeca(index) {
            initialPecas.splice(index, 1); // Remove o item do array
            renderPecas(); // Re-renderiza a lista
        }

        function renderServicos() {
            servicosContainer.innerHTML = ''; // Limpa os itens existentes
            initialServicos.forEach((item, index) => {
                const total = item.quant * item.preco;
                const row = document.createElement('div');
                row.className = 'item-display-row';
                row.innerHTML = `
                    <span>${item.produto} - ${formatCurrency(total)}</span>
                    <button class="remove-button" onclick="removeServico(${index})">X</button>
                `;
                servicosContainer.appendChild(row);
            });
            drawCanvas(); // Sempre redesenha o canvas após atualizar a lista
        }

        function addServico() {
            const quant = parseFloat(newServicoQuantInput.value);
            const produto = newServicoProdutoInput.value.trim();
            const preco = parseFloat(newServicoPrecoInput.value);

            if (isNaN(quant) || quant <= 0 || !produto || isNaN(preco) || preco < 0) {
                alert("Por favor, preencha todos os campos do serviço corretamente (Quantidade > 0, Preço >= 0).");
                return;
            }

            initialServicos.push({ quant: quant, produto: produto, preco: preco });
            renderServicos(); // Re-renderiza a lista de serviços

            // Limpa os campos após adicionar
            newServicoQuantInput.value = "1";
            newServicoProdutoInput.value = "";
            newServicoPrecoInput.value = "0.00";
        }

        function removeServico(index) {
            initialServicos.splice(index, 1); // Remove o item do array
            renderServicos(); // Re-renderiza a lista
        }

        // Function to increment the budget number
        function incrementOrcamento() {
            const numeroOrcamentoInput = document.getElementById('numeroOrcamento');
            let currentNumber = parseInt(numeroOrcamentoInput.value, 10);
            if (!isNaN(currentNumber)) {
                numeroOrcamentoInput.value = currentNumber + 1;
            } else {
                numeroOrcamentoInput.value = "1"; // Default if not a number
            }
            drawCanvas(); // Redraw canvas to reflect the new number
        }

        // Função para salvar o canvas como PDF
        function saveCanvasAsPdf() {
            // Desenha o canvas uma última vez para garantir que está atualizado
            drawCanvas();

            // Abre a janela de impressão do navegador
            // A `@media print` no CSS cuidará de mostrar apenas o canvas
            window.print();
        }

        // Adiciona um listener para atualizar o canvas quando os dados do cliente/veículo mudam
        document.querySelectorAll('#numeroOrcamento, #dataOrcamento, #nomeCliente, #enderecoCliente, #cidadeCliente, #ufCliente, #emailCliente, #telCliente, #tipoVeiculo, #corVeiculo, #placaVeiculo, #cidadeVeiculo').forEach(input => {
            input.addEventListener('input', drawCanvas);
        });

        // Chama as funções de renderização no carregamento para exibir os dados iniciais
        document.addEventListener('DOMContentLoaded', () => {
            renderPecas();
            renderServicos();
            drawCanvas(); // Garante que o canvas seja desenhado no carregamento com os dados iniciais
        });

        // Função para quebrar texto
        function wrapText(context, text, x, y, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let lines = [];

            for (let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = context.measureText(testLine);
                let testWidth = metrics.width;
                if (testWidth > maxWidth && n > 0) {
                    lines.push(line);
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            lines.push(line);

            for (let i = 0; i < lines.length; i++) {
                context.fillText(lines[i], x, y + (i * lineHeight));
            }
            return lines.length; // Retorna o número de linhas usadas
        }

        function drawCanvas() {
            // Limpa o canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Define a cor de fundo
            ctx.fillStyle = '#fcf9e7'; // Cor semelhante ao papel
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            // Define o estilo de desenho
            ctx.font = '16px Arial'; // Tamanho de fonte um pouco maior
            ctx.fillStyle = '#333';
            ctx.strokeStyle = '#555';
            ctx.lineWidth = 1;

            let currentY = 70; // Mais espaço no topo
            const marginX = 70; // Margem lateral maior
            const lineHeight = 25; // Altura da linha um pouco maior

            // Cabeçalho
            ctx.font = 'bold 24px Arial'; // Fonte maior para o título
            ctx.fillText('POSTO DE MOLAS SÃO BENTO', marginX, currentY);
            ctx.textAlign = 'right'; // Alinha o texto do orçamento à direita
            ctx.fillText('ORÇAMENTO', canvas.width - marginX, currentY);
            ctx.textAlign = 'left'; // Volta ao alinhamento padrão
            currentY += 30;

            ctx.font = 'bold 18px Arial';
            ctx.fillText('PEÇAS E SERVIÇOS', marginX, currentY);
            ctx.textAlign = 'right';
            ctx.fillText(`Nº ${document.getElementById('numeroOrcamento').value}`, canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 40;

            // Informações da Empresa
            ctx.font = '14px Arial'; // Fonte maior para info da empresa
            ctx.fillText('Suspensão de Caminhão e Caminhonete', marginX, currentY);
            currentY += 20;
            ctx.fillText('Alinhamento e Balanceamento - Suspensão a Ar', marginX, currentY);
            currentY += 20;
            ctx.fillText('42 99934-3158 | 42 99946-5858', marginX, currentY);
            ctx.textAlign = 'right';
            ctx.fillText('CNPJ 50.076.502/0001-74', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 20;
            ctx.fillText('postodemolassaobento@gmail.com - Av. Souza Naves, 4250 - CEP 84064-000 - Ponta Grossa / PR', marginX, currentY);
            currentY += 40;

            // Detalhes do Cliente e Veículo
            ctx.font = 'bold 16px Arial';
            ctx.fillText('DADOS DO CLIENTE E VEÍCULO', marginX, currentY);
            currentY += lineHeight;
            ctx.font = '14px Arial';
            ctx.fillText(`Nome: ${document.getElementById('nomeCliente').value}`, marginX, currentY);
            ctx.fillText(`Endereço: ${document.getElementById('enderecoCliente').value}`, marginX + 350, currentY); // Ajuste de posição
            currentY += lineHeight;
            ctx.fillText(`Cidade/UF: ${document.getElementById('cidadeCliente').value}/${document.getElementById('ufCliente').value}`, marginX, currentY);
            ctx.fillText(`E-mail: ${document.getElementById('emailCliente').value}`, marginX + 350, currentY); // Ajuste de posição
            currentY += lineHeight;
            ctx.fillText(`Telefone: ${document.getElementById('telCliente').value}`, marginX, currentY);
            currentY += lineHeight;
            ctx.fillText(`Veículo: ${document.getElementById('tipoVeiculo').value}`, marginX, currentY);
            ctx.fillText(`Cor: ${document.getElementById('corVeiculo').value}`, marginX + 350, currentY); // Ajuste de posição
            currentY += lineHeight;
            ctx.fillText(`Placa: ${document.getElementById('placaVeiculo').value}`, marginX, currentY);
            ctx.fillText(`Cidade Veículo: ${document.getElementById('cidadeVeiculo').value}`, marginX + 350, currentY); // Ajuste de posição
            currentY += 40;

            // Cabeçalho da Tabela para Itens
            ctx.font = 'bold 14px Arial'; // Fonte maior
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('UNID.', marginX + 90, currentY); // Ajuste de posição
            ctx.fillText('DESCRIÇÃO', marginX + 180, currentY); // Ajuste de posição
            ctx.textAlign = 'right';
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 180, currentY); // Ajuste de posição
            ctx.fillText('TOTAL', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 8;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += 20;

            ctx.font = '14px Arial';
            let totalPecas = 0;
            // Desenha as Peças
            initialPecas.forEach(item => {
                const itemTotal = item.quant * item.precoUnit;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                ctx.fillText(item.unid, marginX + 90, currentY);
                const linesUsed = wrapText(ctx, item.produto, marginX + 180, currentY, 400, lineHeight); // Largura maior para descrição
                ctx.textAlign = 'right';
                ctx.fillText(formatCurrency(item.precoUnit), canvas.width - marginX - 180, currentY);
                ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX, currentY);
                ctx.textAlign = 'left';
                totalPecas += itemTotal;
                currentY += (linesUsed * lineHeight); // Ajusta Y pela quantidade de linhas usadas
            });
            currentY += 20;

            // Cabeçalho da Tabela para Serviços
            ctx.font = 'bold 14px Arial';
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('DESCRIÇÃO', marginX + 180, currentY); // Ajuste de posição
            ctx.textAlign = 'right';
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 180, currentY); // Ajuste de posição
            ctx.fillText('TOTAL', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 8;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += 20;

            ctx.font = '14px Arial';
            let totalServicos = 0;
            // Desenha os Serviços
            initialServicos.forEach(item => {
                const itemTotal = item.quant * item.preco;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                const linesUsed = wrapText(ctx, item.produto, marginX + 180, currentY, 400, lineHeight); // Largura maior para descrição
                ctx.textAlign = 'right';
                ctx.fillText(formatCurrency(item.preco), canvas.width - marginX - 180, currentY);
                ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX, currentY);
                ctx.textAlign = 'left';
                totalServicos += itemTotal;
                currentY += (linesUsed * lineHeight); // Ajusta Y pela quantidade de linhas usadas
            });
            currentY += 30;

            // Totais
            ctx.font = 'bold 16px Arial'; // Fonte maior para totais
            ctx.textAlign = 'right';
            ctx.fillText('TOTAL DE PEÇAS:', canvas.width - marginX - 250, currentY); // Ajuste de posição
            ctx.fillText(formatCurrency(totalPecas), canvas.width - marginX, currentY);
            currentY += lineHeight + 5;

            ctx.fillText('TOTAL DE SERVIÇOS:', canvas.width - marginX - 250, currentY); // Ajuste de posição
            ctx.fillText(formatCurrency(totalServicos), canvas.width - marginX, currentY);
            currentY += lineHeight + 5;

            ctx.font = 'bold 18px Arial'; // Fonte ainda maior para total geral
            ctx.fillText('TOTAL GERAL:', canvas.width - marginX - 250, currentY); // Ajuste de posição
            ctx.fillText(formatCurrency(totalPecas + totalServicos), canvas.width - marginX, currentY);
            ctx.textAlign = 'left'; // Volta ao alinhamento padrão
            currentY += 50; // Mais espaço antes do rodapé

            // Rodapé
            currentY = canvas.height - 70; // Posição do rodapé mais abaixo
            ctx.font = '12px Arial'; // Fonte um pouco maior
            ctx.textAlign = 'center'; // Centraliza o rodapé
            ctx.fillText('Posto de Molas São Bento - Todos os direitos reservados.', canvas.width / 2, currentY);
            ctx.textAlign = 'left'; // Volta ao alinhamento padrão
        }

    </script>
</body>
</html>
