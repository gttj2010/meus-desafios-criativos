# Desafio Criativo: Extraindo Insights do Feedback de Clientes Bancários
> **Desafio de Projeto desenvolvido para a plataforma Digital Innovation One (DIO)**

Este repositório documenta a resolução do Desafio Criativo focado na estruturação e refinamento de um prompt de Inteligência Artificial para análise de sentimentos, triagem de dores e geração de insights acionáveis baseados em feedbacks de clientes do setor bancário.

---

## 🧱 Passo 1: Definição da Intenção

*   **Quero que a IA analise:** Bases de comentários, avaliações de lojas de aplicativos (App Store/Google Play) e transcrições de chats de suporte de clientes bancários.
*   **Para identificar:** Gargalos operacionais, falhas em transações financeiras (como PIX e cartões), elogios e oportunidades de melhoria em canais digitais.
*   **O resultado será usado por:** Equipes de Experiência do Cliente (CX), Gerentes de Produto (PMs) e times de Tecnologia/Inovação.
*   **Para apoiar:** A tomada de decisão na melhoria contínua dos canais digitais, priorização de correções de bugs em ambiente produtivo e refinamento do autoatendimento.
*   **A entrega deve conter:** Um resumo executivo de alto nível, uma tabela estruturada mapeando o problema e a criticidade, e sugestões de planos de ação práticos.
*   **O resultado será considerado bom se:** Apresentar clareza técnica, for pautado exclusivamente em dados reais fornecidos, mantiver foco em ações práticas e separar percepções subjetivas de falhas sistêmicas brutas.

---

## 🧱 Passo 2: Contexto e Restrições

*   **Contexto:** Estou trabalhando com feedbacks de clientes bancários relacionados ao ecossistema de pagamentos instantâneos (PIX), usabilidade do aplicativo mobile, segurança em transações de investimentos e tempo de espera no atendimento humano via chat.
*   **Dados disponíveis:** A base fornecida contém metadados contendo: ID anônimo do cliente, data/hora da interação, texto do feedback livre, categoria do produto citado (PIX, Cartão, Conta, Investimentos) e nota de satisfação (NPS/CSAT de 1 a 5).
*   **Critérios de análise:** A IA deve categorizar as entradas por tema, classificar o sentimento (Positivo, Neutro, Negativo) e determinar o nível de urgência/criticidade (Baixa, Média, Alta).
*   **Cuidados e restrições obrigatórias:**
    *   *Aderência estrita:* Use apenas os dados fornecidos no contexto.
    *   *Zero Alucinação:* Não invente números, estatísticas falsas ou causas raiz sem comprovação factual na base.
    *   *Segurança de Dados:* Sob nenhuma hipótese exponha dados pessoais, sensíveis ou identificadores (como CPF, nomes, senhas ou saldos).
    *   *Estilo Linguístico:* Use uma linguagem corporativa, executiva, direta e totalmente orientada a negócios (*data-driven*).

---

## 🧱 Passo 3: O Prompt Final Refinado e Unificado

Abaixo está o comando de Engenharia de Prompts consolidado, pronto para ser copiado e utilizado em qualquer Large Language Model (LLM):

```text
Atue como um Especialista Sênior em Engenharia de Dados e Experiência do Cliente (CX) no setor bancário.

Sua tarefa é analisar uma base de feedbacks textuais de clientes bancários relacionados ao ecossistema de pagamentos (PIX), aplicativo mobile, investimentos e canais de suporte para identificar padrões ocultos e dores críticas.

Contexto: Os insights gerados por você serão consumidos por diretores de produtos e gerentes de engenharia para priorizar o backlog de desenvolvimento e reduzir as taxas de atrito em transações financeiras digitais.

Dados disponíveis: Serão fornecidos blocos de comentários contendo a data do registro, canal de origem, o relato livre do usuário, o produto correspondente e a nota atribuída de 1 a 5.

Instruções de análise aplicadas:
1. Classifique cada feedback cruzando o tema principal com a análise de sentimento (Positivo, Neutro ou Negativo) e defina um nível de urgência (Alta, Média, Baixa).
2. Identifique os 3 problemas mais recorrentes que demandam atenção imediata e os associe a evidências textuais curtas extraídas dos dados fornecidos.
3. Elabore recomendações e planos de ações preventivas e corretivas direcionadas para a equipe de tecnologia.

Formato da resposta esperado:
- Um resumo executivo conciso contendo a visão geral do cenário atual (máximo 5 linhas).
- Uma tabela Markdown estruturada com as colunas: | Produto/Canal | Sentimento | Criticidade | Dor Identificada | Evidência (Trecho do Feedback) | Ação Sugerida |.
- Uma lista em tópicos destacando as 3 maiores oportunidades de retenção de clientes.

Restrições severas:
- Baseie-se unicamente nas informações enviadas. Não crie cenários fictícios.
- Proteja dados sensíveis. Se houver nomes, números de contas ou CPFs, mascare-os.
- Caso o volume de dados de uma categoria seja insuficiente para gerar um padrão, aponte essa limitação explicitamente no relatório.
- Adote um tom formal, objetivo, analítico e focado em tomada de decisão estratégica.
