# 🛡️ LAB 04: Excesso de Autonomia e Chamada Insegura de Ferramentas (OWASP LLM06)

Este repositório contém o laboratório prático de cibersegurança em Inteligência Artificial focado na vulnerabilidade de **Excesso de Autonomia e Chamada Insegura de Ferramentas (OWASP LLM06: Excessive Agency)**. 

Aqui exploramos de forma estruturada como agentes de IA integrados a ferramentas de backend podem ser manipulados para executar ações destrutivas (Red Team) e como implementar barreiras defensivas robustas no backend (Blue Team).

---

## 🎯 Objetivo do Laboratório

Demonstrar na prática como a vulnerabilidade **OWASP LLM06** permite que um atacante explore agentes de IA com permissões excessivas para executar funções críticas (como deletar contas ou executar rotinas privilegiadas sem consentimento), e como construir *Guardrails* de autorização, controle de acesso baseado em papel (RBAC), sistemas de confirmação humana (*Human-in-the-Loop*) e auditoria no backend para mitigar esse risco.

* **Modelo Utilizado:** Qwen 2.5 (1.5B Instruct) (`Qwen/Qwen2.5-1.5B-Instruct`)
* **Ambiente de Execução:** Kaggle Notebooks (Otimizado com GPU T4 x2)
* **Vulnerabilidade Alvo:** OWASP LLM06 - Excessive Agency / Execução Induzida de Ferramentas

---

## 🧪 Estrutura da Atividade

### 🔴 Red Team (Ataque)
* **Conceito:** Exploração da vulnerabilidade OWASP LLM06 onde o assistente autônomo é manipulado por engenharia social e injeções de prompt para acionar funções críticas no sistema sem validação de identidade.
* **Vetores de Teste:** Pretexto de ambiente de homologação (*sandbox*), falsa autoridade de segurança (*privilege escalation* via *impersonation*) e injeção de prompt indireta em documentos externos.

### 🔵 Blue Team (Defesa)
* **Conceito:** Aplicação de estratégias de blindagem estrutural no backend.
* **Solução:** Implementação de barreiras de verificação humana (*Human-in-the-Loop*), controle de acesso estrutural (RBAC) e monitoramento contínuo com logs de auditoria em tempo real.

---

## 📋 Detalhamento das Atividades Práticas

### Módulo Red Team (Ataques de Excessive Agency)
* **Atividade A:** Ataque via pretexto de homologação (*sandbox*).
* **Atividade B:** Ataque por falsa autoridade de segurança (*privilege escalation*).
* **Atividade C:** Ataque de encadeamento indireto de ferramentas (*Indirect Prompt Injection*).

### Módulo Blue Team (Defesa & Blindagem de Backend)
* **Atividade D:** Implementação de *Guardrail* e *Human-in-the-Loop*.
* **Atividade E:** Teste de defesa do *Guardrail* sob ordens administrativas falsas.
* **Atividade F:** Implementação de RBAC (Role-Based Access Control) no backend.
* **Atividade G:** Sistema de auditoria e logs de segurança em tempo real.

---

## 🚀 Como Executar
1. Acesse o **Kaggle Notebooks** e configure o acelerador de hardware para **GPU T4 x2**.
2. Configure seu token de acesso da Hugging Face no ambiente.
3. Crie ou importe o notebook com o código e siga as etapas práticas de Red Team e Blue Team.

---

> **Lição Principal:** *"Jamais dê autonomia total a uma IA para executar ações destrutivas ou privilegiadas (como deletar dados, alterar configurações ou transferir fundos) de forma totalmente automatizada! Sempre implemente barreiras de confirmação humana (Human-in-the-Loop) e verificação estrita de permissões no backend antes de disparar ferramentas!"*
