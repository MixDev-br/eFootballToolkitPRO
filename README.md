# eFootball Toolkit PRO

Canal oficial de distribuição do eFootball Toolkit PRO para Windows.

Este repositório contém somente os pacotes prontos para uso. O código-fonte do aplicativo não é distribuído aqui.

## Download

Baixe sempre a versão mais recente pela página de [Releases](https://github.com/MixDev-br/eFootballToolkitPRO/releases/latest).

- [Baixar eFootball Toolkit PRO 2.0.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/v2.0.1/eFootball-Toolkit-PRO-v2.0.1.zip)
- [Baixar eFootball Toolkit TRIAL 2.0.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/trial-v2.0.1/eFootball-Toolkit-TRIAL-v2.0.1.zip)

Cada versão inclui:

- o pacote dinâmico `.zip` do aplicativo;
- um arquivo `.sha256` para conferência da integridade;
- as notas da versão.

## Instalação

1. Baixe o arquivo `eFootball-Toolkit-PRO-vX.X.zip`.
2. Extraia todo o conteúdo para uma pasta de sua preferência.
3. Não execute nem mova apenas o `.exe`: mantenha a pasta `runtime` junto dele.
4. Execute `eFootballToolkitPRO.exe` como administrador para utilizar os filtros temporários de firewall.

Compatível com eFootball para Steam e Xbox PC.

## Atualizações

O aplicativo consulta o manifesto assinado `update_manifest.json` deste repositório. Os pacotes continuam
sendo baixados exclusivamente pelas Releases e só são aceitos depois da validação de assinatura, tamanho e
SHA-256.

## Integridade do download

No PowerShell, execute:

```powershell
Get-FileHash -Algorithm SHA256 .\eFootball-Toolkit-PRO-v2.0.1.zip
```

Compare o resultado com o arquivo `.sha256.txt` publicado na mesma Release.

## Suporte

Em caso de problema, informe a versão do Toolkit, a plataforma do jogo e envie os registros apresentados pelo aplicativo para
[efootballtoolkitpro.suporte@gmail.com](mailto:efootballtoolkitpro.suporte@gmail.com).
