<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gerador de Orçamento - Posto de Molas São Bento</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 0; /* Remove default padding */
            margin: 0; /* Remove default margin */
            background-color: #f4f4f4;
            min-height: 100vh; /* Make body at least viewport height */
            width: 100vw; /* Make body viewport width */
            overflow-x: hidden; /* Prevent horizontal scroll */
        }
        h1 {
            margin-top: 20px; /* Add some margin to the top of the title */
            margin-bottom: 20px;
        }
        .container {
            display: flex;
            gap: 20px;
            width: 95%; /* Adjust to be almost full width */
            max-width: 1400px; /* Increase max-width for larger screens if desired */
            margin-bottom: 20px;
            flex-grow: 1; /* Allow container to grow and take available space */
        }
        .form-section {
            flex: 1;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            overflow-y: auto; /* Add scroll if content is too long */
        }
        .canvas-section {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        canvas {
            border: 1px solid #ccc;
            background-color: #fcf9e7; /* Cor semelhante ao papel */
            max-width: 100%; /* Ensure canvas scales down on smaller screens */
            height: auto; /* Maintain aspect ratio */
        }
        h2 {
            color: #333;
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #555;
        }
        input[type="text"],
        input[type="number"],
        input[type="email"],
        select {
            width: calc(100% - 12px);
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        /* --- NOVOS ESTILOS PARA CAMPOS DE ADIÇÃO DE ITENS --- */
        .add-item-fields {
            display: flex;
            flex-wrap: wrap; /* Permite que os itens quebrem a linha se não houver espaço */
            gap: 10px; /* Espaço entre os campos */
            margin-bottom: 15px;
            padding: 10px;
            border: 1px dashed #ccc; /* Borda tracejada para separar os campos de adição */
            border-radius: 4px;
            background-color: #f0f0f0;
        }
        .add-item-fields input {
            flex: 1; /* Faz os inputs ocuparem o espaço disponível */
            min-width: 80px; /* Largura mínima para inputs menores */
            margin-bottom: 0; /* Remove a margem inferior padrão dos inputs */
        }
        .add-item-fields input[type="number"] {
            width: 80px; /* Largura específica para quantidade e preço unitário */
            flex: none; /* Não permite que eles se estiquem */
        }
        .add-item-fields input[type="text"].desc-input {
            flex: 3; /* Faz o campo de descrição ser mais largo */
        }
        /* --- ESTILOS EXISTENTES PARA A LISTA DE ITENS --- */
        .item-list-container {
            margin-top: 10px;
            margin-bottom: 10px;
            border-radius: 4px;
            padding: 10px 0;
        }
        .item-display-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 8px;
            margin-bottom: 5px;
            background-color: #f9f9f9;
            border-radius: 4px;
        }
        .item-display-row:last-child {
            margin-bottom: 0;
        }
        .item-display-row span {
            font-weight: bold;
            color: #333;
            flex-grow: 1;
            text-align: right;
            padding-right: 10px;
        }
        .item-display-row .remove-button {
            background-color: #dc3545;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            min-width: 40px;
            text-align: center;
        }
        .item-display-row .remove-button:hover {
            background-color: #c82333;
        }
        /* --- FIM DOS ESTILOS --- */

        button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
            width: 100%;
        }
        button:hover {
            background-color: #218838;
        }
        .totals-section div {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .orcamento-numero-group {
            display: flex;
            align-items: center;
            margin-bottom: 10px; /* Adjust as needed */
        }
        .orcamento-numero-group input {
            margin-bottom: 0; /* Remove default margin */
            flex-grow: 1;
        }
        .orcamento-numero-group button {
            width: auto; /* Allow button to size naturally */
            padding: 8px 12px; /* Adjust padding */
            margin-left: 5px; /* Space between input and button */
            margin-top: 0; /* Remove default margin-top */
            background-color: #007bff; /* Blue for increment button */
        }
        .orcamento-numero-group button:hover {
            background-color: #0056b3;
        }
        /* Estilo para o botão de Salvar PDF */
        #savePdfButton {
            background-color: #17a2b8; /* Cor azul-ciano */
        }
        #savePdfButton:hover {
            background-color: #138496;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
                width: 95%;
            }
            .form-section, .canvas-section {
                flex: none; /* Remove flex-grow on small screens */
                width: 100%; /* Make them full width */
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
                <input type="text" id="numeroOrcamento" value="2894">
                <button onclick="incrementOrcamento()">+</button>
            </div>


            <label for="dataOrcamento">Data:</label>
            <input type="date" id="dataOrcamento" value="2025-07-16">

            <h3>Dados do Cliente</h3>
            <label for="nomeCliente">Nome:</label>
            <input type="text" id="nomeCliente" value="MORITZ">

            <label for="enderecoCliente">Endereço:</label>
            <input type="text" id="enderecoCliente">

            <label for="cidadeCliente">Cidade:</label>
            <input type="text" id="cidadeCliente" value="Ponta Grossa">

            <label for="ufCliente">UF:</label>
            <input type="text" id="ufCliente" value="PR" maxlength="2">

            <label for="emailCliente">E-mail:</label>
            <input type="email" id="emailCliente">

            <label for="telCliente">Telefone:</label>
            <input type="text" id="telCliente">

            <h3>Dados do Veículo</h3>
            <label for="tipoVeiculo">Caminhão / Caminhonete:</label>
            <input type="text" id="tipoVeiculo" value="Caminhão">

            <label for="corVeiculo">Cor:</label>
            <input type="text" id="corVeiculo">

            <label for="placaVeiculo">Placa:</label>
            <input type="text" id="placaVeiculo" value="ABC1D20">

            <label for="cidadeVeiculo">Cidade Veículo:</label>
            <input type="text" id="cidadeVeiculo">

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

            <button onclick="drawCanvas()">Gerar Orçamento no Canvas</button>
            <button id="savePdfButton" onclick="saveCanvasAsPdf()">Salvar PDF</button>
        </div>

        <div class="canvas-section">
            <canvas id="orcamentoCanvas" width="800" height="1100"></canvas>
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
            drawCanvas(); // Always redraw the canvas after updating the list
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
            drawCanvas(); // Always redraw the canvas after updating the list
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
            // Na janela de impressão, o usuário pode selecionar "Salvar como PDF"
            window.print();
        }


        // Chama as funções de renderização no carregamento para exibir os dados iniciais
        document.addEventListener('DOMContentLoaded', () => {
            renderPecas();
            renderServicos();
            drawCanvas(); // Ensure canvas is drawn on load with initial data
        });

        // Função para quebrar texto (permanece a mesma)
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
        }

        function drawCanvas() {
            // Limpa o canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Define a cor de fundo
            ctx.fillStyle = '#fcf9e7'; // Cor semelhante ao papel
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            // Define o estilo de desenho
            ctx.font = '14px Arial';
            ctx.fillStyle = '#333';
            ctx.strokeStyle = '#555';
            ctx.lineWidth = 1;

            let currentY = 50;
            const marginX = 50;
            const lineHeight = 20;

            // Cabeçalho
            ctx.font = 'bold 20px Arial';
            ctx.fillText('POSTO DE MOLAS SÃO BENTO', marginX, currentY);
            ctx.fillText('ORÇAMENTO', canvas.width - marginX - ctx.measureText('ORÇAMENTO').width, currentY);
            currentY += 25;
            ctx.font = 'bold 16px Arial';
            ctx.fillText('PEÇAS E SERVIÇOS', marginX, currentY);
            ctx.font = 'bold 20px Arial';
            ctx.fillText(`Nº ${document.getElementById('numeroOrcamento').value}`, canvas.width - marginX - ctx.measureText(`Nº ${document.getElementById('numeroOrcamento').value}`).width, currentY);
            currentY += 30;

            // Informações da Empresa
            ctx.font = '12px Arial';
            ctx.fillText('Suspensão de Caminhão e Caminhonete', marginX, currentY);
            currentY += 15;
            ctx.fillText('Alinhamento e Balanceamento - Suspensão a Ar', marginX, currentY);
            currentY += 15;
            ctx.fillText('42 99934-3158 | 42 99946-5858', marginX, currentY);
            ctx.fillText('CNPJ 50.076.502/0001-74', canvas.width - marginX - ctx.measureText('CNPJ 50.076.502/0001-74').width, currentY);
            currentY += 15;
            ctx.fillText('postodemolassaobento@gmail.com - Av. Souza Naves, 4250 - CEP 84064-000 - Ponta Grossa / PR', marginX, currentY);
            currentY += 30;

            // Detalhes do Cliente e Veículo
            ctx.font = 'bold 14px Arial';
            ctx.fillText('DADOS DO CLIENTE E VEÍCULO', marginX, currentY);
            currentY += lineHeight;
            ctx.font = '12px Arial';
            ctx.fillText(`Nome: ${document.getElementById('nomeCliente').value}`, marginX, currentY);
            ctx.fillText(`Endereço: ${document.getElementById('enderecoCliente').value}`, marginX + 250, currentY);
            currentY += lineHeight;
            ctx.fillText(`Cidade/UF: ${document.getElementById('cidadeCliente').value}/${document.getElementById('ufCliente').value}`, marginX, currentY);
            ctx.fillText(`E-mail: ${document.getElementById('emailCliente').value}`, marginX + 250, currentY);
            currentY += lineHeight;
            ctx.fillText(`Telefone: ${document.getElementById('telCliente').value}`, marginX, currentY);
            currentY += lineHeight;
            ctx.fillText(`Veículo: ${document.getElementById('tipoVeiculo').value}`, marginX, currentY);
            ctx.fillText(`Cor: ${document.getElementById('corVeiculo').value}`, marginX + 250, currentY);
            currentY += lineHeight;
            ctx.fillText(`Placa: ${document.getElementById('placaVeiculo').value}`, marginX, currentY);
            ctx.fillText(`Cidade Veículo: ${document.getElementById('cidadeVeiculo').value}`, marginX + 250, currentY);
            currentY += 30;

            // Cabeçalho da Tabela para Itens
            ctx.font = 'bold 12px Arial';
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('UNID.', marginX + 70, currentY);
            ctx.fillText('DESCRIÇÃO', marginX + 130, currentY);
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 150, currentY);
            ctx.fillText('TOTAL', canvas.width - marginX - 50, currentY);
            currentY += 5;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += 15;

            ctx.font = '12px Arial';
            let totalPecas = 0;
            // Desenha as Peças
            initialPecas.forEach(item => {
                const itemTotal = item.quant * item.precoUnit;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                ctx.fillText(item.unid, marginX + 70, currentY);
                wrapText(ctx, item.produto, marginX + 130, currentY, 300, lineHeight);
                ctx.fillText(formatCurrency(item.precoUnit), canvas.width - marginX - 150, currentY);
                ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX - 50, currentY);
                totalPecas += itemTotal;
                currentY += lineHeight;
            });
            currentY += 10;

            // Cabeçalho da Tabela para Serviços
            ctx.font = 'bold 12px Arial';
            ctx.fillText('QUANT.', marginX, currentY);
            ctx.fillText('DESCRIÇÃO', marginX + 130, currentY);
            ctx.fillText('VALOR UNIT.', canvas.width - marginX - 150, currentY);
            ctx.fillText('TOTAL', canvas.width - marginX - 50, currentY);
            currentY += 5;
            ctx.beginPath();
            ctx.moveTo(marginX, currentY);
            ctx.lineTo(canvas.width - marginX, currentY);
            ctx.stroke();
            currentY += 15;

            ctx.font = '12px Arial';
            let totalServicos = 0;
            // Desenha os Serviços
            initialServicos.forEach(item => {
                const itemTotal = item.quant * item.preco;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                wrapText(ctx, item.produto, marginX + 130, currentY, 300, lineHeight);
                ctx.fillText(formatCurrency(item.preco), canvas.width - marginX - 150, currentY);
                ctx.fillText(formatCurrency(itemTotal), canvas.width - marginX - 50, currentY);
                totalServicos += itemTotal;
                currentY += lineHeight;
            });
            currentY += 20;

            // Totais
            ctx.font = 'bold 14px Arial';
            ctx.fillText('TOTAL DE PEÇAS:', canvas.width - marginX - 200, currentY);
            ctx.fillText(formatCurrency(totalPecas), canvas.width - marginX - 50, currentY);
            currentY += lineHeight;

            ctx.fillText('TOTAL DE SERVIÇOS:', canvas.width - marginX - 200, currentY);
            ctx.fillText(formatCurrency(totalServicos), canvas.width - marginX - 50, currentY);
            currentY += lineHeight;

            ctx.fillText('TOTAL GERAL:', canvas.width - marginX - 200, currentY);
            ctx.fillText(formatCurrency(totalPecas + totalServicos), canvas.width - marginX - 50, currentY);
            currentY += lineHeight;

            // Rodapé
            currentY = canvas.height - 50;
            ctx.font = '10px Arial';
            ctx.fillText('Posto de Molas São Bento - Todos os direitos reservados.', canvas.width - marginX - ctx.measureText('Posto de Molas São Bento - Todos os direitos reservados.').width, currentY);
        }

    </script>
</body>
</html>
