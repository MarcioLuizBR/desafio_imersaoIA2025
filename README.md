# HELPTEA - Ajuda para Transtornos do Espectro Autista

Este projeto foi desenvolvido como parte da Imersão IA 2025 promovida pela Alura em parceria com o Google. O objetivo é utilizar a API do Google Gemini e os conceitos apresentados nas aulas para construir um sistema de assistência interativa para familiares de pessoas com TEA (Transtorno do Espectro Autista).

## Objetivo

Criar uma aplicação que, a partir de uma pergunta inicial do usuário sobre qualquer tema relacionado ao TEA, obtenha respostas de especialistas virtuais de diversas áreas (assistência social, direito, educação, nutrição e psicologia) e consolide essas respostas de maneira clara e empática por meio de um redator final.

## Tecnologias Utilizadas

* Google Colab (execução do código Python)
* Google Generative AI (Gemini)
* Biblioteca `google-adk` para construção e execução de agentes
* `google_search` como ferramenta auxiliar nos agentes

## Fluxo de Execução

1. O usuário insere uma pergunta ou tema livre relacionado a TEA (ex: "seletividade alimentar").
2. Cada agente responde com base na sua área de especialidade:

   * **Assistente Social**: aspectos de serviços e benefícios públicos
   * **Jurídico**: direitos legais e legislações relevantes
   * **Educacional**: adaptações e apoio pedagógico
   * **Nutricionista**: aspectos relacionados à alimentação
   * **Psicólogo**: apoio emocional e comportamental
3. O agente **Redator Final** consolida todas as respostas em um único texto amigável e resumido.

## Como Executar

1. Acesse o Google Colab
2. Carregue o arquivo `projeto_imersaoIA2025.ipynb`
3. Insira sua chave da API do Google no Colab:

   ```python
   os.environ["GOOGLE_API_KEY"] = userdata.get('GOOGLE_API_KEY')
   ```
4. Execute todas as células para instalar os pacotes e inicializar os agentes
5. Utilize a função `resposta_final_pergunta(pergunta)` para testar seu tema

## Exemplo de Uso

```python
pergunta = "Como lidar com seletividade alimentar em crianças autistas?"
resposta_final_pergunta(pergunta)
```

## Estrutura do Projeto

* **build\_agents()**: Cria e configura os agentes com instruções e ferramentas
* **call\_agent()**: Envia uma pergunta e recebe a resposta de um agente
* **resposta\_final\_pergunta()**: Função principal que coordena o fluxo
* **to\_markdown()**: Formata a saída no Colab

## Autor

Este projeto foi idealizado e implementado por \[Seu Nome Aqui] durante a Imersão IA 2025 (Alura + Google).

## Licença

Este projeto é de uso educacional e sem fins lucrativos, com intuito de estudo, demonstração de aplicação de IA generativa e apoio à comunidade TEA.

---

Caso deseje expandir o projeto futuramente, considere incluir:

* Geolocalização para busca de ONGs e recursos na cidade informada
* Interface via Streamlit ou app
* Armazenamento de histórico de perguntas e respostas
