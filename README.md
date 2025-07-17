
<html lang="pt-BR">

<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Protegida</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f0f2f5;
            color: #333;
            text-align: center;
            flex-direction: column;
        }
        .content {
            background-color: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 90%;
            display: none; /* Esconde o conteúdo por padrão */
        }
        h1 {
            color: #007bff;
            margin-bottom: 20px;
        }
        p {
            font-size: 1.1em;
            line-height: 1.6;
        }
        .footer {
            margin-top: 30px;
            font-size: 0.85em;
            color: #666;
        }
    </style>
</head>
<body>

   
       
    </div>

    <script>
        const CORRECT_PASSWORD = "102030";
        let passwordEntered = false;

        // Loop para pedir a senha até que seja correta
        while (!passwordEntered) {
            const userInput = prompt("Por favor, digite a senha para acessar esta página:");

            if (userInput === CORRECT_PASSWORD) {
                passwordEntered = true;
                alert("Senha correta! Bem-vindo.");
                document.getElementById('protectedContent').style.display = 'block'; // Mostra o conteúdo
            } else {
                alert("Senha incorreta. Tente novamente.");
            }
        }
    </script>

</body>
</html>
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

        .form-section, .canvas-preview {
            flex: 1;
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px var(--shadow-medium);
            transition: transform 0.3s ease-in-out;
        }

        .form-section:hover, .canvas-preview:hover {
            transform: translateY(-5px);
        }

        .canvas-container {
            border: 1px solid var(--border-color);
            background-color: #fcf9e7; /* Cor semelhante ao papel */
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: inset 0 0 5px rgba(0,0,0,0.05);
            margin-bottom: 20px; /* Espaçamento entre as páginas na visualização */
        }

        canvas {
            display: block; /* Remove espaçamento extra abaixo do canvas */
            width: 100%; /* Ajusta para preencher o container */
            height: auto;
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

        input:where([type="text"], [type="number"], [type="email"], [type="date"]),
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

        input:where([type="text"], [type="number"], [type="email"], [type="date"]):focus,
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
        .add-item-fields input:where([type="number"]) {
            width: 90px;
            flex: none;
        }
        .add-item-fields input:where([type="text"]).desc-input {
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
            .form-section, .canvas-preview {
                flex: none;
                width: 100%;
            }
            .canvas-preview {
                padding: 15px; /* Reduz padding para canvas em telas menores */
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 1.8em;
                margin-top: 20px;
                margin-bottom: 20px;
            }
            .form-section, .canvas-preview {
                padding: 20px;
            }
            input:where([type="text"], [type="number"], [type="email"], [type="date"]), select, button {
                font-size: 0.95em;
                padding: 10px;
            }
            .add-item-fields {
                flex-direction: column; /* Pilha os inputs em telas menores */
                gap: 8px; /* Ajusta o espaçamento */
            }
            .add-item-fields input {
                width: 100%; /* Força a largura total */
                min-width: unset; /* Remove min-width para melhor flexibilidade */
            }
            .add-item-fields input:where([type="number"]) {
                width: 100%; /* Ocupa a largura total */
            }
            .add-item-fields input:where([type="text"]).desc-input {
                width: 100%; /* Ocupa a largura total */
            }
        }

        /* --- Estilos para Impressão (PDF) - Otimizados para múltiplas páginas --- */
        @media print {
            @page {
                size: A4 portrait;
                margin: 0;
            }

            body {
                background-color: white !important;
                margin: 0;
                padding: 0;
                display: block;
                overflow: hidden;
            }
            h1, .form-section, .add-item-fields, button, .item-list-container, .orcamento-numero-group {
                display: none !important; /* Oculta todo o formulário e botões */
            }
            .container {
                display: block;
                width: 100%;
                max-width: none;
                margin: 0;
                padding: 0;
            }
            .canvas-preview {
                box-shadow: none !important;
                padding: 0 !important;
                margin: 0 !important;
                background-color: white !important;
                display: block;
                width: 100%;
                height: auto; /* Deixa a altura ser definida pelo conteúdo */
            }
            .canvas-container {
                border: none !important;
                box-shadow: none !important;
                background-color: white !important;
                margin-bottom: 0 !important; /* Remove margem entre canvases impressos */
                page-break-after: always; /* Garante que cada canvas começa em uma nova página */
                position: relative; /* Necessário para o page-break-after funcionar corretamente em alguns casos */
                height: 100vh; /* Tenta forçar a altura da viewport de impressão */
                overflow: hidden; /* Garante que nada transborde */
            }
            .canvas-container:last-child {
                page-break-after: avoid; /* Não quebra depois da última página */
            }
            canvas {
                border: none !important;
                box-shadow: none !important;
                background-color: #fcf9e7 !important; /* Mantém a cor de fundo do "papel" */
                display: block;
                width: 100vw !important; /* Tenta usar a largura total da viewport de impressão */
                height: 100vh !important; /* Tenta usar a altura total da viewport de impressão */
                object-fit: contain; /* Redimensiona o canvas para caber na página sem cortar */
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

            <label for="cpfCnpjCliente">CPF/CNPJ:</label>
            <input type="text" id="cpfCnpjCliente" placeholder="Ex: 123.456.789-00 ou 12.345.678/0001-90">

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

            <label for="QUEM FEZ">QUEM FEZ:</label>
            <input type="text" id="QUEM FEZ" placeholder="Ex: AURI E EZEQUIEL ">

            
            <h3>Peças</h3>
            <div class="add-item-fields">
                <input type="number" id="newPecaQuant" value="1" min="0.1" step="0.1" placeholder="Quant. (Ex: 1)">
                <input type="text" id="newPecaUnid" value="UNID." placeholder="Unid. (Ex: UNID., MT, KG)">
                <input type="text" id="newPecaProduto" class="desc-input" placeholder="Descrição da Peça (Ex: Mola Parabólica)">
                <input type="number" id="newPecaPrecoUnit" value="0.00" min="0" step="0.01" placeholder="Preço Unit. (Ex: 150.00)">
            </div>
            <div id="pecasContainer" class="item-list-container">
            </div>
            <button onclick="addPeca()">Adicionar Peça</button>

            <h3>Serviços</h3>
            <div class="add-item-fields">
                <input type="number" id="newServicoQuant" value="1" min="0.1" step="0.1" placeholder="Quant. (Ex: 1)">
                <input type="text" id="newServicoProduto" class="desc-input" placeholder="Descrição do Serviço (Ex: Troca de Amortecedores)">
                <input type="number" id="newServicoPreco" value="0.00" min="0" step="0.01" placeholder="Preço Total (Ex: 300.00)">
            </div>
            <div id="servicosContainer" class="item-list-container">
            </div>
            <button onclick="addServico()">Adicionar Serviço</button>

            <h3>Desconto</h3>
            <label for="descontoValor">Valor do Desconto:</label>
            <input type="number" id="descontoValor" value="0.00" min="0" step="0.01" placeholder="Ex: 50.00">

            <button id="savePdfButton" onclick="saveCanvasAsPdf()">Salvar/Imprimir PDF</button>
        </div>

        <div class="canvas-preview" id="canvasPreviewContainer">
            </div>
    </div>

    <script>
        const canvasPreviewContainer = document.getElementById('canvasPreviewContainer');
        const pecasContainer = document.getElementById('pecasContainer');
        const servicosContainer = document.getElementById('servicosContainer');

        // Referências para os campos de entrada de peças
        const newPecaQuantInput = document.getElementById('newPecaQuant');
        const newPecaUnidInput = document.getElementById('newPecaUnid');
        const newPecaProdutoInput = document.getElementById('newPecaProduto');
        const newPecaPrecoUnitInput = document.getElementById('newPecaPrecoUnit');

        // Referências para os campos de entrada de serviços
        const newServicoQuantInput = document.getElementById('newServicoQuant');
        const newServicoProdutoInput = document.getElementById('newServicoProduto');
        const newServicoPrecoInput = document.getElementById('newServicoPreco');

        // Referência para o campo de desconto
        const descontoValorInput = document.getElementById('descontoValor');


        // Arrays para armazenar as peças e serviços
        const initialPecas = [];
        const initialServicos = [];

        // Dimensões do canvas para A4 (aproximadamente 210mm x 297mm a 300dpi)
        const CANVAS_WIDTH = 1000;
        const CANVAS_HEIGHT = 1400; // Altura de uma página A4 em pixels (aprox. 300dpi)

        // Margens internas do conteúdo
        const MARGIN_X = 60; // REDUZIDO
        const MARGIN_TOP_INITIAL = 60; // REDUZIDO
        const MARGIN_BOTTOM_PAGE = 60; // REDUZIDO
        const MAX_CONTENT_HEIGHT_PER_PAGE = CANVAS_HEIGHT - MARGIN_TOP_INITIAL - MARGIN_BOTTOM_PAGE;

        // Altura de texto e espaçamento base
        const BASE_FONT_SIZE = 18; // REDUZIDO
        const BASE_LINE_HEIGHT = 28; // REDUZIDO
        const SMALL_LINE_HEIGHT = BASE_LINE_HEIGHT - 3; // REDUZIDO para itens de lista


        let currentPageCtx = null; // Contexto do canvas da página atual
        let currentPageY = MARGIN_TOP_INITIAL; // Posição Y atual no canvas da página atual

        // Armazena todos os canvases criados
        let canvases = [];

        function formatCurrency(value) {
            return parseFloat(value).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        // Função para iniciar uma nova página no canvas
        function startNewPage() {
            const canvasDiv = document.createElement('div');
            canvasDiv.className = 'canvas-container';
            const newCanvas = document.createElement('canvas');
            newCanvas.width = CANVAS_WIDTH;
            newCanvas.height = CANVAS_HEIGHT;
            canvasDiv.appendChild(newCanvas);
            canvasPreviewContainer.appendChild(canvasDiv);

            currentPageCtx = newCanvas.getContext('2d');
            currentPageCtx.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
            currentPageCtx.fillStyle = '#fcf9e7';
            currentPageCtx.fillRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
            currentPageCtx.fillStyle = '#333';
            currentPageCtx.strokeStyle = '#555';
            currentPageCtx.lineWidth = 1;

            canvases.push(newCanvas);
            currentPageY = MARGIN_TOP_INITIAL; // Reinicia Y para o topo da nova página
        }

        // Função para quebrar texto em várias linhas e desenhá-lo
        function drawWrappedText(ctx, text, x, y, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let currentYForLines = y;
            let linesDrawn = 0;

            for (let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = ctx.measureText(testLine);
                let testWidth = metrics.width;

                if (testWidth > maxWidth && n > 0) {
                    ctx.fillText(line.trim(), x, currentYForLines);
                    currentYForLines += lineHeight;
                    linesDrawn++;
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            if (line.trim() !== '') {
                ctx.fillText(line.trim(), x, currentYForLines);
                currentYForLines += lineHeight;
                linesDrawn++;
            }
            return linesDrawn * lineHeight; // Retorna a altura total ocupada
        }

        // Função para calcular a altura que um texto ocuparia
        function measureWrappedTextHeight(ctx, text, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let lines = 0;
            if (text.trim() === '') return 0; // Handle empty text

            for (let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = ctx.measureText(testLine);
                let testWidth = metrics.width;
                if (testWidth > maxWidth && n > 0) {
                    lines++;
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            lines++; // For the last line
            return lines * lineHeight;
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
            drawAllCanvases();
        }

        function addPeca() {
            const quant = parseFloat(newPecaQuantInput.value);
            const unid = newPecaUnidInput.value.trim();
            const produto = newPecaProdutoInput.value.trim();
            const precoUnit = parseFloat(newPecaPrecoUnitInput.value);

            // CORREÇÃO: Preço Unitário deve ser >= 0
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
            drawAllCanvases();
        }

        function addServico() {
            const quant = parseFloat(newServicoQuantInput.value);
            const produto = newServicoProdutoInput.value.trim();
            const preco = parseFloat(newServicoPrecoInput.value);

            // CORREÇÃO: Preço Total deve ser >= 0
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
            drawAllCanvases();
        }

        function saveCanvasAsPdf() {
            drawAllCanvases();
            window.print();
        }

        document.querySelectorAll('#numeroOrcamento, #dataOrcamento, #nomeCliente, #cpfCnpjCliente, #enderecoCliente, #cidadeCliente, #ufCliente, #emailCliente, #telCliente, #tipoVeiculo, #corVeiculo, #placaVeiculo, #cidadeVeiculo, #descontoValor # QUEM FEZ').forEach(input => {
            input.addEventListener('input', drawAllCanvases);
        });

        document.addEventListener('DOMContentLoaded', () => {
            const today = new Date();
            const day = String(today.getDate()).padStart(2, '0');
            const month = String(today.getMonth() + 1).padStart(2, '0');
            const year = today.getFullYear();
            document.getElementById('dataOrcamento').value = `${year}-${month}-${day}`;

            renderPecas();
            renderServicos();
            drawAllCanvases();
        });

        // Função principal para desenhar todas as páginas
        function drawAllCanvases() {
            canvasPreviewContainer.innerHTML = ''; // Limpa canvases anteriores
            canvases = []; // Limpa a lista de canvases

            startNewPage(); // Inicia a primeira página

            // --- Cabeçalho da Empresa ---
            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 10}px Arial`; // REDUZIDO
            currentPageCtx.fillText('POSTO DE MOLAS SÃO BENTO', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('ORÇAMENTIIIIIO', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 6}px Arial`; // REDUZIDO
            currentPageCtx.fillText('PEÇAS E SERVIÇOS', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            const numeroOrcamento = document.getElementById('numeroOrcamento').value.trim();
            currentPageCtx.fillText(`Nº ${numeroOrcamento === '' ? 'Não informado' : numeroOrcamento}`, CANVAS_WIDTH - MARGIN_X, currentPageY); // CORREÇÃO: "Não informado"
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            currentPageCtx.fillText('Suspensão de Caminhão e Caminhonete', MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('Alinhamento e Balanceamento - Suspensão a Ar', MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('42 99934-3158 | 42 99946-5858', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('CNPJ 50.076.502/0001-74', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('postodemolassaobento@gmail.com - Av. Souza Naves, 4250 - CEP 84064-000 - Ponta Grossa / PR', MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO

            // --- Dados do Cliente e Veículo ---
            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 2}px Arial`; // REDUZIDO
            let clientVehicleSectionHeight = (BASE_LINE_HEIGHT + 10) + (SMALL_LINE_HEIGHT * 5) + (BASE_LINE_HEIGHT + 20); // Título + 5 linhas de dados + espaçamento final

            if (currentPageY + clientVehicleSectionHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.fillText('DADOS DO CLIENTE E VEÍCULO', MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO
            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO

            const nomeCliente = document.getElementById('nomeCliente').value.trim();
            const cpfCnpjCliente = document.getElementById('cpfCnpjCliente').value.trim();
            const enderecoCliente = document.getElementById('enderecoCliente').value.trim();
            const cidadeCliente = document.getElementById('cidadeCliente').value.trim();
            const ufCliente = document.getElementById('ufCliente').value.trim();
            const emailCliente = document.getElementById('emailCliente').value.trim();
            const telCliente = document.getElementById('telCliente').value.trim();
            const tipoVeiculo = document.getElementById('tipoVeiculo').value.trim();
            const corVeiculo = document.getElementById('corVeiculo').value.trim();
            const placaVeiculo = document.getElementById('placaVeiculo').value.trim();
            const cidadeVeiculo = document.getElementById('cidadeVeiculo').value.trim();

            // CORREÇÃO: "Não informado" para campos vazios
            currentPageCtx.fillText(`Nome: ${nomeCliente === '' ? 'Não informado' : nomeCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`CPF/CNPJ: ${cpfCnpjCliente === '' ? 'Não informado' : cpfCnpjCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Endereço: ${enderecoCliente === '' ? 'Não informado' : enderecoCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cidade/UF: ${cidadeCliente === '' ? 'Não informado' : cidadeCliente}/${ufCliente === '' ? 'Não informado' : ufCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`E-mail: ${emailCliente === '' ? 'Não informado' : emailCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Telefone: ${telCliente === '' ? 'Não informado' : telCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Veículo: ${tipoVeiculo === '' ? 'Não informado' : tipoVeiculo}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cor: ${corVeiculo === '' ? 'Não informado' : corVeiculo}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Placa: ${placaVeiculo === '' ? 'Não informado' : placaVeiculo}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cidade Veículo: ${cidadeVeiculo === '' ? 'Não informado' : cidadeVeiculo}`, MARGIN_X + 400, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO

            // --- Seção de Peças ---
            let pecasSectionTitleHeight = BASE_LINE_HEIGHT + 6 + 10;
            let pecasTableHeaderHeight = (BASE_FONT_SIZE + 2 + 10) + (SMALL_LINE_HEIGHT + 5);

            if (currentPageY + pecasSectionTitleHeight + pecasTableHeaderHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('PEÇAS', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
            currentPageCtx.fillText('UNID.', MARGIN_X + 100, currentPageY); // Ajustado X
            currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY); // Ajustado X
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY); // Ajustado X
            currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += 8; // REDUZIDO
            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X, currentPageY);
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.stroke();
            currentPageY += SMALL_LINE_HEIGHT + 5; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            initialPecas.forEach(item => {
                const itemTotal = item.quant * item.precoUnit;

                const requiredHeight = measureWrappedTextHeight(currentPageCtx, item.produto, 350, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH

                if (currentPageY + requiredHeight + (SMALL_LINE_HEIGHT * 1) > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                    startNewPage();
                    // Redesenha cabeçalho de peças na nova página
                    currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`;
                    currentPageCtx.textAlign = 'center';
                    currentPageCtx.fillText('PEÇAS (continuação)', CANVAS_WIDTH / 2, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += BASE_LINE_HEIGHT + 10;

                    currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`;
                    currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
                    currentPageCtx.fillText('UNID.', MARGIN_X + 100, currentPageY);
                    currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY);
                    currentPageCtx.textAlign = 'right';
                    currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                    currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += 8;
                    currentPageCtx.beginPath();
                    currentPageCtx.moveTo(MARGIN_X, currentPageY);
                    currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.stroke();
                    currentPageY += SMALL_LINE_HEIGHT + 5;
                    currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`;
                }

                currentPageCtx.fillText(item.quant.toFixed(2), MARGIN_X, currentPageY);
                currentPageCtx.fillText(item.unid, MARGIN_X + 100, currentPageY);
                const actualHeightUsed = drawWrappedText(currentPageCtx, item.produto, MARGIN_X + 180, currentPageY, 350, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH
                currentPageCtx.textAlign = 'right';
                currentPageCtx.fillText(formatCurrency(item.precoUnit), CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                currentPageCtx.fillText(formatCurrency(itemTotal), CANVAS_WIDTH - MARGIN_X, currentPageY);
                currentPageCtx.textAlign = 'left';
                currentPageY += actualHeightUsed;
            });
            currentPageY += 30; // REDUZIDO

            // --- Seção de Serviços ---
            let servicosSectionTitleHeight = BASE_LINE_HEIGHT + 6 + 10;
            let servicosTableHeaderHeight = (BASE_FONT_SIZE + 2 + 10) + (SMALL_LINE_HEIGHT + 5);

            if (currentPageY + servicosSectionTitleHeight + servicosTableHeaderHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('SERVIÇOS', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
            currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY); // Ajustado X
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY); // Ajustado X
            currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += 8; // REDUZIDO
            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X, currentPageY);
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.stroke();
            currentPageY += SMALL_LINE_HEIGHT + 5; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            initialServicos.forEach(item => {
                const itemTotal = item.quant * item.preco;
                const requiredHeight = measureWrappedTextHeight(currentPageCtx, item.produto, 450, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH

                if (currentPageY + requiredHeight + (SMALL_LINE_HEIGHT * 1) > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                    startNewPage();
                    // Redesenha cabeçalho de serviços na nova página
                    currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`;
                    currentPageCtx.textAlign = 'center';
                    currentPageCtx.fillText('SERVIÇOS (continuação)', CANVAS_WIDTH / 2, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += BASE_LINE_HEIGHT + 10;

                    currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`;
                    currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
                    currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY);
                    currentPageCtx.textAlign = 'right';
                    currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                    currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += 8;
                    currentPageCtx.beginPath();
                    currentPageCtx.moveTo(MARGIN_X, currentPageY);
                    currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.stroke();
                    currentPageY += SMALL_LINE_HEIGHT + 5;
                    currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`;
                }

                currentPageCtx.fillText(item.quant.toFixed(2), MARGIN_X, currentPageY);
                const actualHeightUsed = drawWrappedText(currentPageCtx, item.produto, MARGIN_X + 180, currentPageY, 450, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH
                currentPageCtx.textAlign = 'right';
                currentPageCtx.fillText(formatCurrency(item.preco), CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                currentPageCtx.fillText(formatCurrency(itemTotal), CANVAS_WIDTH - MARGIN_X, currentPageY);
                currentPageCtx.textAlign = 'left';
                currentPageY += actualHeightUsed;
            });
            currentPageY += 40; // REDUZIDO

            // --- Totais e Rodapé ---
            let totalsFooterHeight = (SMALL_LINE_HEIGHT + 8) * 3 + (BASE_FONT_SIZE + 8 + 15) + (SMALL_LINE_HEIGHT + 8) + 80 + 25 + BASE_FONT_SIZE; // Ajustado os cálculos de altura para os novos tamanhos de fonte e linha

            if (currentPageY + totalsFooterHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            const totalPecas = initialPecas.reduce((sum, item) => sum + (item.quant * item.precoUnit), 0);
            const totalServicos = initialServicos.reduce((sum, item) => sum + (item.quant * item.preco), 0);
            const desconto = parseFloat(document.getElementById('descontoValor').value) || 0;
            const totalGeral = totalPecas + totalServicos - desconto;

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('TOTAL DE PEÇAS:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalPecas), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.fillText('TOTAL DE SERVIÇOS:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalServicos), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.fillText('DESCONTO:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(desconto), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 8}px Arial`; // REDUZIDO
            currentPageCtx.fillText('TOTAL GERAL:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalGeral), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 30; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'left';
            const dataOrcamento = document.getElementById('dataOrcamento').value;
            const dataFormatada = dataOrcamento ? new Date(dataOrcamento).toLocaleDateString('pt-BR', { day: 'numeric', month: 'long', year: 'numeric' }) : 'Não informado'; // CORREÇÃO: "Não informado"
            currentPageCtx.fillText(`Ponta Grossa, ${dataFormatada}`, MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 60; // REDUZIDO

            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X + 150, currentPageY); // Ajustado X
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X - 150, currentPageY); // Ajustado X
            currentPageCtx.stroke();
            currentPageY += 20; // REDUZIDO
            currentPageCtx.font = `${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('Assinatura do Responsável', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
        }
    </script>
</body>
</html>
