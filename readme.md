# Pesquisa Culturama

Este projeto consiste em um sistema de formulário web para **Pesquisa de Opinião**, desenvolvido com foco em acessibilidade, semântica estrutural e validação de dados coletados dos usuários.

## 🚀 Funcionalidades

O projeto é composto por uma interface de formulário dividida semanticamente nas seguintes seções:
* **Dados Pessoais:** Captura de informações como nome, idade, data de nascimento, e-mail, telefone (com máscara de validação) e upload de imagem de perfil.
* **Perfil:** Coleta de gênero, estado civil, estado (abrangendo as 27 unidades federativas do Brasil) e cidade.
* **Hábitos:** Seleção múltipla de redes sociais utilizadas, campo de estilo musical sugerido via `datalist` e seletor de cor favorita.
* **Opinião:** Avaliação em escala de rádio sobre a qualidade dos serviços prestados e um espaço textual para comentários adicionais.
* **Confirmações:** Termos de consentimento para participação na pesquisa e opção de recebimento do resultado por e-mail.

O fluxo de envio direciona o usuário para uma página de confirmação (`sucesso.html`) que utiliza propriedades de acessibilidade digital para alertar o sucesso do envio aos leitores de tela.

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Utilização de tags semânticas avançadas (`<fieldset>`, `<legend>`, `<datalist>`) e atributos nativos de validação (`required`, `pattern`, `min`, `max`).
* **CSS3:** Estilização externa customizada (arquivo localizado em `css/style.css`).
* **Google Fonts:** Tipografia importada utilizando as fontes *Fjalla One* e *Work Sans*.

## ♿ Acessibilidade e Validação

O formulário foi projetado seguindo boas práticas de desenvolvimento web:
* **Atributos ARIA:** Uso de `aria-describedby` para associar instruções de preenchimento nos campos de telefone e upload de imagem, além de `aria-label` nos botões de ação.
* **Mapeamento de Mensagens:** A página de sucesso utiliza o atributo `role="alert"` para que tecnologias assistivas priorizem a leitura do status positivo ao usuário.
* **Regras de Validação:** Limitação de idade (entre 12 e 100 anos) e expressão regular estrita para o número de telefone com 11 dígitos numéricos contínuos.