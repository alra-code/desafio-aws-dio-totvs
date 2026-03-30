# Política de Retenção de Dados (Amazon S3)

**Escopo:** Gestão de documentos digitais e receitas médicas.

---

### 📅 Ciclo de Vida dos Dados

* **Dados Ativos (0-30 dias):** Armazenados na classe **S3 Standard**. Focado em acesso imediato para conferência de vendas e consultas rápidas.
* **Dados Semi-Ativos (31-90 dias):** Movimentação automática via *Lifecycle Policy* para **S3 Standard-IA** (Acesso Infrequente). Reduz o custo de armazenamento mantendo a disponibilidade para auditorias.
* **Arquivamento Legal (91 dias - 5 anos):** Movimentação para o **S3 Glacier Flexible Retrieval**. Cumpre a legislação de guarda de receituários com o menor custo possível.
* **Exclusão Permanente:** Após 5 anos (ou conforme legislação vigente), os dados são deletados automaticamente para garantir a conformidade e eliminar custos residuais.

Voltar >>> [Readme](./readme.md)