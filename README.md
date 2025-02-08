# Coleta de Tweets por Localização (Brasil)

Este projeto utiliza a API do Twitter (via biblioteca Tweepy) para coletar tweets que mencionam o Brasil. Ele extrai informações como hashtags, nome de usuário, tipo de tweet, verificação do usuário e número de seguidores. Os dados são salvos em um arquivo pickle e posteriormente convertidos para um arquivo CSV para facilitar a análise.

## Pré-requisitos
Antes de executar o código, certifique-se de ter instalado as seguintes bibliotecas Python:

- `tweepy`
- `pandas`
- `pickle`

Você pode instalá-las usando o pip:

```bash
pip install tweepy pandas
```

## Configuração

### Obtenha credenciais da API do Twitter:
1. Crie uma conta de desenvolvedor no Twitter: [Twitter Developer](https://developer.twitter.com/).
2. Crie um aplicativo e obtenha as chaves de API: API Key, API Secret Key, Access Token e Access Token Secret.
3. Configure as credenciais substituindo as variáveis de autenticação no código com suas chaves da API do Twitter.

Exemplo:

```python
import tweepy

auth = tweepy.OAuth1UserHandler(
    "SUA_API_KEY",
    "SUA_API_SECRET_KEY",
    "SEU_ACCESS_TOKEN",
    "SEU_ACCESS_TOKEN_SECRET"
)
```

## Como Executar

Clone este repositório:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio
```

Execute o script Python:

```bash
python nome_do_script.py
```

O script realizará as seguintes etapas:
- Conectar-se à API do Twitter.
- Buscar tweets que mencionam o Brasil.
- Extrair informações relevantes (hashtags, nome de usuário, etc.).
- Salvar os dados em um arquivo pickle (`hashtag_data.pkl`).
- Converter os dados para um arquivo CSV (`hashtag_data.csv`).

### Download dos arquivos
Se estiver executando em um ambiente como o Google Colab, os arquivos `hashtag_data.pkl` e `hashtag_data.csv` serão baixados automaticamente. Caso contrário, os arquivos serão salvos no diretório local.

## Estrutura do Projeto

```
├── nome_do_script.py       # Código principal para coleta e processamento dos tweets
├── hashtag_data.pkl        # Arquivo pickle gerado com os dados coletados
├── hashtag_data.csv        # Arquivo CSV gerado a partir do pickle para análise
├── README.md               # Instruções sobre o projeto
```

## Exemplo de Saída
O arquivo CSV (`hashtag_data.csv`) terá a seguinte estrutura:

| user       | tweet_type | verified | followers | hashtags              |
|------------|-----------|----------|-----------|------------------------|
| joaosilva  | mixed     | True     | 1500      | [#Python, #Data]       |
| maria123   | recent    | False    | 300       | [#Brasil]              |
| techguru   | popular   | True     | 50000     | [#Tech, #Inovação]    |

Este projeto permite coletar tweets e analisar as tendências relacionadas ao Brasil, facilitando estudos e pesquisas sobre o que está sendo discutido na plataforma.

