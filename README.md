# eFootball Toolkit PRO

<p align="center">
  <strong>Monitoramento de partidas, overlay e ferramentas de rede para eFootball no Windows e consoles.</strong>
</p>

<p align="center">
  <a href="README.md"><img src="docs/images/language-pt-br.svg" alt="Português (Brasil)" height="42"></a>
  <a href="README.en-US.md"><img src="docs/images/language-en-us.svg" alt="English (US)" height="42"></a>
  <a href="README.es-ES.md"><img src="docs/images/language-es-es.svg" alt="Español (España)" height="42"></a>
</p>

<p align="center">
  <a href="https://mixdev-br.github.io/eFootballToolkitPRO/?lang=pt"><strong>Site oficial</strong></a>
  ·
  <a href="https://github.com/MixDev-br/eFootballToolkitPRO/releases/latest"><strong>Baixar versão PRO</strong></a>
  ·
  <a href="https://github.com/MixDev-br/eFootballToolkitPRO/releases/tag/trial-v2.1.1"><strong>Testar no Windows por 5 dias</strong></a>
  ·
  <a href="OPENWRT_MOBILE_GUIDE.md"><strong>Guia Mobile e OpenWrt</strong></a>
</p>

<p align="center">
  <img alt="Versão 2.1.1" src="https://img.shields.io/badge/versão-2.1.1-22d3ee">
  <img alt="Windows 10 e 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-2563eb">
  <img alt="Compatível com Steam e Xbox PC" src="https://img.shields.io/badge/eFootball-Steam%20%7C%20Xbox%20PC-10b981">
  <img alt="Idiomas disponíveis" src="https://img.shields.io/badge/idiomas-PT%20%7C%20EN%20%7C%20ES-a855f7">
</p>

> Este é o canal oficial de distribuição do eFootball Toolkit PRO. O repositório contém os pacotes prontos para uso, o manifesto de atualização e a documentação pública.

## Visão geral

O Toolkit reúne informações que normalmente ficam espalhadas ou escondidas durante a busca por partidas:

- ping, região, distância e endpoint da sessão em tempo real;
- identificação de partidas P2P e partidas em servidor;
- overlay compacto sobre o jogo;
- central de servidores com medições por país;
- modos e regras temporárias de firewall;
- histórico de partidas, adversários e reencontros;
- diagnóstico de controles Xbox e PlayStation;
- suporte ao eFootball da **Steam** e do **Xbox PC**;
- monitoramento de PC, PlayStation e Xbox pelo **OpenWrt**;
- aplicativo Mobile para acompanhar partidas e controlar os modos X1 e COOP.

## Conheça o aplicativo

### Monitor da partida

![Tela principal do monitor](docs/images/01-monitor-principal.png)

A tela principal concentra o estado da captura e as informações da sessão. Quando uma partida é encontrada, o painel apresenta:

- **tipo da conexão**, como P2P ou servidor;
- **destino e protocolo** usados pela partida;
- **ping**, região identificada e distância aproximada;
- eventos importantes no painel **Atividade**;
- detalhes de conexão, servidor e adversário nos campos **IP1, IP2 e IP3**;
- atalhos para iniciar o eFootball, controlar o monitor, trocar o modo de jogo e abrir a central de adversários.

### Firewall e modos de jogo

![Tela de firewall](docs/images/02-firewall.png)

A área de Firewall controla onde as regras temporárias do modo escolhido serão aplicadas:

- **Somente eFootball:** limita os filtros ao executável do jogo;
- **Sistema inteiro:** aplica o modo à máquina, opção recomendada para a edição Xbox PC;
- **Sem regras:** mantém o monitor funcionando sem solicitar filtros do Toolkit.

O painel também informa o escopo escolhido, a plataforma detectada, o modo em uso e a quantidade de filtros ativos. As proteções são transitórias e deixam de existir quando a sessão do aplicativo é encerrada.

<details>
<summary><strong>Editor de regras personalizadas</strong></summary>

![Editor de regras de firewall](docs/images/03-editor-regras.png)

O editor permite criar, revisar e restaurar regras personalizadas. Apenas regras criadas pelo usuário ou encontradas no Windows são expostas nessa tela; as definições internas do Toolkit permanecem protegidas.

</details>

<details>
<summary><strong>Vincular regras existentes do Windows</strong></summary>

![Janela para vincular regras do Windows](docs/images/04-vincular-regras.png)

Essa janela permite aproveitar definições já existentes no Firewall do Windows em funções do Toolkit. Nome, direção, protocolo, endereços e portas são importados sem ativar, desativar ou modificar a regra original.

</details>

### Central de servidores

![Central de servidores](docs/images/05-central-servidores.png)

A central organiza os servidores conhecidos em uma lista compacta com país, endereço, estado do filtro e resultado da medição. Nela é possível:

- testar todos os destinos ou escolher um país específico;
- buscar por IP, medição ou estado;
- adicionar um endereço IPv4 ou IPv6 público;
- bloquear, liberar, editar ou testar somente um servidor;
- acompanhar quantos destinos estão permitidos, bloqueados e disponíveis.

Os resultados exibidos são medições reais. Quando um destino não responde, o Toolkit mantém o estado como não testado ou sem resposta em vez de inventar um ping.

<details>
<summary><strong>Seleção regional</strong></summary>

![Seleção de países e servidores](docs/images/06-selecao-regional.png)

O seletor regional ajuda a priorizar países durante a procura por partidas. O usuário escolhe os destinos preferidos, enquanto o Toolkit trata temporariamente os demais destinos durante a busca. Novos IPs públicos observados podem ser verificados e catalogados localmente.

