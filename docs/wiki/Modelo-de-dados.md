# Modelo de dados

Rascunho do modelo (será detalhado na issue de UML). Base para o `db.json` do JSON Server e para a v2 em PostgreSQL.

```mermaid
erDiagram
    EMPRESAS ||--o{ VAGAS : anuncia
    VAGAS ||--|| VAGA_TRANSPARENCIA : tem
    VAGAS ||--o{ VAGA_BENEFICIOS : oferece
    VAGAS ||--o{ VAGA_ETAPAS : possui
    CATEGORIAS ||--o{ NOTICIAS : classifica

    VAGAS {
        int id PK
        string codigo
        string titulo
        string escolaridade
        int experiencia_meses
        decimal salario
        int numero_vagas
        string modelo_trabalho
        string tipo
        boolean exclusiva_pcd
        date publicada_em
        date inscricoes_ate "opcional"
    }
    EMPRESAS {
        int id PK
        string razao_social "opcional"
        string nome_fantasia "opcional"
        string cnpj "opcional"
    }
    VAGA_TRANSPARENCIA {
        int vaga_id FK
        text atividades
        string horario "opcional"
        string local_trabalho "opcional"
        text entrevista
    }
    NOTICIAS {
        int id PK
        string titulo
        text resumo
        date publicada_em
        int categoria_id FK
    }
```

Outras tabelas previstas: `servicos`, `faq`, `depoimentos`, `unidades` e `contatos` (SAC e Ouvidoria).
