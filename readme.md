# Análise de Correlações e Defasagens

Este repositório contém o código utilizado para realizar a análise de correlações e defasagens entre variáveis econômicas, como PIB, SELIC e outros indicadores relevantes. A análise foi realizada utilizando Python, com dados obtidos diretamente das APIs do Banco Central do Brasil e do IBGE.

Confira a análise completa: [Análise de Correlações e Defasagens](https://udata.dev/analise-de-correlacoes-e-defasagens/)

## Requisitos

Para executar este projeto, você precisará de:

- Python 3.9 ou superior
- [Pipenv](https://pipenv.pypa.io/en/latest/) para gerenciar dependências
- Conexão com a internet para acessar as APIs do Banco Central e do IBGE

## Instalação

1. Clone este repositório:
   ```
   git clone https://github.com/G-Cintra/udata-observatorio.git
   cd udata-observatorio
   ```
2. Configure o ambiente virtual com pipenv:
   
   ```
   pipenv install
   ```

3. Ative o ambiente virtual:
   ```
    pipenv shell
   ```

## Uso

1. Certifique-se de que todas as dependências estão instaladas e o ambiente virtual está ativado.

2. Todo o código está disponível no arquivo notebook.ipynb

## Estrutura do Repositório

- **`notebook.ipynb`**: Arquivo principal que executa a análise.
- **`dados/`**: Diretório onde os arquivos de dados são armazenados.
- **`imagens/`**: Diretório onde os gráficos gerados serão salvos.
- **`merged_data.csv`**: Dados trimestrais para todas as sérias abordadas no período de 2012 a 2024.
- **`dados_alterados.log`**: Registro dos dados que foram alterados. Como os indicadores possuem frequências de amostragem distintas, foi necessário harmonizar os dados para padronizar os períodos analisados. Para isso, nas séries em que o dado referente ao primeiro dia do trimestre não estava disponível, foi utilizado o valor mais próximo dentro do mesmo trimestre. Essa abordagem permite uma análise consistente das interrelações entre os indicadores ao longo do tempo.
- **`dados/processados/`**: Contém os dados os dados originais após as alterações registradas no arquivo `dados_alterados.log`.
- **`Pipfile` e `Pipfile.lock`**: Arquivos de configuração do Pipenv para gerenciar dependências.

## Dependências

As principais dependências do projeto incluem:

- **`pandas`**: Para manipulação de dados.
- **`seaborn`**: Para geração de gráficos.
- **`matplotlib`**: Para suporte gráfico adicional.
- **`requests`**: Para acessar as APIs.

As dependências completas estão especificadas no arquivo `Pipfile`.

## Sobre a Análise

A análise utiliza dados das seguintes fontes:

- **Banco Central do Brasil**: Séries temporais de taxas de juros, spreads, inadimplência, entre outros.
- **IBGE**: Dados do PIB e IPCA.

O período analisado vai de 2012 a 2024, com ajustes para harmonizar as séries temporais de diferentes frequências.

Confira a análise completa em: [Análise de Correlações e Defasagens](https://udata.dev/analise-de-correlacoes-e-defasagens/)

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests com sugestões, correções ou melhorias.

## Licença

Este projeto está licenciado sob a [GNU GPLv3](LICENSE).