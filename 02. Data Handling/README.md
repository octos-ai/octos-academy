# Handling Tabular Data

Pessoal, a nossa ideia não é lançar uma lista de tutoriais/aulas para seguirem. Por maior que seja a dedicação, sabemos que no fim das contas não se retém o conteúdo.

Por isso, disponibilizamos uma lista de exercícios acompanhada de [materiais de referência](https://jakevdp.github.io/PythonDataScienceHandbook/03.00-introduction-to-pandas.html) que devem ser consultados conforme progredirem e acharem necessário. A referência que linkamos é uma que acreditamos ser particularmente boa: clara e objetiva, com código disponível no Google Colab.
Lembrem-se: o mais importante é aprender, não ser rápido!

PS: Esse material não é nosso! Encontramos na internet durante nosso busca para montar o curso. Temos que tirar o chapéu para o autor.

## Requirements

    - numpy==1.13.3
    - matplotlib==2.0.2
    - seaborn==0.8.1
    - pandas==1.0.4

Crie um novo environment com todos os requerimentos necessários a partir do seguinte comando:

    conda create -name <ENV_NAME> -file requirements.txt

Depois de configurar o novo enviromnment, para ative o usando (windows)

    activate <ENV_NAME>

ou se você está em uma máquina linux

    source activate <ENV_NAME>

Agora já pode começar a trabalhar nos exercícios. Basta navegar até o diretório aonde estão localizados os exercícios e e lançar o jupyter notebook a partir do terminal usando o comando

    jupyter notebook

Alternativamente, use o [Google Colab](https://colab.research.google.com). Nele você não precisará instalar nada além de poder acessar de qualquer lugar! Basta fazer o upload do seu jupyter notebook ou então entrar diretamente com a URL do jupyter nesse repositório. Por outro lado, pode precisar fazer o upload de alguns dos materiais disponibilizados como os datasets.

## Lessons

|                                                 |                                                                   |                             |
| :---------------------------------------------: | :---------------------------------------------------------------: | :-------------------------: |
|   [Getting and knowing](#getting-and-knowing)   |                          [Merge](#merge)                          | [Time Series](#time-series) |
| [Filtering and Sorting](#filtering-and-sorting) |                          [Stats](#stats)                          |    [Deleting](#deleting)    |
|              [Grouping](#grouping)              |                  [Visualization](#visualization)                  |          Indexing           |
|                 [Apply](#apply)                 | [Creating Series and DataFrames](#creating-series-and-dataframes) |          Exporting          |

### [Getting and knowing](Exercises/01_Getting_%26_Knowing_Your_Data)

[Chipotle](Exercises/01_Getting_%26_Knowing_Your_Data/Chipotle)
[Occupation](Exercises/01_Getting_%26_Knowing_Your_Data/Occupation)
[World Food Facts](Exercises/01_Getting_%26_Knowing_Your_Data/World%20Food%20Facts)

### [Filtering and Sorting](Exercises/02_Filtering_%26_Sorting)

[Chipotle](Exercises/02_Filtering_%26_Sorting/Chipotle)
[Euro12](Exercises/02_Filtering_%26_Sorting/Euro12)
[Fictional Army](Exercises/02_Filtering_%26_Sorting/Fictional%20Army)

### [Grouping](Exercises/03_Grouping)

[Alcohol Consumption](Exercises/03_Grouping/Alcohol_Consumption)
[Occupation](Exercises/03_Grouping/Occupation)
[Regiment](Exercises/03_Grouping/Regiment)

### [Apply](Exercises/04_Apply)

[Students Alcohol Consumption](Exercises/04_Apply/Students_Alcohol_Consumption)
[US_Crime_Rates](Exercises/04_Apply/US_Crime_Rates)

### [Merge](Exercises/05_Merge)

[Auto_MPG](Exercises/05_Merge/Auto_MPG)
[Fictitious Names](Exercises/05_Merge/Fictitous%20Names)
[House Market](Exercises/05_Merge/Housing%20Market)

### [Stats](Exercises/06_Stats)

[US_Baby_Names](Exercises/06_Stats/US_Baby_Names)
[Wind_Stats](Exercises/06_Stats/Wind_Stats)

### [Visualization](Exercises/07_Visualization)

[Chipotle](Exercises/07_Visualization/Chipotle)
[Titanic Disaster](Exercises/07_Visualization/Titanic_Desaster)
[Scores](Exercises/07_Visualization/Scores)
[Online Retail](Exercises/07_Visualization/Online_Retail)
[Tips](Exercises/07_Visualization/Tips)

### [Creating Series and DataFrames](Exercises/08_Creating_Series_and_DataFrames)

[Pokemon](Exercises/08_Creating_Series_and_DataFrames/Pokemon)

### [Time Series](Exercises/09_Time_Series)

[Apple_Stock](Exercises/09_Time_Series/Apple_Stock)
[Getting_Financial_Data](Exercises/09_Time_Series/Getting_Financial_Data)
[Investor_Flow_of_Funds_US](Exercises/09_Time_Series/Getting_Financial_Data)

### [Deleting](Exercises/10_Deleting)

[Iris](Exercises/10_Deleting/Iris)
[Wine](Exercises/10_Deleting/Wine)


## Copyright

* [Exercícios](Exercises) - Copyright (c) 2018, [Guilherme Samora](https://github.com/guipsamora)
    * [BSD 3-Clause](Exercies/LICENSE)

