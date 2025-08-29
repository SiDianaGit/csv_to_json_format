# csv_to_json_format
A Python project to convert csv files (UTF-8) delimited by ";" to .json format

# Conversor de CSV para JSON
Uma ferramenta simples e eficiente para converter arquivos CSV, que utilizam ponto e vírgula como separador e são codificados em UTF-8, para o formato de dados JSON.

Este projeto foi criado como um template de pacote Python para demonstrar o processo de empacotamento e publicação no **PyPI** utilizando o **Twine**.

## Funcionalidades
- Converte um arquivo CSV para uma lista de objetos JSON.
- Suporta arquivos CSV com cabeçalho e codificação UTF-8.
- Utiliza ponto e vírgula (`;`) como delimitador de colunas.

## Instalação

Você pode instalar a biblioteca diretamente do PyPI (após sua publicação) usando `pip`:

Para testes:
```
pip install -i https://test.pypi.org/simple/ csv-to-json-format
```

Para produção

```bash
pip install -i https://pypi.org/simple/ csv-to-json-format
```


## Exemplo de Código

Para usar o conversor, importe a função convert_csv_to_json de dentro do seu pacote e chame-a com os caminhos dos arquivos de entrada e saída.

´´´
from convert_format.csv_to_json import csv_to_json
´´´

### Defina os caminhos para o seu arquivo CSV de entrada e JSON de saída
input_csv = 'dados_de_exemplo.csv'
output_json = 'dados_convertidos.json'

### Chame a função para realizar a conversão
´´´
csv_to_json.convert_csv_to_json(input_csv, output_json)
´´
 Se a conversão for bem-sucedida, você verá uma mensagem de confirmação
 "Conversão concluída! O arquivo JSON foi salvo em: dados_convertidos.json"

### Exemplo de Arquivos
Aqui está como um arquivo de entrada e saída se pareceriam.


#### CSV de entrada (dados_de_exemplo.csv):

Fragmento do código


nome;idade;cidade

Ana;28;São Paulo

Carlos;35;Rio de Janeiro




#### JSON de saída (dados_convertidos.json):

JSON

[
    {
        "nome": "Ana",
        "idade": 28,
        "cidade": "São Paulo"
    },
    {
        "nome": "Carlos",
        "idade": 35,
        "cidade": "Rio de Janeiro"
    }
]

### Estrutura do Projeto
A estrutura de arquivos segue o padrão recomendado para pacotes Python, conforme a imagem de referência.

csv_to_json_format/
├── README.md
├── setup.py
├── requirements.txt
├── convert_format/
│   ├── __init__.py
│   ├── csv_to_json
│   │   ├── __init__.py
│   │   ├── csv_to_json.py
│   └── convert_main/
│       ├── __init__.py
│       └── main.py

Contribuição
Sinta-se à vontade para abrir issues ou pull requests se você tiver sugestões ou encontrar problemas.
