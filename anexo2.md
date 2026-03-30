# Manual de Boas Práticas - Amazon EC2

**Objetivo:** Garantir a performance da farmácia com o menor custo possível.

---

### 1. Direito ao Tamanho (Right Sizing)
Nunca utilize uma instância maior do que o necessário. Monitore o uso de CPU e Memória e ajuste o tipo da instância (ex: mudar de `t3.medium` para `t3.micro`) conforme a carga real de trabalho.

### 2. Uso de Instâncias Spot
Utilize instâncias **Spot** para tarefas que não são críticas em tempo real (como processamento de relatórios de estoque de madrugada). Isso permite uma economia de até **90%** em relação ao preço sob demanda.

### 3. Tags de Identificação
Sempre taguear as instâncias (ex: `Projeto: Farmacia`, `Ambiente: Producao`). Isso facilita a leitura detalhada da fatura no **AWS Billing** e a identificação de desperdícios.

### 4. Agendamento (Instance Scheduler)
Configure o desligamento automático de instâncias de ambientes de teste ou administrativo fora do horário comercial da farmácia, evitando cobranças por ociosidade.