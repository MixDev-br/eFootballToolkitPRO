## eFootball Toolkit PRO 2.3.0

Esta versão traz uma ampla reengenharia do motor de detecção e acompanhamento de partidas, com foco em precisão, continuidade e compatibilidade entre Steam, Xbox PC e OpenWrt.

### Monitor e partidas

- O motor de partidas foi amplamente reestruturado, com novas etapas de classificação e ciclo de vida para reconhecer conexões P2P e PSP com mais segurança.
- Trocas de IP, porta e transporte TCP/UDP agora são acompanhadas sem dividir indevidamente uma única partida.
- Corrigido o encerramento de partidas no Xbox PC que podiam permanecer presas no monitor ou ser substituídas sem o registro correto.
- Reencontros e adversários marcados agora distinguem melhor uma reconexão da mesma partida de uma nova sessão, com alertas visuais e bloqueios mais consistentes.

### Modos e rede

- Novo COOP inteligente com seleção de países, geolocalização rápida e bloqueio controlado somente depois que a partida é identificada; tentativas bloqueadas não são gravadas no histórico.
- P2P Experimental e COOP passaram a funcionar também pelo OpenWrt no aplicativo Windows, mantendo inalterado o fluxo já validado com captura local pelo Npcap.
- Catálogo regional ampliado com novos países, cidades e endpoints internacionais.

### Mobile

- Os avisos sonoros de partidas PSP e P2P agora são claramente diferentes, facilitando a identificação do tipo de conexão sem precisar olhar para a tela.

### DirectX e experiência do aplicativo

- Detecção do DirectX em uso revisada para Steam e Xbox PC.
- O clique direito no botão do eFootball permite iniciar a versão Steam com DX11 ou DX12, ou preservar integralmente as opções personalizadas do usuário.
- A primeira abertura agora começa pela escolha do idioma antes da ativação e inclui um tutorial guiado da dashboard.
- Interfaces de Firewall, Central de Servidores e Rede e Overlay foram reorganizadas, com melhorias gerais de responsividade e legibilidade.
- Encerramento do aplicativo e limpeza dos componentes de captura ficaram mais rápidos e confiáveis.
