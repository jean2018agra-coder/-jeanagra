# Reinos Místicos — gerar o APK

Você não precisa instalar Android Studio. O GitHub compila o APK de graça.

## Passo a passo
1. Crie uma conta em https://github.com (se não tiver).
2. Crie um repositório novo (pode ser privado), por exemplo `reinos-misticos`.
3. Envie TODO o conteúdo desta pasta para o repositório
   (botão "Add file" > "Upload files"; inclua a pasta `.github`).
   Dica: pastas que começam com ponto podem ficar ocultas no seu sistema;
   se não conseguir enviar `.github`, crie o arquivo pelo site:
   "Add file" > "Create new file" e digite `.github/workflows/build-apk.yml`,
   colando o conteúdo do arquivo de mesmo nome.
4. Abra a aba **Actions**, escolha **Gerar APK** e clique em **Run workflow**.
5. Espere uns 5 a 8 minutos. Abra a execução concluída e baixe
   **ReinosMisticos-APK** em "Artifacts" (vem num .zip com o `app-debug.apk`).
6. Passe o APK para o celular, abra e permita "instalar apps de fontes desconhecidas".

## Atualizar o jogo
Troque o arquivo `www/index.html` pela versão nova e rode o workflow de novo.

## Observações
- O jogo roda 100% offline; o progresso é salvo no próprio app.
- O app abre deitado e em tela cheia.
- O ícone e a tela de abertura vêm da pasta `assets/` (icon-only, icon-foreground, icon-background, splash). Para trocar o ícone, substitua esses PNGs (1024x1024; o foreground deve ficar dentro da área central).
- O APK é de teste (debug): serve para instalar no seu celular e de amigos.
  Para publicar na Play Store é preciso gerar um APK/AAB assinado.
