# EasyBank

Aplicativo Android do EasyBank, construído com [Capacitor](https://capacitorjs.com/) e configurado para carregar a aplicação web do projeto em um WebView nativo.

> **Status atual:** este repositório contém a estrutura Android extraída e um APK de debug. O código-fonte completo da aplicação web não está incluído no repositório neste momento. O aplicativo Android está configurado para abrir a aplicação hospedada em `https://archive-spark-migrator.lovable.app/entrar`.

O conteúdo do projeto Android está disponível diretamente nas pastas `android/` e `node_modules/`, para facilitar a inspeção e a compilação.

## Sobre o aplicativo

O EasyBank é um protótipo de banco digital criado para oferecer uma experiência simples, moderna e sem burocracia. A interface utiliza principalmente tons de rosa, branco e cinza escuro, com navegação por ações rápidas e mensagens visuais de sucesso ou erro.

O aplicativo demonstrado inclui autenticação por CPF e senha, criação de conta, consulta de saldo, Pix, transferências, cartão de crédito, caixinhas de objetivos financeiros, recargas, cobranças e extrato. A demonstração também apresenta recursos de validação e atualização do saldo após as operações.

## Funcionalidades demonstradas

### Login e criação de conta

- Tela de boas-vindas com a identidade visual do EasyBank e o slogan “Seu banco seguro, simples & sem burocracia ;)”.
- Login utilizando CPF e senha.
- Opções para entrar com segurança, recuperar a senha e criar uma conta.
- Cadastro com nome completo, CPF, e-mail e senha.
- Indicadores visuais de segurança, como dispositivo verificado e criptografia de ponta a ponta.

### Dashboard

A tela inicial apresenta uma saudação personalizada, dados de agência e conta, saldo disponível e acesso ao extrato. O valor do saldo pode ser ocultado pelo ícone de visualização.

Também são exibidas ações rápidas para Pix, pagamentos, transferências, cartões, cobranças, caixinhas, recargas e extrato. A tela inclui um resumo do cartão, com o valor da fatura atual, além de uma lista das atividades mais recentes.

### Pix

O fluxo de Pix permite pagar por QR Code ou informar uma chave manualmente, como CPF ou e-mail. Quando o QR Code é utilizado, o aplicativo acessa a câmera para realizar a leitura e preencher os dados do pagamento.

Também é possível receber ou cobrar por meio da geração de QR Code estático ou dinâmico, com valor definido pelo usuário, além de consultar as chaves cadastradas.

### Transferências e extrato

O aplicativo possui transferência convencional com preenchimento de agência, conta de destino e valor. O extrato apresenta as movimentações recentes, incluindo transferências enviadas e recebidas e outros lançamentos exibidos durante a demonstração.

### Cartão de crédito

Na área de cartões, o usuário pode consultar a fatura atual e o limite disponível, acessar o cartão virtual e registrar uma nova compra para simulação de gastos. O limite é atualizado na interface após o registro da compra.

O pagamento da fatura aceita um valor parcial ou total utilizando o saldo da conta. A demonstração apresenta uma validação para impedir pagamentos acima do valor da fatura, exibindo a mensagem “Valor maior que a fatura”. O cartão virtual também é apresentado como opção para compras online e pagamentos por aproximação.

### Caixinhas

As caixinhas permitem organizar dinheiro por objetivos financeiros, como uma viagem. O usuário pode criar uma caixinha informando seu nome e sua meta, guardar dinheiro a partir do saldo principal, resgatar o valor para a conta e excluir a caixinha.

Quando o valor a guardar é maior que o saldo disponível, o aplicativo apresenta a mensagem “Saldo insuficiente”.

### Outras áreas

A demonstração também apresenta atalhos para recarga, cobrança e cartão. O saldo inicial e os valores exibidos no vídeo são dados de demonstração e não representam uma conta bancária real.

## Conteúdo do repositório

