# Cadastro de participante

Exercício das páginas 15 e 16 da Aula 5 — Formulários e validação, do professor Arley.

Aplicação Flutter para web e Android com duas telas: cadastro e resumo do participante.

## Executar

Na pasta do projeto:

```bash
flutter pub get
flutter run -d chrome
```

Para Android, conecte um celular com depuração USB ou abra um emulador. Consulte os dispositivos e execute usando o identificador exibido:

```bash
flutter devices
flutter run -d ID_DO_DISPOSITIVO
```

## Funcionamento

Preencha e-mail, nome, telefone no formato `11-91234-5678` e CPF com 11 dígitos. O exercício não exige verificar os dígitos verificadores do CPF.

O botão **Exibir dados** valida os campos e abre o resumo. A ação de concluir no teclado do campo CPF faz o mesmo. **Voltar para editar** mantém o formulário preenchido. **Limpar** apaga os textos, remove as mensagens de erro e retira o foco.

## Código

O código está em `lib/main.dart`, seguindo a organização do exemplo da aula:

- `CadastroApp`: configuração do aplicativo e do tema.
- `Participante`: classe com os quatro atributos `final`.
- `TelaCadastro`: formulário, controladores e uma função de validação por campo.
- `TelaResumo`: recebe o participante pelo construtor e apresenta seus dados.

Foram utilizados os conteúdos das aulas: classes e funções Dart, widgets, `StatefulWidget`, controladores, `Navigator.push`/`pop`, `Form`, `TextFormField` e `GlobalKey<FormState>`. Não há pacotes adicionais nem persistência de dados.

## Verificação

```bash
flutter analyze
flutter build web
flutter build apk --debug
```
