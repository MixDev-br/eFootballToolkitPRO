# Histórico de versões

## eFootball Toolkit Mobile 2.3.1 — build 10

- Dispositivos sem nome podem ser renomeados na seleção do OpenWrt pelo botão de lápis.
- Os nomes ficam salvos no APK pelo MAC, inclusive após reabrir o aplicativo ou trocar o IP.
- É possível editar ou remover o nome salvo.
- A lista se adapta a telas pequenas e a texto ampliado.

## eFootball Toolkit PRO 2.3.1 — 03/09/2026

Atualização de precisão e estabilidade após a ampla renovação do monitor na versão 2.3.0.

### Geolocalização e monitor

- A localização de partidas P2P agora usa consenso entre três fontes independentes consultadas em paralelo no Windows e no Android.
- Ping STUN e distância física participam da validação para reduzir resultados geográficos incompatíveis com a latência observada.
- Refinado o encerramento e a retomada de partidas P2P para distinguir melhor oscilações da mesma conexão e novos reencontros.
- Ajustes adicionais nos alertas de adversários marcados e nas mudanças de endpoint durante uma sessão.

### Aplicativos e atualização

- Corrigida a opção da Steam que preserva integralmente as instruções personalizadas de inicialização.
- O Mobile passou a usar o mesmo manifesto assinado do Windows, com validação de assinatura, versão, tamanho e SHA-256 do APK.
- A compilação pública do Windows não inclui a ferramenta interna de log detalhado usada nas builds de diagnóstico.

## eFootball Toolkit PRO 2.3.0 — 01/09/2026

Esta versão traz uma ampla reengenharia do motor de detecção e acompanhamento de partidas, com foco em precisão, continuidade e compatibilidade entre Steam, Xbox PC, Android e OpenWrt.

### Monitor e partidas

- O motor de partidas foi amplamente reestruturado para reconhecer com mais segurança o início, o encerramento, as reconexões e as trocas de IP, porta e transporte TCP/UDP.
- Corrigidas partidas do Xbox PC que podiam permanecer presas no monitor ou ser substituídas sem o encerramento correto.
- Reencontros e adversários marcados agora distinguem melhor uma reconexão da mesma partida de uma nova sessão, com alertas e bloqueios mais consistentes.
- Servidores fora da faixa tradicional e transições de endpoint passam a ser acompanhados sem dividir indevidamente uma única partida.

### Modos, rede e regiões

- Novo COOP inteligente com seleção de países, geolocalização rápida e bloqueio controlado somente depois que a partida é identificada.
- P2P Experimental e COOP agora funcionam também pelo OpenWrt no aplicativo Windows, preservando o fluxo de captura local pelo Npcap.
- Catálogo regional ampliado com novos países, cidades e endpoints internacionais.
- No Mobile, os alertas de partidas PSP e P2P agora usam sons claramente diferentes.

### DirectX e experiência do aplicativo

- Detecção do DirectX revisada para Steam e Xbox PC.
- O clique direito no botão do eFootball permite iniciar a versão Steam com DX11 ou DX12, ou preservar as opções personalizadas do usuário.
- A primeira abertura começa pela escolha do idioma antes da ativação e inclui um tutorial guiado da dashboard.
- Telas de Jogo, Firewall, Central de Servidores e Rede e Overlay reorganizadas para melhorar legibilidade, responsividade e navegação.
- Encerramento do aplicativo e limpeza dos componentes de captura ficaram mais rápidos e confiáveis.

## eFootball Toolkit PRO 2.1.2 — 29/08/2026

Atualização obrigatória focada em estabilidade, personalização e continuidade das preferências do jogador.

### Novidades

- O modo P2P Experimental permite escolher o uso do bloqueio DNS e alterar essa opção pelo clique direito.
- Nova tela de abertura mais limpa e moderna.
- O site agora avisa sobre a instalação obrigatória do Npcap antes dos downloads para Windows.

### Correções e melhorias

- O último modo de jogo e o último escopo do firewall escolhidos ficam salvos entre as execuções.
- Reconexões rápidas da mesma partida foram refinadas para evitar reencontros falsos.
- Corrigidas travadas na interface ao alternar o P2P Experimental e o escopo das regras.
- Melhorias gerais de estabilidade, mensagens e acabamento visual.

## eFootball Toolkit PRO 2.1.1 — 25/08/2026

Atualização obrigatória com novos recursos de comunicação, melhorias no monitor e expansão do aplicativo Mobile.

### Novidades

- Central de notificações no Windows, com avisos oficiais organizados por prioridade.
- Novo modo P2P Experimental para testar uma combinação alternativa de proteções.
- Aplicativo Mobile com central de adversários, histórico de partidas e novos modos pelo OpenWrt.
- Regras Force P2P separadas em portas, DNS e servidores, permitindo combinações personalizadas.

### Correções e melhorias

- Reconexões rápidas da mesma partida deixam de aumentar incorretamente o contador de reencontros.
- Monitor e regras via OpenWrt ficaram mais estáveis no Windows e no Android.
- Informações de servidor e adversário foram simplificadas na área de detalhes.
- Interface e mensagens revisadas para a distribuição pública.

## eFootball Toolkit PRO 2.1.0 — 24/08/2026

Atualização obrigatória que amplia o Toolkit para PC e consoles por meio do OpenWrt.

### Novidades

- Integração guiada com roteadores OpenWrt para monitorar PC, PlayStation e Xbox.
- Aplicativo Mobile com monitor de partidas e modos X1 e COOP.
- Avaliação gratuita do Mobile por 30 dias durante a etapa inicial.
- O Windows agora lista todas as placas de rede disponíveis.
- O botão do eFootball informa a versão do DirectX detectada durante o jogo.
- Configuração do OpenWrt simplificada e diagnóstico de conectividade IPv6.

### Correções e melhorias

- Encerramento das partidas e captura pelo roteador mais confiáveis.
- Overlay com posição e tamanhos personalizados preservados.
- Interface, mensagens e fluxo de configuração revisados para distribuição.
- Modos X1 e COOP do Mobile ajustados para o uso pelo roteador.

## eFootball Toolkit PRO 2.0.3 — 03/08/2026

Atualização obrigatória focada em compatibilidade, medição e estabilidade das partidas.

### Correções

- Regras locais do Firewall do Windows voltaram a poder ser vinculadas aos modos personalizados.
- Partidas LAN agora exibem corretamente a rede local no monitor, overlay e histórico.
- A medição de ping em partidas PSP tenta novamente quando o servidor descarta a primeira resposta.
- O encerramento de partidas PSP ficou mais confiável.

### Melhorias

- Alertas sonoros distintos para partidas PSP, P2P e LAN.
- Prévia dos alertas disponível nas configurações.

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
