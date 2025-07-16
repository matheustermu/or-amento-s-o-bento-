<!DOCTYPE html>
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
                <input type="text" id="numeroOrcamento" placeholder="Ex: 2894">
                <button onclick="incrementOrcamento()">+</button>
            </div>

            <label for="dataOrcamento">Data:</label>
            <input type="date" id="dataOrcamento">

            <h3>Dados do Cliente</h3>
            <label for="nomeCliente">Nome:</label>
            <input type="text" id="nomeCliente" placeholder="Ex: João da Silva ou Empresa XYZ">

            <label for="enderecoCliente">Endereço:</label>
            <input type="text" id="enderecoCliente" placeholder="Ex: Rua Exemplo, 123 - Centro">

            <label for="cidadeCliente">Cidade:</label>
            <input type="text" id="cidadeCliente" placeholder="Ex: Curitiba">

            <label for="ufCliente">UF:</label>
            <input type="text" id="ufCliente" maxlength="2" placeholder="Ex: PR">

            <label for="emailCliente">E-mail:</label>
            <input type="email" id="emailCliente" placeholder="Ex: cliente@email.com">

            <label for="telCliente">Telefone:</label>
            <input type="text" id="telCliente" placeholder="Ex: (42) 99999-9999">

            <h3>Dados do Veículo</h3>
            <label for="tipoVeiculo">Caminhão / Caminhonete:</label>
            <input type="text" id="tipoVeiculo" placeholder="Ex: Scania P360 ou Ford Ranger">

            <label for="corVeiculo">Cor:</label>
            <input type="text" id="corVeiculo" placeholder="Ex: Branco ou Preto">

            <label for="placaVeiculo">Placa:</label>
            <input type="text" id="placaVeiculo" placeholder="Ex: XYZ9E87">

            <label for="cidadeVeiculo">Cidade Veículo:</label>
            <input type="text" id="cidadeVeiculo" placeholder="Ex: São Paulo">

            <h3>Peças</h3>
            <div class="add-item-fields">
                <input type="number" id="newPecaQuant" value="1" min="0.1" step="0.1" placeholder="Quant.">
                <input type="text" id="newPecaUnid" value="UNID." placeholder="Unid.">
                <input type="text" id="newPecaProduto" class="desc-input" placeholder="Descrição da Peça">
                <input type="number" id="newPecaPrecoUnit" value="0.00" min="0" step="0.01" placeholder="Preço Unit.">
            </div>
            <div id="pecasContainer" class="item-list-container">
            </div>
            <button onclick="addPeca()">Adicionar Peça</button>

            <h3>Serviços</h3>
            <div class="add-item-fields">
                <input type="number" id="newServicoQuant" value="1" min="0.1" step="0.1" placeholder="Quant.">
                <input type="text" id="newServicoProduto" class="desc-input" placeholder="Descrição do Serviço">
                <input type="number" id="newServicoPreco" value="0.00" min="0" step="0.01" placeholder="Preço Total">
            </div>
            <div id="servicosContainer" class="item-list-container">
            </div>
            <button onclick="addServico()">Adicionar Serviço</button>

            <button id="savePdfButton" onclick="saveCanvasAsPdf()">Salvar PDF</button>
        </div>

        <div class="canvas-section">
            <canvas id="orcamentoCanvas" width="800" height="1130"></canvas>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('orcamentoCanvas');
        const ctx = canvas.getContext('2d');
        const pecasContainer = document.getElementById('pecasContainer');
        const servicosContainer = document.getElementById('servicosContainer');

        const newPecaQuantInput = document.getElementById('newPecaQuant');
        const newPecaUnidInput = document.getElementById('newPecaUnid');
        const newPecaProdutoInput = document.getElementById('newPecaProduto');
        const newPecaPrecoUnitInput = document.getElementById('newPecaPrecoUnit');

        const newServicoQuantInput = document.getElementById('newServicoQuant');
        const newServicoProdutoInput = document.getElementById('newServicoProduto');
        const newServicoPrecoInput = document.getElementById('newServicoPreco');

        const initialPecas = [];
        const initialServicos = [];

        function formatCurrency(value) {
            return parseFloat(value).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        function renderPecas() {
            pecasContainer.innerHTML = '';
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
            drawCanvas();
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
            renderPecas();

            newPecaQuantInput.value = "1";
            newPecaUnidInput.value = "UNID.";
            newPecaProdutoInput.value = "";
            newPecaPrecoUnitInput.value = "0.00";
        }

        function removePeca(index) {
            initialPecas.splice(index, 1);
            renderPecas();
        }

        function renderServicos() {
            servicosContainer.innerHTML = '';
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
            drawCanvas();
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
            renderServicos();

            newServicoQuantInput.value = "1";
            newServicoProdutoInput.value = "";
            newServicoPrecoInput.value = "0.00";
        }

        function removeServico(index) {
            initialServicos.splice(index, 1);
            renderServicos();
        }

        function incrementOrcamento() {
            const numeroOrcamentoInput = document.getElementById('numeroOrcamento');
            let currentNumber = parseInt(numeroOrcamentoInput.value, 10);
            if (!isNaN(currentNumber)) {
                numeroOrcamentoInput.value = currentNumber + 1;
            } else {
                numeroOrcamentoInput.value = "1";
            }
            drawCanvas();
        }

        function saveCanvasAsPdf() {
            drawCanvas();
            window.print();
        }

        document.querySelectorAll('input, select').forEach(input => {
            input.addEventListener('input', drawCanvas);
        });

        document.addEventListener('DOMContentLoaded', () => {
            const today = new Date();
            const day = String(today.getDate()).padStart(2, '0');
            const month = String(today.getMonth() + 1).padStart(2, '0');
            const year = today.getFullYear();
            document.getElementById('dataOrcamento').value = `${year}-${month}-${day}`;

            renderPecas();
            renderServicos();
            drawCanvas();
        });

        function wrapText(context, text, x, y, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let lines = [];

            if (!text.trim()) {
                context.fillText('___________________', x, y); // Linha sublinhada para campo vazio
                return 1;
            }

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
            return lines.length;
        }

        function drawCanvas() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#fcf9e7';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#333';
            ctx.strokeStyle = '#555';
            ctx.lineWidth = 1.5;

            const baseFontSize = 18; // Tamanho de fonte base
            const baseLineHeight = 30; // Altura da linha base
            let currentY = 70; // Margem superior
            const marginX = 70; // Margem lateral
            const infoOffset = 380; // Offset para a segunda coluna de informações

            // --- Cabeçalho ---
            ctx.font = 'bold 38px Arial'; // Tamanho do título aumentado para 38px
            ctx.fillText('POSTO DE MOLAS SÃO BENTO', marginX, currentY);
            ctx.textAlign = 'right';
            ctx.font = 'bold 32px Arial';
            ctx.fillText('ORÇAMENTO', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 45;

            ctx.font = 'bold 24px Arial';
            ctx.fillText('PEÇAS E SERVIÇOS', marginX, currentY);
            ctx.textAlign = 'right';
            const numeroOrcamento = document.getElementById('numeroOrcamento').value || 'Não Informado';
            ctx.fillText(`Nº ${numeroOrcamento}`, canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 55;

            // --- Informações da Empresa ---
            ctx.font = `${baseFontSize}px Arial`;
            ctx.fillText('Suspensão de Caminhão e Caminhonete', marginX, currentY);
            currentY += baseLineHeight - 5;
            ctx.fillText('Alinhamento e Balanceamento - Suspensão a Ar', marginX, currentY);
            currentY += baseLineHeight - 5;
            ctx.fillText('42 99934-3158 | 42 99946-5858', marginX, currentY);
            ctx.textAlign = 'right';
            ctx.fillText('CNPJ 50.076.502/0001-74', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += baseLineHeight - 5;
            ctx.fillText('postodemolassaobento@gmail.com - Av. Souza Naves, 4250 - CEP 84064-000 - Ponta Grossa / PR', marginX, currentY);
            currentY += 70; // Mais espaço

            // --- Detalhes do Cliente e Veículo ---
            ctx.font = `bold ${baseFontSize + 4}px Arial`;
            ctx.fillText('DADOS DO CLIENTE E VEÍCULO', marginX, currentY);
            currentY += baseLineHeight + 10;
            ctx.font = `${baseFontSize}px Arial`;

            const nomeCliente = document.getElementById('nomeCliente').value || 'Não Informado';
            const enderecoCliente = document.getElementById('enderecoCliente').value || 'Não Informado';
            const cidadeCliente = document.getElementById('cidadeCliente').value || 'Não Informado';
            const ufCliente = document.getElementById('ufCliente').value || 'Não Informado';
            const emailCliente = document.getElementById('emailCliente').value || 'Não Informado';
            const telCliente = document.getElementById('telCliente').value || 'Não Informado';

            const tipoVeiculo = document.getElementById('tipoVeiculo').value || 'Não Informado';
            const corVeiculo = document.getElementById('corVeiculo').value || 'Não Informado';
            const placaVeiculo = document.getElementById('placaVeiculo').value || 'Não Informado';
            const cidadeVeiculo = document.getElementById('cidadeVeiculo').value || 'Não Informado';
            const dataOrcamento = document.getElementById('dataOrcamento').value;
            const formattedDate = dataOrcamento ? new Date(dataOrcamento + 'T12:00:00').toLocaleDateString('pt-BR', {day: '2-digit', month: '2-digit', year: 'numeric'}) : 'Não Informado';

            ctx.fillText(`Data: ${formattedDate}`, marginX, currentY);
            ctx.fillText(`Nome: ${nomeCliente}`, marginX + infoOffset, currentY);
            currentY += baseLineHeight;

            ctx.fillText(`Endereço: ${enderecoCliente}`, marginX, currentY);
            ctx.fillText(`Cidade/UF: ${cidadeCliente}/${ufCliente}`, marginX + infoOffset, currentY);
            currentY += baseLineHeight;

            ctx.fillText(`E-mail: ${emailCliente}`, marginX, currentY);
            ctx.fillText(`Telefone: ${telCliente}`, marginX + infoOffset, currentY);
            currentY += baseLineHeight;

            ctx.fillText(`Veículo: ${tipoVeiculo}`, marginX, currentY);
            ctx.fillText(`Cor: ${corVeiculo}`, marginX + infoOffset, currentY);
            currentY += baseLineHeight;

            ctx.fillText(`Placa: ${placaVeiculo}`, marginX, currentY);
            ctx.fillText(`Cidade Veículo: ${cidadeVeiculo}`, marginX + infoOffset, currentY);
            currentY += 80; // Mais espaço

            // --- Título da Seção de Peças ---
            ctx.font = `bold ${baseFontSize + 4}px Arial`;
            ctx.fillText('PEÇAS:', marginX, currentY);
            currentY += baseLineHeight + 5;

            // --- Cabeçalho da Tabela para Peças ---<p style="text-align: center;">Peças</p>
            ctx.font = `bold ${baseFontSize + 2}px Arial`;
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('UNID.', marginX + 100, currentY);
            ctx.fillText('DESCRIÇÃO', marginX + 200, currentY);
            ctx.textAlign = 'right';
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 200, currentY);
            ctx.fillText('TOTAL', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 10;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += baseLineHeight;

            ctx.font = `${baseFontSize}px Arial`;
            let totalPecas = 0;
            let pecasLinesCount = 0;
            const maxPecasLines = 6;

            if (initialPecas.length > 0) {
                initialPecas.forEach(item => {
                    if (pecasLinesCount < maxPecasLines) {
                        const itemTotal = item.quant * item.precoUnit;
                        ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                        ctx.fillText(item.unid, marginX + 100, currentY);
                        const linesUsed = wrapText(ctx, item.produto, marginX + 200, currentY, 280, baseLineHeight - 8);
                        ctx.textAlign = 'right';
                        ctx.fillText(formatCurrency(item.precoUnit), canvas.width - marginX - 200, currentY);
                        ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX, currentY);
                        ctx.textAlign = 'left';
                        totalPecas += itemTotal;
                        currentY += (linesUsed * (baseLineHeight - 8));
                        pecasLinesCount += linesUsed;
                    }
                });
            }

            for (let i = pecasLinesCount; i < maxPecasLines; i++) {
                ctx.fillText('0.00', marginX, currentY);
                ctx.fillText('_______', marginX + 100, currentY);
                wrapText(ctx, '', marginX + 200, currentY, 280, baseLineHeight - 8);
                ctx.textAlign = 'right';
                ctx.fillText('R$ 0,00', canvas.width - marginX - 200, currentY);
                ctx.fillText('R$ 0,00', canvas.width - marginX, currentY);
                ctx.textAlign = 'left';
                currentY += baseLineHeight - 8;
            }
            currentY += 50;

            // --- Título da Seção de Serviços ---
            ctx.font = `bold ${baseFontSize + 4}px Arial`;
            ctx.fillText('SERVIÇOS:', marginX, currentY);
            currentY += baseLineHeight + 5;

            // --- Cabeçalho da Tabela para Serviços ---<p style="text-align: center;">Serviços</p>
            ctx.font = `bold ${baseFontSize + 2}px Arial`;
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('DESCRIÇÃO', marginX + 200, currentY);
            ctx.textAlign = 'right';
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 200, currentY);
            ctx.fillText('TOTAL', canvas.width - marginX, currentY);
            ctx.textAlign = 'left';
            currentY += 10;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += baseLineHeight;

            ctx.font = `${baseFontSize}px Arial`;
            let totalServicos = 0;
            let servicosLinesCount = 0;
            const maxServicosLines = 6;

            if (initialServicos.length > 0) {
                initialServicos.forEach(item => {
                    if (servicosLinesCount < maxServicosLines) {
                        const itemTotal = item.quant * item.preco;
                        ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                        const linesUsed = wrapText(ctx, item.produto, marginX + 200, currentY, 280, baseLineHeight - 8);
                        ctx.textAlign = 'right';
                        ctx.fillText(formatCurrency(item.preco), canvas.width - marginX - 200, currentY);
                        ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX, currentY);
                        ctx.textAlign = 'left';
                        totalServicos += itemTotal;
                        currentY += (linesUsed * (baseLineHeight - 8));
                        servicosLinesCount += linesUsed;
                    }
                });
            }

            for (let i = servicosLinesCount; i < maxServicosLines; i++) {
                ctx.fillText('0.00', marginX, currentY);
                wrapText(ctx, '', marginX + 200, currentY, 280, baseLineHeight - 8);
                ctx.textAlign = 'right';
                ctx.fillText('R$ 0,00', canvas.width - marginX - 200, currentY);
                ctx.fillText('R$ 0,00', canvas.width - marginX, currentY);
                ctx.textAlign = 'left';
                currentY += baseLineHeight - 8;
            }
            currentY += 60;

            // --- Totais ---
            ctx.font = `bold ${baseFontSize + 6}px Arial`;
            ctx.textAlign = 'right';
            ctx.fillText('TOTAL DE PEÇAS:', canvas.width - marginX - 250, currentY);
            ctx.fillText(formatCurrency(totalPecas), canvas.width - marginX, currentY);
            currentY += baseLineHeight + 15;

            ctx.fillText('TOTAL DE SERVIÇOS:', canvas.width - marginX - 250, currentY);
            ctx.fillText(formatCurrency(totalServicos), canvas.width - marginX, currentY);
            currentY += baseLineHeight + 15;

            ctx.font = 'bold 30px Arial';
            ctx.fillText('TOTAL GERAL:', canvas.width - marginX - 250, currentY);
            ctx.fillText(formatCurrency(totalPecas + totalServicos), canvas.width - marginX, currentY);

            ctx.textAlign = 'left';
            // Ajusta a posição Y do rodapé para ficar a 70px da parte inferior do canvas
            currentY = canvas.height - 70;

            // --- Rodapé ---
            ctx.font = '18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('Posto de Molas São Bento - Todos os direitos reservados.', canvas.width / 2, currentY);
            ctx.textAlign = 'left';
        }
    </script>
</body>
</html>
