# Água! — PWA de hidratação

## Publicar no GitHub Pages
1. Crie um repositório público, por exemplo `agua-lembrete`.
2. Envie os quatro arquivos `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg` para a raiz.
3. Abra **Settings → Pages → Build and deployment → Deploy from a branch**, selecione `main` e `/ (root)` e salve.
4. Abra a URL do Pages em HTTPS no celular e instale pela opção de adicionar à tela inicial.

## Limitação importante
Este PWA em HTML funciona como lembrete insistente **enquanto está aberto/ativo**. JavaScript e service workers não oferecem agendamento confiável de alarmes locais quando o app está fechado ou suspenso. Para alarmes em segundo plano, é preciso construir um aplicativo Android nativo com permissões de alarme/notificações, ou integrar um backend que envie Web Push (com limitações do iOS/Android). Não bloqueia outros apps nem a tela do celular.

As informações são armazenadas somente no navegador do dispositivo (localStorage). Não há sincronização entre aparelhos. O teste de alarme funciona mesmo fora da janela de horários após ativar; alertas regulares respeitam o horário definido.
