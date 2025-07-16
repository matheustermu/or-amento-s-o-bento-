function drawCanvas() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = '#fcf9e7';
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = '#333';
    ctx.strokeStyle = '#555';
    ctx.lineWidth = 1.5;

    const baseFontSize = 18; // Reduzido para 18px
    const baseLineHeight = 30; // Reduzido para 30px
    let currentY = 70; // Margem superior
    const marginX = 70; // Margem lateral
    const infoOffset = 380; // Offset para a segunda coluna de informações

    // --- Cabeçalho ---
    ctx.font = 'bold 36px Arial'; // Aumentado ligeiramente para 30px para o título principal
    ctx.fillText('POSTO DE MOLAS SÃO BENTO', marginX, currentY);
    ctx.textAlign = 'right';
    ctx.font = 'bold 32px Arial'; // Mantido em 32px para "ORÇAMENTO"
    ctx.fillText('ORÇAMENTO', canvas.width - marginX, currentY);
    ctx.textAlign = 'left';
    currentY += 45;

    ctx.font = 'bold 24px Arial'; // Reduzido para 24px
    ctx.fillText('PEÇAS E SERVIÇOS', marginX, currentY);
    ctx.textAlign = 'right';
    const numeroOrcamento = document.getElementById('numeroOrcamento').value || 'Não Informado';
    ctx.fillText(`Nº ${numeroOrcamento}`, canvas.width - marginX, currentY);
    ctx.textAlign = 'left';
    currentY += 55;

    // --- Informações da Empresa ---
    ctx.font = `${baseFontSize}px Arial`; // Agora 18px
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
    ctx.font = `bold ${baseFontSize + 4}px Arial`; // Agora 22px
    ctx.fillText('DADOS DO CLIENTE E VEÍCULO', marginX, currentY);
    currentY += baseLineHeight + 10;
    ctx.font = `${baseFontSize}px Arial`; // Fonte base 18px

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

    // --- Cabeçalho da Tabela para Peças ---
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

    ctx.font = `${baseFontSize}px Arial`; // Agora 18px para os itens
    let totalPecas = 0;
    let pecasLinesCount = 0; // Contador de linhas de peças
    const maxPecasLines = 6; // Limite de linhas visíveis para peças

    if (initialPecas.length > 0) {
        initialPecas.forEach(item => {
            if (pecasLinesCount < maxPecasLines) {
                const itemTotal = item.quant * item.precoUnit;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                ctx.fillText(item.unid, marginX + 100, currentY);
                const linesUsed = wrapText(ctx, item.produto, marginX + 200, currentY, 280, baseLineHeight - 8); // Largura reduzida para descrição
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

    // Preenche com linhas vazias se houver menos que o máximo
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
    currentY += 50; // Mais espaço

    // --- Título da Seção de Serviços ---
    ctx.font = `bold ${baseFontSize + 4}px Arial`;
    ctx.fillText('SERVIÇOS:', marginX, currentY);
    currentY += baseLineHeight + 5;

    // --- Cabeçalho da Tabela para Serviços ---
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

    ctx.font = `${baseFontSize}px Arial`; // Agora 18px para os itens
    let totalServicos = 0;
    let servicosLinesCount = 0; // Contador de linhas de serviços
    const maxServicosLines = 6; // Limite de linhas visíveis para serviços

    if (initialServicos.length > 0) {
        initialServicos.forEach(item => {
            if (servicosLinesCount < maxServicosLines) {
                const itemTotal = item.quant * item.preco;
                ctx.fillText(item.quant.toFixed(2), marginX, currentY);
                const linesUsed = wrapText(ctx, item.produto, marginX + 200, currentY, 280, baseLineHeight - 8); // Largura reduzida para descrição
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

    // Preenche com linhas vazias se houver menos que o máximo
    for (let i = servicosLinesCount; i < maxServicosLines; i++) {
        ctx.fillText('0.00', marginX, currentY);
        wrapText(ctx, '', marginX + 200, currentY, 280, baseLineHeight - 8);
        ctx.textAlign = 'right';
        ctx.fillText('R$ 0,00', canvas.width - marginX - 200, currentY);
        ctx.fillText('R$ 0,00', canvas.width - marginX, currentY);
        ctx.textAlign = 'left';
        currentY += baseLineHeight - 8;
    }
    currentY += 60; // Mais espaço

    // --- Totais ---
    ctx.font = `bold ${baseFontSize + 6}px Arial`; // Agora 24px
    ctx.textAlign = 'right';
    ctx.fillText('TOTAL DE PEÇAS:', canvas.width - marginX - 250, currentY);
    ctx.fillText(formatCurrency(totalPecas), canvas.width - marginX, currentY);
    currentY += baseLineHeight + 15;

    ctx.fillText('TOTAL DE SERVIÇOS:', canvas.width - marginX - 250, currentY);
    ctx.fillText(formatCurrency(totalServicos), canvas.width - marginX, currentY);
    currentY += baseLineHeight + 15;

    ctx.font = 'bold 30px Arial'; // Agora 30px
    ctx.fillText('TOTAL GERAL:', canvas.width - marginX - 250, currentY);
    ctx.fillText(formatCurrency(totalPecas + totalServicos), canvas.width - marginX, currentY);

    ctx.textAlign = 'left';
    currentY = canvas.height - 70; // Força o rodapé para 70 pixels da parte inferior

    // --- Rodapé ---
    ctx.font = '18px Arial';
    ctx.textAlign = 'center';
    ctx.fillText('Posto de Molas São Bento - Todos os direitos reservados.', canvas.width / 2, currentY);
    ctx.textAlign = 'left';
}
