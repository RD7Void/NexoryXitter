# Nexory Xitter

Painel para Windows x64 com interface ImGui, overlay Direct3D 11 e integração com Free Fire no BlueStacks.

Este repositório é o canal de **distribuição de releases**. Não contém o código-fonte do aplicativo.

## Download

**Versão 1.8.3.0** · [Baixar NexoryXitter-v1.8.3.0-Windows-x64.zip](https://github.com/RD7Void/NexoryXitter/releases/download/1.8.3.0/NexoryXitter-v1.8.3.0-Windows-x64.zip)

[Ver a release](https://github.com/RD7Void/NexoryXitter/releases/tag/1.8.3.0) · [Todas as versões](https://github.com/RD7Void/NexoryXitter/releases) · [Histórico de alterações](CHANGELOG.md)

## O que mudou

A versão 1.8.3.0 corrige a regressão que desativava a mira ao minimizar/esconder o menu. Esconder ou reabrir o menu preserva as funções ativadas e a conexão do worker Python. Somente encerrar o aplicativo desliga os controles contínuos, limpa o toggle SmartAim e solicita a parada do worker. Se a versão anterior salvou os switches desligados, reative as funções desejadas uma vez.

O ESP também passa a usar uma captura conjunta de câmera e entidades durante o frame visual. Amostras antigas deixam de ser desenhadas, e atualizações idênticas da geometria da janela são evitadas. Essas mudanças não representam garantia de atraso zero ou precisão de 100%.

## Recursos

| Área | Conteúdo |
| --- | --- |
| Interface | Tema escuro/claro, navegação inferior, controles ImGui e opções em português/inglês |
| ESP | Caixas, esqueleto, nome, distância, vida, linhas e ícones de armas |
| HUD | Radar, setas fora da tela, contador de alvos e alertas de proximidade |
| Mira | Controles e modos disponíveis no painel, com parada ao fechar/esconder o menu |
| Configurações | Conexão, perfis, hotkeys, conta, licença e seleção de dumps |
| Armas | 321 silhuetas brancas incorporadas e 157 IDs conhecidos associados a ícones |

O catálogo reúne 108 ícones HUD originais e 213 imagens transparentes convertidas em branco. As conversões preservam o alfa; cartões opacos com fundo/moldura ficaram fora da seleção. As imagens pertencem à Garena e aos respectivos titulares. O catálogo não identifica automaticamente a skin cosmética equipada.

## Como usar

1. Baixe o ZIP da release e extraia todos os arquivos para uma pasta.
2. Abra `NexoryXitter.exe` e conclua o login com uma licença válida.
3. Em **Config → Conexão**, selecione o processo/pacote e o perfil compatível com a instalação do jogo.
4. Em **ESP → Geral**, ajuste a visualização. Para os ícones, habilite **Exibir arma** e **Imagem da arma**.
5. Consulte a coleção em **Misc → Armas**.

A navegação principal reúne **Aimbot**, **ESP**, **Misc** e **Config**. As subseções dão acesso aos controles completos; `Ctrl+1…9` acessa as nove páginas originais. A tecla de abrir/esconder o menu é configurável nas preferências.

Esconder o menu mantém os controles ativados. Encerrar o aplicativo desliga os controles contínuos de mira. A restauração de alterações de memória depende de o processo do jogo continuar acessível.

## Requisitos e dados locais

- Windows x64 com suporte a Direct3D 11.
- BlueStacks e versão/arquitetura do jogo compatíveis com os perfis e offsets do painel. As leituras do motor atual esperam IL2CPP de 32 bits.
- Licença válida para autenticação.
- Python/OpenCV é opcional. Para usá-lo, configure Python 3.12 x64 no painel, mantenha a pasta `python` ao lado do executável e instale as dependências de `python/requirements.txt` no interpretador escolhido.

Preferências e dumps da variante ficam em `%LOCALAPPDATA%\Nexory\Alternative`. Os ícones são incorporados ao executável e não são baixados durante o uso.

## Verificação da versão

A release inclui `SHA256SUMS.txt`. Para conferir o executável extraído no PowerShell:

```powershell
Get-FileHash .\NexoryXitter.exe -Algorithm SHA256
```

Compare o resultado com a linha correspondente em `SHA256SUMS.txt`. Os hashes verificam a integridade dos arquivos; não substituem uma assinatura digital do publicador.

A compilação Release x64 e os testes locais de sincronização passaram. Login, funcionamento em partida, offsets da versão atual e restauração no emulador ainda não foram validados nesta entrega. **Config → Conexão** mostra a duração da leitura e a idade da amostra do ESP; isso não mede a latência total até o monitor.

## Suporte

Relate problemas em [Issues](https://github.com/RD7Void/NexoryXitter/issues), informando a versão do painel, a versão do jogo/emulador, o perfil selecionado e os passos para reproduzir. Não publique sua licença, credenciais ou arquivos privados nos relatos.
