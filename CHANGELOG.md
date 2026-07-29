# Histórico de versões

## eFootball Toolkit PRO 2.0.1 — 29/07/2026

Atualização focada em estabilidade, automação e precisão das informações.

### Correções

- Corrigido o overlay que não abria quando o monitor iniciava automaticamente com o aplicativo.
- Corrigido o cálculo do ping médio ao testar somente um país na Central de Servidores.
- Aplicativo e overlay agora encerram juntos com mais rapidez.
- Abertura do overlay mais confiável durante a inicialização.
- Proteção de reencontros refinada para maior estabilidade.

### Melhorias

- Novos servidores podem ser reconhecidos depois de uma partida confirmada.
- Inicialização automática do monitor agora segue o mesmo fluxo do acionamento manual.
- Novo teste de regressão garante a abertura automática do overlay mesmo antes de o eFootball ser iniciado.

## eFootball Toolkit PRO 2.0 — 28/07/2026

A versão 2.0 apresenta uma interface totalmente renovada e reúne monitor,
overlay, servidores, ferramentas de rede e diagnóstico em uma experiência mais
clara e organizada.

### Novidades e melhorias

- Nova interface com navegação reorganizada.
- Overlay redesenhado, redimensionável e com informações ao vivo.
- Monitor de partidas aprimorado para IPv4, IPv6 e reconexões.
- Central de Servidores com seleção por países e testes de ping.
- Histórico de partidas, adversários e reencontros mais organizado.
- Diagnóstico de controles Xbox e PlayStation.
- Suporte a português, inglês e espanhol.
- Atualizações automáticas com suporte a versões obrigatórias.

### Instalação

- Instale o [Npcap pelo site oficial](https://npcap.com/#download).
- Extraia todo o conteúdo do ZIP.
- Execute o Toolkit como administrador.

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
