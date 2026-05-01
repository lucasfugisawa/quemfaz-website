---
layout: default
title: Política de Privacidade — QuemFaz
permalink: /privacidade.html
---

# Política de Privacidade

**Última atualização:** 2026-05-01
**Versão:** 1.0.0

> **Aviso ao revisor:** este texto é um rascunho preparado pela engenharia, baseado na infraestrutura técnica do aplicativo. Antes de publicação, deve ser revisado por um Encarregado de Proteção de Dados (DPO) ou advogado especializado em LGPD. Os pontos específicos pendentes de validação jurídica estão listados em `docs/launch/lgpd-privacy-addendum-draft.md` no repositório principal.

---

## 1. Quem somos

O **QuemFaz** é uma plataforma que conecta consumidores a prestadores de serviços locais no Brasil.

**Controlador dos dados:** [a definir conforme estrutura societária — CPF do fundador ou CNPJ da empresa].
**Contato:** [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br).
**Encarregado de Proteção de Dados (DPO):** [a definir — LGPD art. 41].

## 2. Quais dados coletamos

| Dado | Para que coletamos | Quando |
|---|---|---|
| Número de telefone | Autenticação por SMS (OTP) | Cadastro |
| Nome completo | Identificação no perfil | Cadastro |
| Foto de perfil | Identificação visual | Após cadastro (opcional para clientes; obrigatório para profissionais) |
| Data de nascimento | Verificação de idade mínima (18+) para prestadores de serviço | Cadastro de profissional |
| Cidade selecionada | Filtro de busca por região | Cadastro |
| Descrição do perfil profissional | Apresentação do prestador | Cadastro de profissional |
| Fotos de portfólio | Apresentação visual do trabalho | Cadastro de profissional |
| Histórico de buscas | Métricas internas de serviços mais procurados (agregadas) | Durante uso |
| Identificadores técnicos (endereço IP, modelo do dispositivo, versão do app) | Operação técnica e diagnóstico | Durante uso |
| Relatórios de erro (Sentry) | Identificar e corrigir problemas no aplicativo | Quando o app encontra erros |

**Não coletamos:** localização precisa, contatos do dispositivo, histórico de outros aplicativos, dados de pagamento (não há transações financeiras dentro do app — o contato com o profissional acontece via WhatsApp ou telefone, fora da plataforma).

## 3. Como usamos os dados

- **Operação do serviço.** Permitir login, exibir perfis nas buscas, conectar consumidor e profissional.
- **Comunicação operacional.** Enviar códigos de autenticação por SMS.
- **Métricas internas.** Entender quais serviços são mais buscados em cada cidade, melhorar o aplicativo.
- **Segurança.** Detectar abuso (rate limiting baseado em IP, identificação de relatos repetidos do mesmo perfil).
- **Suporte.** Responder a contatos enviados para [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br).

**Não vendemos seus dados pessoais a terceiros. Não os usamos para publicidade direcionada.**

## 4. Com quem compartilhamos os dados

Compartilhamos apenas com provedores de infraestrutura essenciais ao funcionamento da plataforma — todos vinculados por contrato a obrigações de proteção de dados equivalentes às da LGPD:

| Provedor | Dados compartilhados | Finalidade |
|---|---|---|
| Amazon Web Services (AWS) | Todos os dados pessoais armazenados (banco de dados, imagens) | Hospedagem da infraestrutura |
| Sentry | Identificadores técnicos + traços de erro (sem nome/telefone/email) | Monitoramento de erros |
| OpenAI | Trechos de descrição de perfil profissional, durante o cadastro | Interpretação de descrições para mapeamento ao catálogo de serviços |
| Operadoras de SMS (AWS SNS) | Número de telefone, código OTP de 6 dígitos | Envio do SMS de autenticação |

Compartilhamentos com autoridades públicas ocorrem apenas mediante ordem judicial ou requisição legal formal.

## 5. Transferência internacional de dados

