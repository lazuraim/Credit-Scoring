## Кредитный скоринг

Реализация модели кредитного скоринга

## Описание датасета


| data/application_record.csv |
|--------------------|

| Feature | Description |
|----------|----------|
| ID | Client number |
| CODE_GENDER	| Gender |
| FLAG_OWN_CAR | Is there a car	|
| FLAG_OWN_REALTY	| Is there a property	|
| CNT_CHILDREN	| Number of children	|
| AMT_INCOME_TOTAL	| Annual income	|
| NAME_INCOME_TYPE	| Income category	|
| NAME_EDUCATION_TYPE	| Education level	|
| NAME_FAMILY_STATUS	| Marital status	|
| NAME_HOUSING_TYPE	| Way of living	|
| DAYS_BIRTH	Birthday	| Count backwards from current day (0), -1 means yesterday |
| DAYS_EMPLOYED	| Start date of employment	Count backwards from current day(0). If positive, it means the person currently unemployed. |
| FLAG_MOBIL	| Is there a mobile phone	|
| FLAG_WORK_PHONE	| Is there a work phone	|
| FLAG_PHONE	| Is there a phone |
| FLAG_EMAIL	| Is there an email	|
| OCCUPATION_TYPE	| Occupation	|
| CNT_FAM_MEMBERS	| Family size |


| data/credit_record.csv |
|--------------------|

| Feature | Description |
|----------|----------|
| ID | Client number |
| MONTHS_BALANCE	| Record month	The month of the extracted data is the starting point, backwards, 0 is the current month, -1 is the previous month, and so on |
| STATUS	Status	| 0: 1-29 days past due 1: 30-59 days past due 2: 60-89 days overdue 3: 90-119 days overdue 4: 120-149 days overdue 5: Overdue or bad debts, write-offs for more than 150 days C: paid off that month X: No loan for the month |

[dataset on kaggle](https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction)

## Преодобработка данных

## Результаты + интерпретация

## Статьи для вдохновения

[ML-пайплайн классических банковских моделей классификации](https://habr.com/ru/companies/vtb/articles/725928/)

[Модель следит за моделью: как MPP-подход помогает прогнозировать риски и принимать решения](https://habr.com/ru/companies/vtb/articles/505892/)

[Три способа оценить данные - разбор каждого с нуля](https://dzen.ru/a/ZugQ6etOIHBDpnEM)

[Логистическая регрессия. Теория и реализация. С нуля](https://habr.com/ru/articles/864890/)
