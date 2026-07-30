\# dbt CI/CD Workflow



\## CI Pipeline (PR Time)



Developer

↓

Feature Branch

↓

Pull Request

↓

GitHub Actions CI

↓

dbt compile

↓

dbt test

↓

dbt build





\## CD Pipeline (Deploy Time)



Merge to Main

↓

Deploy dbt Models

↓

Production Tests

↓

Scheduled Jobs





\## Tests



\### PR Time

\- dbt compile

\- dbt test

\- dbt build --select modified+



\### Deploy Time

\- Full dbt build

\- Source freshness

\- Regression tests





\## Secrets Management



Secrets:

\- Database username

\- Password

\- Warehouse credentials



Storage:

\- GitHub Actions Secrets

\- Azure Key Vault