A infraestrutura técnica do QuemFaz é operada pela Amazon Web Services (AWS) na região **us-east-1 (Norte da Virgínia, Estados Unidos)**. Isso significa que os dados pessoais coletados pelo aplicativo são armazenados e processados em servidores localizados nos Estados Unidos.

A escolha por hospedar a infraestrutura nos EUA decorre da maior disponibilidade de serviços gerenciados na região us-east-1 da AWS, com benefícios diretos de estabilidade, segurança e performance para os usuários.

Esta transferência internacional é realizada com base no **artigo 33 da LGPD** (Lei nº 13.709/2018), que permite a transferência de dados pessoais para países que oferecem grau de proteção adequado, ou mediante consentimento específico do titular.

Ao criar uma conta no QuemFaz, você confirma ter lido este aviso e fornece consentimento específico para que seus dados sejam transferidos para os Estados Unidos e processados pela infraestrutura AWS daquela região.

A AWS é certificada pelos principais frameworks internacionais de segurança e privacidade (ISO 27001, ISO 27017, ISO 27018, SOC 2 Type II). Todos os dados em trânsito entre o aplicativo e os servidores são criptografados via TLS 1.2 ou superior. Dados em repouso são criptografados nos volumes EBS e S3 com chaves gerenciadas pela AWS.

Caso você revogue este consentimento posteriormente, a continuidade do uso do aplicativo poderá ficar inviabilizada — neste caso, sua conta poderá ser desativada e seus dados pessoais excluídos mediante solicitação, conforme detalhado na seção "Seus direitos" abaixo.

## 6. Por quanto tempo guardamos os dados

| Categoria | Período de retenção |
|---|---|
| Dados de conta ativa (telefone, nome, perfil) | Enquanto a conta estiver ativa |
| Dados de conta desativada | [a definir com revisão jurídica — sugestão inicial: 6 meses para fins de auditoria + tributários, depois exclusão definitiva] |
| Histórico de buscas (anônimo agregado) | Indefinido (dados agregados, não identificáveis individualmente) |
| Relatórios de erro (Sentry) | 90 dias |
| Logs de servidor (CloudWatch) | 30 dias |

## 7. Seus direitos

Conforme os artigos 17 a 22 da LGPD, você pode exercer os seguintes direitos a qualquer momento:

- **Confirmação** da existência de tratamento de seus dados;
- **Acesso** aos dados que mantemos sobre você;
- **Correção** de dados incompletos, inexatos ou desatualizados;
- **Anonimização, bloqueio ou eliminação** de dados desnecessários, excessivos ou tratados em desconformidade com a LGPD;
- **Portabilidade** dos dados a outro fornecedor de serviço;
- **Eliminação** dos dados pessoais tratados com base em seu consentimento (exceto nas hipóteses previstas no art. 16 da LGPD);
- **Informação** sobre as entidades públicas e privadas com as quais compartilhamos seus dados;
- **Revogação do consentimento**, nos termos do § 5º do art. 8º da LGPD.

Para exercer qualquer destes direitos, envie um email para [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br) com o assunto **"[LGPD] Solicitação"**. Buscamos responder a todas as solicitações em até 15 dias.

## 8. Cookies e tecnologias similares

Atualmente o QuemFaz não utiliza cookies — o serviço é exclusivamente um aplicativo móvel (Android/iOS), sem versão web. Caso uma versão web seja lançada no futuro, esta política será atualizada e você será notificado.

## 9. Alterações nesta política

Quando alterações materiais forem feitas, o número da versão no topo desta página será atualizado e você será notificado dentro do aplicativo solicitando aceite expresso da nova versão antes de continuar a usar o serviço.

## 10. Como entrar em contato

- **Suporte / dúvidas gerais:** [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br)
- **Solicitações relativas a dados pessoais (LGPD):** mesmo email, com o assunto "[LGPD] Solicitação"
- **Encarregado de Proteção de Dados (DPO):** [a definir]
- **Autoridade Nacional de Proteção de Dados (ANPD):** [www.gov.br/anpd](https://www.gov.br/anpd) — você tem o direito de fazer reclamações diretamente à ANPD se entender que seus direitos não foram atendidos.
