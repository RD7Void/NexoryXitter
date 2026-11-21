# Histórico de versões

## 1.8.1.0 — 21/11/2026

- Interface ImGui alternativa com navegação inferior e acesso às funções do painel.
- Catálogo com 321 silhuetas brancas: 108 ícones HUD e 213 PNGs transparentes convertidos, com alfa preservado.
- Publicação conjunta de câmera e entidades para o desenho do ESP, radar, setas e proximidade.
- Rejeição de amostras visuais com mais de 100 ms e validação de coordenadas de projeção.
- Correção da parada dos controles de mira ao fechar a janela ou esconder o menu: desativa os modos contínuos, limpa o toggle SmartAim e solicita o encerramento do worker Python/OpenCV.
- Reabrir o menu exige reativar manualmente as funções desligadas.

Build Release x64 e testes locais de sincronização aprovados. Login, restauração de alterações de memória e funcionamento em partida não foram validados nesta versão. A restauração depende de o jogo continuar acessível.
