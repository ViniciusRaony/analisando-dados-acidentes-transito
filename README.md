# Analisando acidentes de trânsito no Brasil

Acidentes de trânsito são uma grande preocupação no Brasil e representam um problema de saúde pública, além de causar prejuízos econômicos e sociais. Dados públicos mostram que a maioria dos acidentes de trânsito ocorre em áreas urbanas, envolvendo veículos de passeio e motocicletas.

A análise dos dados de acidentes de trânsito no Brasil entre 2017 e 2022 pode fornecer insights valiosos sobre as causas, locais e fatores de risco desses incidentes, permitindo que as autoridades de trânsito tomem medidas preventivas e mitigatórias.

<center><img alt="Colaboratory logo" width="50%" src="https://raw.githubusercontent.com/ViniciusRaony/analisando-dados-acidentes-transito/main/images/acidente-carro1.jpg"></center>

No entanto, a disponibilidade e a qualidade dos dados de acidentes de trânsito no Brasil ainda são limitadas, o que pode dificultar a análise e a interpretação dos resultados.

Com o objetivo de contribuir para o debate sobre a segurança viária no país, esta análise explorará os dados disponíveis e buscará identificar tendências e padrões relevantes.

**Neste *notebook*, irei analisar os dados referentes à todos os Estados do Brasil, e ver quais insights podem ser extraídos a partir de dados brutos.**

## Obtenção dos Dados

Todos os dados usados aqui foram obtidos a partir do site do Governo Federal Brasileiro de acordo com o Plano de Dados Abertos da PRF, que consta [neste meu link](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos). 

Vale ressaltar que as informações sensíveis estão devidamente anonimizadas nos arquivos fornecidos.

Para esta análise exploratória inicial, seão baixados os arquivos *Agrupados por pessoa dos anos de* : 2017, 2018, 2019, 2020, 2021 e 2022.

## Análise Exploratória dos Dados - Informações

- O tratamento de dados foi realizado em Python e consta no arquivo .ipynb desse repositório;
- Os dados processados foram armazenados no banco mysql executado em container docker conectados ao Superset;
- O dashboard foi elaborado utilizando o Superset (versão docker https://superset.apache.org/docs/installation/installing-superset-using-docker-compose/)

**Dicionário das variáveis**

* `id` - número de id gerado para identificar o acidente
* `data_inversa` - data que ocorreu o acidente
* `dia_semana` - dia da semana que ocorreu o acidente
* `horario` - horário do acidente
* `uf` - Estado em que ocorreu o acidente
* `br` - rodovia Federal em que ocorreu o acidente
* `km` - kilometragem da BR onde onde ocorreu o acidente
* `municipio`municipio - município em que ocorreu o acidente
* `causa_acidente` - causa do acidente
* `tipo_acidente` - colisão frontal, traseira
* `classificacao_acidente` - se houve ou não vítimas fatais
* `fase_dia` - qual período do dia ocorreu o acidente
* `sentido_via` - crescente é mão única e decrescente é mão dupla
* `condicao_metereologica` - condição meteorológica na hora do acidente
* `tipo_pista` - pista possui mais de uma faixa para a trafegabilidade?
* `tracado_via` - acidente ocorreu numa reta ou curva?
* `id_veiculo` - número de id gerado para identificar o automóvel envolvido no acidente
* `tipo_veiculo` - tipo de veículo envolvido no acidente
* `marca` - marca do veículo envolvido no acidente 
* `ano_fabricacao_veiculo` - ano de fabricação do veículo envolvido no acidente
* `tipo_envolvido` - sujeito envolvido no acidente: Condutor, Passageiro ou Testemunha
* `estado_fisico` - grau de ferimentos no acidente
* `idade` - idade do indivíduo envolvido no acidente
* `sexo` - sexo dos envolvidos no acidente
* `ilesos` - quantidade de pessoas que saíram ilesas do acidente
* `feridos_leves` - quantidade de pessoas que saíram ferimentos leves do acidente
* `feridos_graves` - quantidade de pessoas que saíram ferimentos graves do acidente
* `mortos` - quantidade de pessoas que viéram a óbito no acidente
* `latitude` - coordenada da latitude do acidente
* `longitude` - coordenada da longitude do acidente
* `regional` - superitendência da PRF responsável
* `delegacia` - delegacia da PRF responsável
* `uop` - orgão federativo responsável

<center><img alt="Colaboratory logo" width="100%" src="https://raw.githubusercontent.com/ViniciusRaony/analisando-dados-acidentes-transito/main/images/Superset-dashboard-prf2017-2022.jpg"></center>

## TODO ##
Elaborar material detalhado dos insights em versão-web
