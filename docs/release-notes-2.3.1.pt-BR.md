## eFootball Toolkit PRO 2.3.1

Esta atualização consolida as correções encontradas após a versão 2.3.0 e melhora a precisão da identificação de partidas P2P no Windows e no Android.

### Geolocalização P2P

- Novo sistema de geolocalização com consenso entre três fontes independentes, consultadas em paralelo para manter a identificação rápida.
- Ping STUN e distância física agora participam da validação, reduzindo localizações incompatíveis com a latência observada.
- Cache inteligente reaproveita evidências recentes sem prender o aplicativo a uma resposta incorreta.
- A mesma lógica está disponível no Windows e no Mobile, sem depender de requisições ao Worker do Toolkit.

### Monitor de partidas

- Refinado o ciclo de encerramento e reconexão de partidas P2P para reduzir sessões encerradas cedo demais e reencontros classificados como continuação da partida anterior.
- Melhor tratamento das retomadas de tráfego do mesmo endpoint e das mudanças de IP, porta e transporte durante uma sessão.
- Ajustes adicionais na identificação de adversários marcados e nos alertas de reencontro.

### Aplicativo e atualizações

- Corrigida a opção da Steam para preservar as instruções de inicialização personalizadas sem alterá-las ao abrir o jogo.
- O Mobile agora consulta o mesmo manifesto assinado do Windows, valida versão, assinatura, tamanho e SHA-256 antes de entregar o APK ao instalador do Android.
- A compilação pública do Windows não inclui a interface nem a coleta do log detalhado de diagnóstico.

