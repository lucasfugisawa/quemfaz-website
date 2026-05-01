---
layout: default
title: Excluir minha conta
description: Como solicitar a exclusão da sua conta no QuemFaz e dos dados associados.
eyebrow: Exclusão de conta
lede: Como solicitar a exclusão da sua conta no QuemFaz e dos dados pessoais associados.
updated: 2026-05-01
permalink: /excluir-conta.html
---

## Sobre o app

Esta página descreve o procedimento de exclusão de conta do **QuemFaz**, aplicativo de marketplace de profissionais de serviços locais.

- **App**: QuemFaz
- **Operação mantida por**: Lucas Fugisawa (CPF 220.414.728-12)
- **Identificadores nas lojas**:
  - Google Play: `com.fugisawa.quemfaz`
  - App Store: `com.fugisawa.quemfaz`
- **Site**: [https://quemfaz.com.br](https://quemfaz.com.br)
- **Canal oficial de contato**: [contato@quemfaz.com.br](mailto:contato@quemfaz.com.br)

## Como solicitar a exclusão

### Por email (caminho atual)

1. Envie um email para **[contato@quemfaz.com.br](mailto:contato@quemfaz.com.br?subject=Excluir%20conta)** com o assunto **"Excluir conta"**.
2. No corpo do email, informe o **número de telefone celular cadastrado** no app (em formato `+55 (DDD) 9XXXX-XXXX` ou `+55DDD9XXXXXXXX`).
3. Para confirmar que o pedido vem de fato do titular da conta, vamos enviar um **código de 6 dígitos por SMS** para o número informado. Responda ao email com o código.
4. Após confirmar a identidade, a conta é **desativada imediatamente** (deixa de aparecer em buscas e não consegue mais fazer login).
5. A exclusão final dos dados pessoais ocorre conforme detalhado em **[O que é excluído e o que é retido](#o-que-é-excluído-e-o-que-é-retido)** abaixo.
6. Você recebe uma confirmação por email quando o processo for concluído. Prazo total: até **15 dias corridos** a partir da confirmação por SMS, conforme o prazo recomendado pela ANPD para atendimento de solicitações LGPD.

### Pelo app (em breve)

A funcionalidade de exclusão de conta diretamente pelo app está prevista para uma próxima atualização. Quando estiver disponível, o caminho será **Perfil → Configurações → Excluir minha conta**, e segue o mesmo fluxo de confirmação por SMS descrito acima.

## O que é excluído e o que é retido

### Dados que são excluídos imediatamente após a confirmação

- Número de telefone celular (após período de retenção de auditoria — ver abaixo)
- Nome
- Foto de perfil
- Data de nascimento
- Cidade selecionada
- Descrição do perfil profissional
- Fotos de portfólio
- Histórico de buscas individual (associado à sua conta)
- Tokens de autenticação ativos (efeito imediato: você é deslogado de todos os dispositivos)
- Tokens de notificação push (você para de receber notificações)

### Dados retidos por período definido (e a base legal)

| Categoria de dado | Período de retenção após desativação | Base legal |
|---|---|---|
| Telefone, nome, perfil (de conta desativada) | **6 meses**, para fins de auditoria, prevenção a fraudes e cumprimento de obrigações tributárias e regulatórias | Art. 16, I e III, da LGPD (cumprimento de obrigação legal e legítimo interesse de prevenção a fraudes) |
| Histórico de buscas agregado e anônimo | **Indefinido** (dados agregados, sem identificação individual após anonimização) | Art. 12 da LGPD (dados anonimizados não são considerados dados pessoais) |
| Relatórios de erro técnico (Sentry, sem nome/telefone/email) | **90 dias** | Art. 7º, IX, da LGPD (legítimo interesse em diagnóstico de falhas) |
| Logs de servidor (CloudWatch — endereço IP e identificadores técnicos) | **30 dias** | Art. 7º, IX, da LGPD (legítimo interesse em segurança e operação) |
| Comprovantes de transações eventuais com a operação (não há, atualmente) | Variável conforme legislação fiscal aplicável | Art. 16, I, da LGPD |

Após o período de retenção, os dados são **excluídos definitivamente** dos sistemas de produção. Backups operacionais com criptografia em repouso são rotacionados a cada 30 dias e expiram completamente em até 90 dias adicionais.

## O que NÃO é excluído por essa solicitação

- **Conversas que você teve via WhatsApp ou telefone com profissionais ou clientes** — o QuemFaz nunca teve acesso a esses dados (a conversação acontece direto entre as partes, fora da plataforma). Pra apagar essas conversas, fale com o WhatsApp ou exclua manualmente.
- **Dados que outros usuários tenham capturado por conta própria** — por exemplo, se você compartilhou seu telefone via WhatsApp com um profissional, esse profissional ainda terá seu contato fora da nossa plataforma. O QuemFaz não controla isso.

## Exclusão obrigatória pelo QuemFaz

O QuemFaz pode encerrar uma conta sem solicitação do titular nos casos descritos nas [Diretrizes da Comunidade](/diretrizes.html) e nos [Termos de Uso](/termos.html) — por exemplo, em caso de fraude, identidade falsa, ou conteúdo ilegal. Nesses casos, os mesmos prazos de retenção descritos acima se aplicam.

## Outros direitos do titular

A exclusão é apenas um dos direitos previstos pela LGPD. Você também tem direito a confirmação de tratamento, acesso, correção, portabilidade, anonimização, bloqueio, informação sobre compartilhamentos, e revogação de consentimento. Veja a **[Política de Privacidade](/privacidade.html)** completa, em especial a Seção 8 ("Seus direitos").

Pra exercer outros direitos, escreva para [contato@quemfaz.com.br](mailto:contato@quemfaz.com.br) com o assunto **"[LGPD] Solicitação"**.

## Em caso de dúvidas

- **Contato geral / dúvidas sobre o processo**: [contato@quemfaz.com.br](mailto:contato@quemfaz.com.br)
- **Encarregado pelo Tratamento de Dados (DPO), nos termos do art. 41 da LGPD**: Lucas Fugisawa — [contato@quemfaz.com.br](mailto:contato@quemfaz.com.br) com o assunto **"[LGPD] DPO"**.
- **Autoridade Nacional de Proteção de Dados (ANPD)**: caso você entenda que seus direitos não foram atendidos, pode reclamar diretamente em [www.gov.br/anpd](https://www.gov.br/anpd).
