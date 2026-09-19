# Atualizações de 19/09/2026

# eFootball Toolkit PRO 2.3.5

Mudanças em relação à versão 2.3.4.

## Controle regional

- O antigo modo COOP e o seletor de atraso separado foram reunidos no **Region Selector**, na barra lateral. A seleção anterior de países é migrada, evitando duas configurações para a mesma finalidade.
- O Region Selector atende partidas por servidor, incluindo COOP. No PC, aplica 500 ms aos testes de conexão fora dos países permitidos e bloqueia servidores recusados quando identificados. Requer monitor e regras habilitados.
- Com a extensão EFT MATCH ativa, o bloqueio regional do COOP pode começar a partir dos relays recebidos na busca. Sem a extensão, continua usando a detecção do Monitor.
- Novo filtro de regiões X1 com países permitidos e opções PSP, P2P ou ambas. No PC, usa a extensão EFT MATCH, funciona independentemente do modo e do escopo geral das regras e não é aplicado às sessões identificadas como COOP.
- O filtro P2P trata os endereços IPv4 e IPv6 disponíveis do adversário para evitar que uma troca entre as duas conexões contorne o bloqueio. Países não identificados não são bloqueados por suposição.
- Novas explicações nos controles regionais e avisos de bloqueio ou falha no overlay.

## EFT MATCH, adversários e histórico

- Melhor reconhecimento de partidas COOP, inclusive para quem entra como convidado, com separação entre companheiros de equipe e adversários.
- O overlay da extensão mostra até três adversários do COOP simultaneamente. O overlay do Toolkit permite alternar entre eles para consultar e marcar cada jogador.
- Campo de apelido com lista de nicks salvos, seleção e opção de salvar um novo nick. O nick continua sendo informado pelo usuário.
- Melhor uso dos endereços da sessão para localizar o adversário e calcular a distância até o servidor efetivamente utilizado. No COOP, a localização acompanha o adversário selecionado; dados ausentes permanecem indisponíveis.
- Melhor continuidade dos dados EFT durante interrupções breves e mudanças entre conexões P2P e servidor, preservando a identidade da partida e evitando duplicação no histórico. Uma nova busca não deve herdar os dados da anterior.
- Histórico com nick, identificação EFT e plataforma, além da possibilidade de marcar o jogador pela conta a partir da partida registrada.

## Testes da Konami

- Nova janela com pings por região recebidos do jogo, busca por país/região, datas disponíveis e indicadores da atividade do atraso.
- Explicações e tooltip sobre o funcionamento, a necessidade de iniciar a extensão nas configurações do Toolkit e o procedimento quando todos os valores aparecem como N/A.
- Avaliação automática indica se os pings fora dos países permitidos são compatíveis com o atraso ou se o cache ainda pode estar sem ele. É uma estimativa: ping alto, sozinho, não confirma atraso aplicado nem garante um servidor específico.

## OpenWrt

- O monitor usa o dispositivo selecionado no roteador, sem precisar abrir eFootball no PC.
- Correção da identificação do modo OpenWrt ao reabrir o Toolkit, incluindo os casos em que a configuração existe mas o roteador está indisponível.
- Opções que dependem da extensão EFT MATCH e do atraso de servidores ficam indisponíveis com explicação. No OpenWrt, o Region Selector usa o bloqueio pelo Monitor, sem injetar atraso.
- Traduções da configuração e dos controles OpenWrt em português, inglês e espanhol.

## Monitor e produção

- Atualização do ping e da perda ICMP no overlay quando chegam novas medições, evitando manter o percentual anterior. A perda ICMP é uma estimativa das sondas ao servidor, não uma medição direta da perda de todos os pacotes do jogo.
- Logs detalhados de diagnóstico do monitor e da extensão EFT MATCH desativados na versão de produção.
- Mensagens técnicas do EFT MATCH removidas de Atividades, preservando os eventos do monitor e avisos ao usuário. A cópia das atividades usa a notificação visual do Toolkit, com tooltip e confirmação traduzidos.
- Filtro de regiões X1 com textos e países traduzidos para inglês e espanhol; busca e ordenação seguem o idioma escolhido.