Esse recurso auxilia a seleção, mas não garante que a organização da partida será feita em uma região específica.

</details>

### Rede e overlay

![Personalização de rede e overlay](docs/images/07-rede-overlay.png)

Nesta tela o usuário escolhe a placa de rede usada na captura e personaliza o painel flutuante:

- formato de uma ou duas linhas;
- nível de opacidade;
- blocos visíveis;
- status, modo, distância, ping e perda;
- FPS, polling do controle, reencontros, endpoint, região e hora;
- prévia instantânea antes de voltar ao jogo.

#### Overlay durante o jogo

![Overlay do eFootball Toolkit](docs/images/11-overlay-em-jogo.png)

O overlay mantém os dados essenciais visíveis sem ocupar a tela principal. Ele acompanha a partida em tempo real e pode mostrar apenas os campos escolhidos pelo usuário. Quando a sessão permite marcar um adversário, o botão **Marcar IP** aparece no lado direito.

### Central de adversários e partidas

![Central de bloqueados e partidas](docs/images/08-central-adversarios.png)

A central separa as informações em três listas:

- **Bloqueados agora:** filtros ativos na sessão atual;
- **Reencontros:** adversários marcados para identificação futura;
- **Partidas:** histórico das sessões protegidas.

As colunas reúnem nome, IPs observados, região, data, ping e distância quando essas informações estão disponíveis. O bloqueio automático é uma proteção auxiliar: mudanças de IP, conexões compartilhadas ou decisões da própria infraestrutura do jogo podem impedir o cancelamento automático de uma partida.

### Testador de controle

![Testador de controle Xbox](docs/images/09-testador-controle.png)

O diagnóstico reconhece controles compatíveis e apresenta uma representação visual adequada para Xbox ou PlayStation. Botões, gatilhos e analógicos reagem aos comandos em tempo real.

Quando o dispositivo disponibiliza as informações, a tela também mostra:

- tipo de conexão;
- estado da bateria;
- suporte a vibração;
- taxa de polling e intervalo médio;
- comportamento dos analógicos e entradas pressionadas.

### Configurações

![Configurações do aplicativo](docs/images/10-configuracoes-redigida.png)

As preferências ficam reunidas em uma tela única e são restauradas na próxima abertura. Entre as opções estão:

- português, inglês e espanhol;
- alerta sonoro ao encontrar partida;
- início automático do monitor;
- abertura automática do overlay;
- avisos sobre modos e Xbox PC;
- restauração das regras do aplicativo;
- acesso direto ao suporte.

O código do dispositivo foi ocultado na imagem pública por segurança.

## Trial e PRO

| Recurso | Trial | PRO |
|---|:---:|:---:|
| Duração | 5 dias | Conforme o plano |
| Monitor de partida | Completo | Completo |
| Overlay | 1 linha essencial | Personalizável |
| Modos de jogo | X1 | X1, COOP e personalizados |
| Central de servidores | — | Completa |
| Histórico e adversários | — | Completo |
| Ferramentas de firewall | Limitadas | Completas |
| Chave ou cartão para testar | Não | — |

## Download

- [Baixar eFootball Toolkit PRO 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/v2.1.1/eFootball-Toolkit-PRO-v2.1.1.zip)
- [Baixar eFootball Toolkit TRIAL 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/trial-v2.1.1/eFootball-Toolkit-TRIAL-v2.1.1.zip)
- [Baixar eFootball Toolkit Mobile 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/v2.1.1/eFootball-Toolkit-Mobile-v2.1.1.apk)
- [Configurar o Mobile e o OpenWrt](OPENWRT_MOBILE_GUIDE.md)
- [Consultar todas as versões](https://github.com/MixDev-br/eFootballToolkitPRO/releases)

Cada versão inclui o pacote `.zip`, um arquivo `.sha256` para conferência de integridade e as notas da atualização.

## Requisitos

- Windows 10 ou Windows 11;
- eFootball para Steam ou Xbox PC;
- privilégios de administrador para os filtros temporários;
- [Npcap](https://npcap.com/#download) instalado.

O **Npcap** é o componente usado para observar o tráfego de rede local necessário às medições do monitor. Baixe-o somente pelo site oficial.

## Instalação

1. Instale o [Npcap oficial](https://npcap.com/#download).
2. Baixe a versão PRO ou Trial pelas Releases.
3. Extraia **todo o conteúdo** do arquivo ZIP.
4. Mantenha o executável junto da pasta `runtime`.
5. Execute `eFootballToolkitPRO.exe`.

Não mova nem execute apenas o `.exe` isoladamente.

## Atualizações e integridade

O aplicativo consulta o manifesto assinado `update_manifest.json` deste repositório. Os pacotes são baixados exclusivamente pelas Releases e aceitos somente depois da validação de assinatura, tamanho e SHA-256.

Para conferir manualmente um download no PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\eFootball-Toolkit-PRO-v2.1.1.zip
```

Compare o resultado com o arquivo `.sha256.txt` publicado na mesma Release.

## Suporte

- Site: [mixdev-br.github.io/eFootballToolkitPRO](https://mixdev-br.github.io/eFootballToolkitPRO/?lang=pt#suporte)
- E-mail: [efootballtoolkitpro.suporte@gmail.com](mailto:efootballtoolkitpro.suporte@gmail.com)

Ao solicitar ajuda, informe a versão do Toolkit, se utiliza Steam ou Xbox PC e descreva o comportamento observado.

---

eFootball Toolkit PRO é um projeto independente e não possui vínculo com a KONAMI.
