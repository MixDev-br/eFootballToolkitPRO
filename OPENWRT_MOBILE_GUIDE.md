# eFootball Toolkit Mobile com OpenWrt

Este guia mostra o que você precisa para monitorar partidas do eFootball no PC, PlayStation ou Xbox usando o aplicativo Android e um roteador com OpenWrt.

> O firmware original do fabricante não é suficiente. O roteador precisa estar executando OpenWrt e aparecer como **compatível** no assistente do Toolkit.

## Antes de começar

Você precisa de:

- um celular Android com o eFootball Toolkit Mobile;
- um roteador com OpenWrt, acesso por SSH e o pacote `nftables` disponível;
- PC, PlayStation ou Xbox conectado à rede desse roteador;
- usuário administrador e senha do OpenWrt somente durante a instalação;
- pelo menos 256 KiB livres no armazenamento persistente; 512 KiB ou mais é recomendado;
- uma licença Mobile válida e vinculada ao código `AND-...` do celular.

Não abra portas no roteador e não exponha o painel do OpenWrt à internet. O aplicativo e o agente se comunicam somente dentro da rede local.

## Arquiteturas aceitas

O assistente escolhe automaticamente o agente correto para estas arquiteturas:

| Arquitetura detectada pelo OpenWrt | Agente do Toolkit |
| --- | --- |
| MIPS 24Kc big-endian | `mips_24kc` |
| MIPS 24Kc little-endian | `mipsel_24kc` |
| ARM Cortex-A7, Cortex-A9 ou ARMv7 | `arm_cortex-a7` |
| ARM64 / AArch64 | `aarch64` |
| x86-64 | `x86_64` |

A arquitetura compatível não garante, sozinha, que qualquer modelo funcionará bem. Memória, espaço livre, versão do OpenWrt e suporte a `nftables` também são verificados.

### Roteadores usados no desenvolvimento

- **TP-Link Archer C60 v2:** adequado para os testes do agente e do monitor.
- **D-Link DIR-505 A1:** pode executar OpenWrt, mas tem armazenamento e desempenho muito limitados; não é recomendado para clientes.

Para outro modelo, confirme a revisão de hardware exata na [Tabela de Hardware do OpenWrt](https://openwrt.org/toh/start) antes de instalar qualquer firmware. Um arquivo destinado a outra revisão pode inutilizar o roteador.

## Instalação pelo aplicativo

1. Conecte o celular e o aparelho que será monitorado à rede do OpenWrt.
2. No Toolkit Mobile, abra **OpenWrt** e toque em **Configurar roteador**.
3. Informe o endereço local do roteador, normalmente `192.168.1.1`, o usuário `root` e a senha administrativa.
4. Confira a identidade e a impressão digital SSH mostradas pelo aplicativo.
5. Aguarde a verificação do modelo, arquitetura, `nftables` e espaço livre.
6. Escolha o PC, PlayStation ou Xbox na lista de aparelhos encontrados.
7. Confirme a instalação e execute o teste de conexão.
8. Quando aparecer **Roteador conectado**, volte ao monitor e inicie a captura.

O Toolkit envia o agente compatível, cria um token exclusivo e acompanha o aparelho escolhido pelo endereço MAC. A senha administrativa não é salva. Nas conexões seguintes, o aplicativo usa apenas o token local.

## IP fixo do aparelho monitorado

Para evitar que o console ou PC receba outro endereço depois de reiniciar, crie uma reserva DHCP no OpenWrt:

1. abra **Rede → DHCP e DNS → Concessões estáticas**;
2. selecione o aparelho pelo MAC;
3. escolha um IPv4 livre dentro da rede LAN;
4. salve e aplique;
5. reconecte o aparelho à rede.

O assistente do Toolkit continua usando o MAC como identidade principal e atualiza o IP quando necessário.

## Modos de jogo

- **X1:** aplica o conjunto revisado para reduzir tentativas em faixas de servidor e preservar sessões diretas compatíveis.
- **COOP:** usa o conjunto próprio para partidas cooperativas e servidores dedicados.

As regras ficam restritas ao aparelho escolhido. Se o aplicativo perder contato com o roteador, o agente remove os filtros temporários automaticamente.

## Solução rápida de problemas

### O roteador não aparece

- confirme que celular e roteador estão na mesma rede;
- tente o IP da interface LAN do OpenWrt;
- confira se o SSH está ativo na porta 22;
- desligue temporariamente VPNs no celular durante a instalação.

### Arquitetura não suportada

Não tente instalar manualmente outro binário. Envie ao suporte o modelo, a revisão de hardware e o texto exibido pelo assistente.

### Espaço insuficiente

Remova pacotes que você instalou e não usa ou escolha um roteador com mais armazenamento. Não apague componentes essenciais do OpenWrt.

### O aparelho não aparece na lista

Ligue o PC ou console, conecte-o à rede do OpenWrt e atualize a lista. Se necessário, gere tráfego abrindo a loja ou um jogo online.

### IPv6 não funciona

Use o diagnóstico IPv6 do Toolkit. Ele verifica WAN, delegação de prefixo e distribuição na LAN antes de oferecer qualquer reparo.

## Segurança e privacidade

- a senha do OpenWrt é usada apenas durante a instalação e não é armazenada;
- o token de pareamento é individual e fica protegido no roteador e no dispositivo;
- o monitor observa somente o aparelho selecionado;
- nenhuma porta precisa ser encaminhada para a internet;
- reinstalar pelo assistente atualiza o agente quando o aplicativo contém uma versão mais nova.

Suporte: [efootballtoolkitpro.suporte@gmail.com](mailto:efootballtoolkitpro.suporte@gmail.com)