O EFT MATCH permanece opcional e exige licença própria. Os recursos que usam seus dados dependem da extensão ativa e atualizada no PC; não estão disponíveis no console via OpenWrt. Licenças e configurações salvas são preservadas.


# EFT MATCH 0.2.6 — build 9

Mudanças em relação à versão 0.2.5, build 8.

## Português

- Reconhecimento de partidas COOP, inclusive ao participar como convidado, usando a mesma lógica compartilhada com a extensão do Toolkit para identificar a equipe adversária.
- Overlay com até três adversários do COOP visíveis ao mesmo tempo. Alterações na lista também atualizam o painel, mesmo quando o primeiro adversário permanece igual.
- Ao voltar para uma partida X1, o overlay retorna ao formato individual. A opção de ocultar e reexibir preserva a lista COOP da sessão atual.
- Campo de apelido com menu de nicks salvos e opção de salvar um novo nick. A seleção permanece disponível após reiniciar o aplicativo.
- Fluxo de produção sem coleta adicional de comandos exclusivos de diagnóstico. O processamento necessário à identificação das partidas continua ativo.

O nick continua sendo informado pelo usuário. No COOP, o painel apresenta os nomes e plataformas disponíveis; não promete divisão, ranking ou força coletiva quando esses dados não chegam. O aplicativo continua exigindo sua licença EFT MATCH e acesso à internet.

## English

- COOP recognition, including when joining as a guest, using the same shared opponent-team identification logic as the Toolkit extension.
- The overlay shows up to three COOP opponents together. Roster changes refresh the panel even if the first opponent stays the same.
- Returning to X1 restores the individual opponent layout. Hiding and showing the overlay preserves the current COOP roster.
- Saved nickname dropdown with an option to save another nickname. Your selection remains available after restarting the app.
- Production flow excludes additional commands used only for diagnostics. Processing required to identify matches remains active.

Your nickname still needs to be entered manually. COOP displays available names and platforms; division, ranking and team strength are not promised when the data is unavailable. An EFT MATCH license and internet access are still required.


# eFootball Toolkit Mobile 2.3.2 — build 14

- Bandeiras ao lado da localização das partidas.
- Filtro de Região X1 com países permitidos e ativação independente das regras do modo.
- SMART COOP passa a se chamar Seletor de Região, com ajuda explicativa dos modos e filtros.
- Verificação real da conexão OpenWrt ao iniciar, estado desconectado visível e opção de iniciar o monitor automaticamente.
- Usuário e senha SSH salvos em armazenamento seguro para reutilização na configuração.
- Idiomas PT/EN com seleção persistente.
- Correção do painel cinza ao rolar a lista de países.
- Ferramentas experimentais de coleta e logs removidas das Configurações de produção.

Requer roteador OpenWrt compatível. O filtro usa a conexão identificada pelo monitor; não injeta atraso nem oferece dados da extensão EFT MATCH.

## English

- Country flags next to match locations.
- X1 region filter with allowed countries and activation independent of mode rules.
- SMART COOP renamed to Region Selector, with help for modes and filters.
- Verified OpenWrt connection at startup, visible disconnected state and optional automatic monitoring.
- SSH credentials saved in secure storage for setup reuse.
- Persistent PT/EN language selection.
- Fixed the gray panel when scrolling the country list.
- Experimental capture and logging tools removed from production Settings.

Requires a compatible OpenWrt router. Filtering uses the connection identified by the monitor; it does not inject delay or provide EFT MATCH extension data.


---

# Histórico de versões

## EFT MATCH 0.2.3 — 09/09/2026

Melhorias importantes de segurança, estabilidade e proteção dos componentes internos. Esta é uma atualização obrigatória para continuar utilizando o EFT MATCH.

Important improvements to security, stability and protection of internal components. This update is required to continue using EFT MATCH.

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
