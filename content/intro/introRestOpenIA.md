# Leiningen  <img align="right" src="https://github.com/MorpphAI/platform.Morph/blob/main/content/images/morphTrans.png" alt="Imagem da linguagem" width="60">

# 📚 Documentação da API 

## Índice
1. [Autenticação](#autenticação)
2. [Enviar Mensagens para o Agente](#enviar-mensagens-para-o-agente)
3. [Gerenciamento de Arquivos](#gerenciamento-de-arquivos)
4. [Listar e Excluir Arquivos](#listar-e-excluir-arquivos)

## 1. Autenticação

Todas as requisições à API devem ser autenticadas usando uma chave de API. A chave deve ser passada no cabeçalho `Authorization`.

**Cabeçalhos obrigatórios**:
```http
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```
<br/>
<br/>

## 2.  Enviar Mensagens para o Agente
### Este endpoint permite enviar mensagens para o modelo GPT e obter respostas.

#### Retorna um item

```http
  POST https://api.openai.com/v1/chat/completions
```
<br/>

| Parâmetro     | Tipo       | Obrigatório | Descrição                                      |
|---------------|------------|-------------|-----------------------------------------------|
| `model`       | string     | Sim         | Modelo a ser usado. Exemplo: `gpt-4` ou `gpt-3.5-turbo`. |
| `messages`    | array      | Sim         | Histórico de mensagens, incluindo a nova mensagem. |
| `temperature` | float      | Não         | Controla a criatividade da resposta (0.0 a 1.0). Padrão: `0.7`. |
| `max_tokens`  | integer    | Não         | Número máximo de tokens na resposta. Padrão: `256`. |

<br/>
<br/>
### 3. Gerenciamento de Arquivos

Este endpoint permite enviar arquivos para a API. Ele é comumente usado para fine-tuning ou outras aplicações que dependem de dados externos.

#### Endpoint:
```http
  POST https://api.openai.com/v1/files
```


<p align="right">
  <a href="https://github.com/Juniorbasck/astro4noobs/blob/main/content/intro/instalacao.md">Próximo -> Instalação</a>
</p>

<p align="left">
  <a href="https://github.com/MorpphAI/platform.Morph">Voltar para o menu principal</a>
</p>
