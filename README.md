# Tech Challenge • Fase 3: PNAD COVID-19

<img width="29" height="39" alt="image" src="https://github.com/user-attachments/assets/c7c68151-ec02-4412-ac92-a413aca097c6" />  **Proposta:**

Esse estudo visa expor e analisar os microdados da PNAD-COVID-19 para identificar os diferentes impactos na população brasileira em recortes sociais e econômicas nos casos de Covid registrados pela “Pesquisa Nacional por Amostra de Domicílios”, e assim, gerar insights estratégicos que apoiem a tomada de decisão e direcionamento gerencial na criação de medidas e padrões a serem adotados em uma nova crise sanitária.

Em uma análise orientada por dados, esse estudo identifica e quantifica as interconexões entre características clínicas, perfis sociodemográficos e vulnerabilidades econômicas, a fim de gerar um modelo direcionador de ações que permita ao hospital otimizar a alocação de recursos, a triagem de pacientes e a comunicação estratégica.

**•  As regras adotadas nesta analise são:** 

1.	Utilização exclusiva da base de dados PNAD-COVID19 do IBGE.
2.	Seleção de um máximo de 20 variáveis para a análise.
3.	Foco em um período contínuo de três meses: **setembro a novembro de 2020.**

<img width="25" height="35" alt="image" src="https://github.com/user-attachments/assets/f6a95ab0-ed8d-4357-b1f5-f198503a997d" />  **A leitura completa do documento executivo pode ser feita aqui:**<BR/><BR/>

 <img width="25" height="35" alt="image" src="https://github.com/user-attachments/assets/291c7ccb-1da0-4e5e-a4e6-418759ad421d"/>   **Limitações do estudo:**
É importante ressaltar que os dados da PNAD COVID-19 são baseados em entrevistas domiciliares e autorrelato, não em prontuários médicos. Dessa forma, as conclusões refletem a percepção e o conhecimento dos entrevistados e não devem ser confundidas com dados clínicos de diagnóstico confirmado.

# Arquitetura

<img width="1861" height="709" alt="image" src="https://github.com/user-attachments/assets/2cc6385c-1bbd-458f-a3bd-6dd0e6a2810b" />
 <BR/><BR/>


   **1. Coleta de dados** <BR/>
      •	A base de dados foi obtida no site do IBGE, extraindo o resultado da PNAD COVID-19 em um arquivo .xlsx excel.

  **2. ETL**<BR/>
  •	O tratamento de dados foi realizado em SQL utilizando o Snowflake. <BR/>
•	Camada bronze é composta pela raw data extraída do excel com resultados da PNAD. <BR/>
•	Camada Silver é o resultado dos tratamentos de padronização, de/para e enriquecimentos. <BR/>
•	Camada Gold é o resultado da criação das tabelas com dados prontos para consumo. <BR/>

**3. Análise de dados** <BR/>
•	As análises e criação de fato e dimensão foram realizadas no Power BI. <BR/>

**4. End User** <BR/>
•	Os resultados das análises e visualização gráfica foram construídos em Power BI. <BR/>
•	A documentação contendo recomendações foi desenvolvida em Word/ PDF.<BR/>
•	Os códigos e processos foram disponibilizados no Git Hub.<BR/><BR/>

REVIEWREVIEWREVIEWREVIEWREVIEWREVIEWREVIEW
# De/Para (Mapeamento PNAD)




# Diagrama de tabela
![Imagem do WhatsApp de 2025-10-07 à(s) 15 10 16_3a476ae0](https://github.com/user-attachments/assets/0f569549-150d-4032-a0c3-777a33a41e73)

A tabela SOT possui 20 variáveis, distribuídas em grupos:<BR/>

• 4 variáveis de caracterização da pessoa (sexo, idade, escolaridade, cor ou raça).<BR/>
• 5 variáveis de sintomas clínicos da população (febre, tosse, dificuldade de respirar, fadiga, perda de olfato/paladar).<BR/>
• 5 variáveis de comportamento da população durante a pandemia (procurou atendimento, Pronto socorro SUS/UPA, Hospital do SUS, uso de hospital privado).<BR/>
• 3 variáveis econômicas (estava trabalhando, rendimento bruto mensal efetivo, recebimento de bolsa familia).<BR/>
• 3 variáveis de partição (ano, mês, UF).
