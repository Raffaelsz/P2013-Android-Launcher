# PES 2013 Android Launcher — protótipo 0.1.0

Este é um projeto inicial de launcher Android em Kotlin. Ele inclui:
- interface inicial;
- seleção persistente da pasta do jogo pelo seletor oficial do Android;
- verificação básica de `pes2013.exe` e `img`;
- seleção e armazenamento de perfis de desempenho;
- aviso honesto de que o runtime ainda não está integrado.

## Limitação importante
Este projeto **não executa o PES 2013 ainda**. Um launcher não executa um binário Windows por conta própria. Para isso, é necessário integrar um runtime de compatibilidade com suporte ao jogo x86 de 32 bits e uma camada de tradução gráfica compatível com o dispositivo. Essa integração exige trabalho nativo adicional e testes reais.

Use apenas arquivos de jogo que você tenha direito de utilizar. Este projeto não inclui o jogo, executáveis do PES, DLLs proprietárias ou runtime de terceiros.

## Abrir/compilar
Abra a pasta do projeto em um ambiente Android com suporte a Gradle e Android SDK. O projeto usa:
- Android Gradle Plugin 8.7.3
- Kotlin 2.0.21
- compileSdk 35
- minSdk 26

No celular, a compilação pode exigir uma IDE Android compatível e espaço suficiente para baixar Gradle/SDK. AndroidIDE/AIDE podem não suportar todas as versões do plugin ou a configuração exata; se houver erro, envie o texto ou uma captura de tela para adaptar o projeto.

## Próximas etapas
1. Compilar e testar a interface.
2. Melhorar validação de pastas e permissões.
3. Pesquisar a integração técnica do runtime.
4. Implementar controles e parâmetros realmente aceitos pelo runtime.

## Compilação automática pelo GitHub Actions
O projeto inclui `.github/workflows/android.yml`. Para compilar na nuvem:
1. Crie um repositório no GitHub.
2. Envie os arquivos e pastas deste projeto para a raiz do repositório (incluindo `.github/workflows/android.yml`).
3. Abra a aba **Actions**, selecione **Build PES 2013 Android Launcher APK** e toque em **Run workflow** (ou aguarde o build após enviar para `main`).
4. Abra a execução concluída e baixe o artefato `PES2013-Android-Launcher-debug`. Dentro dele estará `app-debug.apk`.

O APK gerado por esse fluxo é uma versão de depuração do launcher. Ele ainda não inclui runtime Windows nem executa o PES 2013.
