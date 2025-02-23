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

[Credit scoring methods](https://pdf.sciencedirectassets.com/313360/1-s2.0-S2405918821X00037/1-s2.0-S2405918822000095/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjENr%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJGMEQCIDjFi6z78zKWIAp7KLlCQh7%2B4nmLCFhSyCf9drFGfkESAiAUSvGKR6yy0TcasG2pU14zmUyhfyhk8l%2Fsflvh6K0JmyqzBQgSEAUaDDA1OTAwMzU0Njg2NSIMGFZB5KTVFqoQD675KpAF0FzbnvhcMi%2FpXB3McTNc9P2XrpBwFhaEJfjbudiAQZxUgQXIL%2BibTi%2FOHI5tnc4%2FQmTylFImVOnE6U0gYLY238Go5BmhQ18XzR1Ail7gIYeIBQMB8%2F2sGKVfFKH3R6L2lGjT4fMsBTl5%2FWNE%2B1seD4oKfoLfXX7zshzOLV8TQceHe%2FnchzrwvHGZFFwEFH4eG1doBVJFqqxEJFLZV94xENpieJDmWC2tqv6JGaZU54CQqXAUPyxA3HAhPrlrdsoqGL0aHBsR2bnFZPbJTS6Pz9dpzsQ6nN7jBQgUFWZtc9uqdRHtBWKFDJ1NbK3RhyZElExRMsvcaJBnZOpUAuP0TVLTAP4ZXTeWcLRugTrb7MOGDufl8mTTueaal6ZmqyXrYWEL%2BStH9IGGaRF6s18aOr110aBll3n57jOUvmmxMMxGZTyU4hlhMmzH54o%2FgzBzs84QMxbRkYLUkMJLnnFY%2FbiCaCYiIm4g%2BLldKlkrlD0G%2BnQdxFIPvSODhb2ZlmgQwep7R5hqMCBhc%2BqKrl8Zb2MvzbTrOqgxj7kmQfEIivG5%2F543wLcSLiOH6qWVFAd0bvQ%2F0RZvTGMk8ldw%2B%2FQGYjGoRQ%2BcGZi21QWUWCeHBHH38eJOczBQ4ff6w4KPtS39L8ehzJawe5XcJnG6J69a0SnX8S3IVu8qZqjk%2B6fTLDyTjR56v6nYSmpyik1pFuvfchPb0GbN%2B6WAas4rjvtUtWU5aNSYjs2gxGXc80px4irON1Y3PFpaPORnQdDIQg9FaEDjSMpT31wfjSgEU%2FhX5wdDUt9RNmFont%2FCPqDzs6dAPxGX%2B0M5mZw%2Bo%2BgexfIIqUJQ4glSYa0scf%2BY8UJsPL0SpGEV1%2FQoFAr82837Sj8w3MvrvQY6sgHl%2Bjh3AUWF3z6xXhEz%2BDOfX%2Fv7iQ60XssQBbep9Ef3JYpNmuGuqfzUCf2%2B91Wy1FJS3sX02uc5wcVnl7SAQYEGet%2BSXwTduNRQYIu43%2FPW1X67fvm4DIGZBvUUcULlckvQmhnWyXuUvZbeej9Znu%2BfdHREUegO1Frw0MP5xu6zHKNwNG0sKnSaG%2Bo14d4NZK0cTyqqnKvBVG6Ej%2Fvw5uRer76HIYLHFTnSAQannQ%2BIQW6M&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250223T094810Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYYNS475TS%2F20250223%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=476a6d57399836c3ebbdf5e2fa5790858ce52af048e2716165335f2d9d6cbb29&hash=6909a298348249e8d768c75e1d90165221e4536f1539742bdadbced0f73b3976&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S2405918822000095&tid=spdf-466132fd-c5f0-410c-9cdb-12cd81a693ea&sid=0583799a72978842b96a5fe329b6855a19f6gxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&rh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=17135d53595753045754&rr=91664c739f9e8d9e&cc=ru)

[Credit scores: perfomance and equity](https://www.nber.org/system/files/working_papers/w32917/w32917.pdf)

[ML-пайплайн классических банковских моделей классификации](https://habr.com/ru/companies/vtb/articles/725928/)

[Модель следит за моделью: как MPP-подход помогает прогнозировать риски и принимать решения](https://habr.com/ru/companies/vtb/articles/505892/)

[Три способа оценить данные - разбор каждого с нуля](https://dzen.ru/a/ZugQ6etOIHBDpnEM)

[Логистическая регрессия. Теория и реализация. С нуля](https://habr.com/ru/articles/864890/)
