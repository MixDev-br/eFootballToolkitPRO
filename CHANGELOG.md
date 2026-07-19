# Histórico de versões

## eFootball Toolkit PRO 1.6 — 19/07/2026

Esta atualização traz melhorias importantes no overlay, no histórico de partidas, nos filtros temporários e no desempenho geral.

### Novidades

- Canal de atualizações migrado para um manifesto assinado publicado no GitHub.
- FPS real do eFootball no overlay, sem depender de RTSS ou MSI Afterburner.
- Compatibilidade da medição de FPS com Steam e Xbox PC.
- Histórico persistente ampliado de 20 para 200 partidas.
- Nome personalizado ao marcar um adversário pelo overlay.
- Nome salvo exibido no gerenciamento de adversários e partidas.
- Criação, edição e exclusão de regras personalizadas no Editor de Firewall.
- Regras personalizadas vinculadas aos modos P2P/PSP, TCP ou COOP.
- Configuração de ação, direção, protocolo, perfil, IPs e portas.
- Validade em meses adicionada ao Gerenciador de Licenças.

### Correções

- Corrigida a leitura que apresentava aproximadamente metade do FPS real.
- Corrigida a opção de exibir ou ocultar reencontros no overlay.
- Corrigidas pequenas travadas ao mover o overlay.
- Corrigidos engasgos ao alternar entre as páginas do aplicativo.
- Corrigido o excesso de atualizações visuais quando nenhuma informação havia mudado.

### Desempenho e estabilidade

- Leitura de FPS isolada da interface em thread e processo próprios.
- Superfície de amostragem gráfica reduzida sem perder a cadência real dos quadros.
- Atualizações do overlay suspensas durante o arrasto.
- Widgets e estilos redesenhados somente quando os dados mudam.
- Processamento da fila de eventos limitado por lote e por tempo, preservando a resposta aos cliques.
- Regras de firewall continuam temporárias e são removidas ao fechar o Toolkit.