- `android/`: projeto Android/Capacitor extraído e pronto para inspeção.
- `node_modules/`: dependências Android do Capacitor incluídas no projeto.
- `app-debug.apk`: APK de desenvolvimento para instalação e testes em dispositivos Android.
- `Readme.md`: documentação do projeto.

## Estrutura do projeto Android

O projeto Android disponível na pasta `android/` possui:

- Módulo principal `app`.
- Activity principal em Java (`MainActivity`), baseada em `BridgeActivity` do Capacitor.
- Configuração do aplicativo em `capacitor.config.json`.
- Recursos nativos, como ícones, tema, layout inicial e `FileProvider`.
- Testes unitários e testes instrumentados de exemplo.
- Gradle Wrapper para facilitar a compilação sem depender de uma instalação global do Gradle.
- Dependências AndroidX e Capacitor Android.

## Informações do projeto

- **Plataforma:** Android.
- **Framework de integração:** Capacitor.
- **Linguagem nativa:** Java.
- **Build:** Gradle e Android Gradle Plugin `8.7.2`.
- **Namespace e application ID:** `com.easybank.app`.
- **Nome do aplicativo:** Easy Bank.
- **SDK mínimo:** 23.
- **SDK de compilação:** 35.
- **SDK de destino:** 35.
- **Versão atual:** `1.0`, código de versão `1`.

A configuração do Capacitor utiliza fundo `#FFF5F7` e permite navegação para o domínio da aplicação web hospedada e para subdomínios `lovable.cloud`.

## Permissões declaradas

O aplicativo declara as seguintes permissões no Android:

- `INTERNET`, para carregar a aplicação web remota.
- `CAMERA`, com o recurso de câmera definido como opcional.

A necessidade real dessas permissões depende das funcionalidades implementadas na aplicação web conectada ao aplicativo.

## Como instalar o APK

1. Baixe o arquivo [`app-debug.apk`](./app-debug.apk).
2. Transfira o arquivo para um dispositivo Android ou use um emulador.
3. Permita a instalação de aplicativos de fontes desconhecidas, se necessário.
4. Instale o APK e abra o aplicativo **Easy Bank**.

O APK é uma versão de debug e deve ser utilizado principalmente para testes. Para distribuição em produção, recomenda-se gerar uma versão assinada (`release`).

## Como compilar o projeto

Depois de clonar o repositório, entre na pasta `android` e execute:

```bash
cd android
./gradlew assembleDebug
```

No Windows, use:

```powershell
cd android
.\gradlew.bat assembleDebug
```

O APK gerado normalmente ficará em:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

## Aplicação web

O Android funciona como um contêiner nativo para a aplicação web. A URL atualmente configurada é:

```text
https://archive-spark-migrator.lovable.app/entrar
```

O arquivo `index.html` presente nos assets Android contém apenas uma mensagem de carregamento. Portanto, a interface e as regras de negócio dependem da aplicação web remota e não estão completas dentro deste repositório.

## Observações

- O APK disponível é de desenvolvimento (`debug`).
- O projeto depende de conexão com a internet para carregar a aplicação web configurada.
- Alterações no endereço da aplicação web devem ser feitas em `android/app/src/main/assets/capacitor.config.json` e exigem uma nova compilação do APK.
- Não foram identificados, no conteúdo atual do repositório, código de backend, banco de dados, autenticação nativa ou implementação local de operações bancárias.
- A descrição das funcionalidades acima foi baseada na demonstração em vídeo enviada para este projeto. Como o código-fonte web completo não está presente no repositório, alguns detalhes de implementação e integrações não puderam ser confirmados diretamente.
- O vídeo indica um protótipo/MVP para demonstração. Entre as limitações observáveis estão validações ainda simples e, em algumas telas, a possibilidade de o teclado numérico sobrepor parte da interface.
- O aplicativo não deve ser tratado como uma instituição financeira ou utilizado para movimentações reais sem uma revisão completa de segurança, backend, autenticação, armazenamento e conformidade.

## Licença

Nenhuma licença foi informada neste repositório até o momento.
