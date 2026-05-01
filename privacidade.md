---
layout: default
title: Política de Privacidade — QuemFaz
permalink: /privacidade.html
---

<!--
Quando a estrutura societária mudar (criação de PJ), atualizar a Seção 1,
bumpar a Versão para 1.1.0 e atualizar LEGAL_REQUIRED_PRIVACY_VERSION no SSM
para forçar reconsentimento dos titulares.
-->

# Política de Privacidade

**Última atualização:** 2026-05-01
**Versão:** 1.0.0

## 1. Quem somos

O **QuemFaz** é uma plataforma que conecta consumidores a prestadores de serviços locais no Brasil.

**Controlador dos dados pessoais:**
Lucas Fugisawa, brasileiro, inscrito no CPF sob o nº 220.414.728-12.

**Canal oficial de contato:** [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br)

**Encarregado pelo Tratamento de Dados Pessoais (DPO), nos termos do art. 41 da LGPD:**
Lucas Fugisawa.
Contato: [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br) com o assunto **"[LGPD] DPO"**.

## 2. Quais dados coletamos

| Dado | Para que coletamos | Quando |
|---|---|---|
| Número de telefone celular | Autenticação por SMS (código OTP) | Cadastro |
| Nome completo | Identificação no perfil | Cadastro |
| Foto de perfil | Identificação visual | Após cadastro (opcional para clientes; obrigatório para profissionais) |
| Data de nascimento | Verificação de idade mínima (18 anos) para prestadores de serviço | Cadastro de profissional |
| Cidade selecionada | Filtro de busca por região | Cadastro |
| Descrição do perfil profissional | Apresentação do prestador | Cadastro de profissional |
| Fotos de portfólio | Apresentação visual do trabalho | Cadastro de profissional |
| Histórico de buscas (agregado) | Métricas internas de serviços mais procurados | Durante uso |
| Identificadores técnicos (endereço IP, modelo do dispositivo, versão do app) | Operação técnica e diagnóstico | Durante uso |
| Relatórios de erro (Sentry) | Identificação e correção de problemas no aplicativo | Quando o app encontra erros |

**Não coletamos:** localização precisa (GPS), contatos do dispositivo, histórico de outros aplicativos, dados de pagamento (não há transações financeiras dentro do app — o contato com o profissional acontece via WhatsApp ou telefone, fora da plataforma).

## 3. Como usamos os dados e em qual base legal

Cada tratamento de dados pessoais realizado pelo QuemFaz tem fundamento expresso no art. 7º da Lei Geral de Proteção de Dados (Lei nº 13.709/2018):

| Finalidade | Dados envolvidos | Base legal |
|---|---|---|
| Permitir login, exibir perfis nas buscas, conectar consumidor e profissional | Telefone, nome, foto, cidade, descrição profissional, fotos de portfólio | Execução de contrato (art. 7º, V) |
| Envio de código de autenticação por SMS | Telefone | Execução de contrato (art. 7º, V) |
| Verificação de idade mínima de profissionais | Data de nascimento | Cumprimento de obrigação legal e regulatória (art. 7º, II) |
| Métricas internas para entender quais serviços são mais buscados em cada cidade | Histórico de buscas (agregado) | Legítimo interesse (art. 7º, IX) |
| Detecção de abuso (rate limiting por IP, identificação de relatos repetidos) | Identificadores técnicos | Legítimo interesse (art. 7º, IX), com prevalência da segurança da plataforma |
| Diagnóstico de falhas técnicas | Identificadores técnicos, traços de erro | Legítimo interesse (art. 7º, IX) |
| Resposta a contatos enviados a [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br) | Email do remetente, conteúdo da mensagem | Execução de contrato (art. 7º, V) ou consentimento (art. 7º, I), conforme o caso |
| Transferência internacional para infraestrutura nos EUA | Todos os dados pessoais armazenados | Consentimento específico (art. 33, VIII), detalhado na Seção 5 |

**Não vendemos seus dados pessoais a terceiros. Não os usamos para publicidade direcionada.**

## 4. Tratamento de dados de menores de idade

Em conformidade com o art. 14 da LGPD:

- O cadastro como **profissional** é restrito a maiores de 18 anos. A data de nascimento é coletada exclusivamente para essa verificação. Caso identifiquemos cadastro de menor como profissional, a conta é encerrada e os dados são eliminados.
- Para uso como **cliente** (busca de profissionais), recomendamos a supervisão de um responsável legal quando o usuário for menor de 18 anos. O QuemFaz não direciona conteúdo a crianças e adolescentes.
- Se identificarmos coleta inadvertida de dados de criança ou adolescente sem o consentimento específico de pelo menos um dos pais ou responsável legal, eliminaremos os dados e encerraremos o uso pelo titular.

## 5. Com quem compartilhamos os dados

Compartilhamos apenas com provedores de infraestrutura essenciais ao funcionamento da plataforma — todos vinculados por contrato a obrigações de proteção de dados equivalentes às da LGPD:

| Provedor | Dados compartilhados | Finalidade |
|---|---|---|
| Amazon Web Services (AWS) | Todos os dados pessoais armazenados (banco de dados, imagens) | Hospedagem da infraestrutura |
| Sentry | Identificadores técnicos + traços de erro (sem nome/telefone/email) | Monitoramento de erros |
| OpenAI | Trechos de descrição de perfil profissional, durante o cadastro | Interpretação de descrições para mapeamento ao catálogo de serviços |
| Operadoras de SMS (AWS SNS) | Número de telefone, código OTP de 6 dígitos | Envio do SMS de autenticação |

Compartilhamentos com autoridades públicas ocorrem apenas mediante ordem judicial ou requisição legal formal, conforme art. 26 da LGPD.

## 6. Transferência internacional de dados

A infraestrutura técnica do QuemFaz é operada pela Amazon Web Services (AWS) na região **us-east-1 (Norte da Virgínia, Estados Unidos)**. Os dados pessoais coletados pelo aplicativo são armazenados e processados em servidores localizados nos Estados Unidos.

A escolha por hospedar a infraestrutura nos EUA decorre da maior disponibilidade de serviços gerenciados na região us-east-1 da AWS, com benefícios diretos de estabilidade, segurança e performance para os usuários.

Esta transferência é realizada com fundamento no **art. 33, inciso VIII, da LGPD**, que admite a transferência internacional mediante consentimento específico e em destaque do titular.

Ao criar uma conta no QuemFaz, você confirma ter lido este aviso e fornece consentimento específico para que seus dados sejam transferidos para os Estados Unidos e processados pela infraestrutura AWS daquela região.

A AWS é certificada pelos principais frameworks internacionais de segurança e privacidade (ISO 27001, ISO 27017, ISO 27018, SOC 2 Type II). Todos os dados em trânsito entre o aplicativo e os servidores são criptografados via TLS 1.2 ou superior. Dados em repouso são criptografados nos volumes EBS e S3 com chaves gerenciadas pela AWS.

Caso você revogue este consentimento posteriormente, a continuidade do uso do aplicativo poderá ficar inviabilizada — neste caso, sua conta poderá ser desativada e seus dados pessoais excluídos mediante solicitação, conforme detalhado na Seção 8.

## 7. Por quanto tempo guardamos os dados

| Categoria | Período de retenção |
|---|---|
| Dados de conta ativa (telefone, nome, perfil) | Enquanto a conta estiver ativa |
| Dados de conta desativada | 6 meses, para fins de auditoria, prevenção a fraudes e cumprimento de obrigações tributárias e regulatórias; após esse prazo, exclusão definitiva |
| Histórico de buscas (anônimo agregado) | Indefinido (dados agregados, não identificáveis individualmente) |
| Relatórios de erro (Sentry) | 90 dias |
| Logs de servidor (CloudWatch) | 30 dias |

A retenção pós-encerramento de conta funda-se no art. 16, inciso I (cumprimento de obrigação legal), II (estudo por órgão de pesquisa, garantida a anonimização) e III (transferência a terceiro, mediante requisitos legais), bem como no legítimo interesse de prevenção a fraudes (art. 7º, IX, c/c art. 10).

## 8. Seus direitos

Conforme os artigos 17 a 22 da LGPD, você pode exercer os seguintes direitos a qualquer momento:

- **Confirmação** da existência de tratamento de seus dados;
- **Acesso** aos dados que mantemos sobre você;
- **Correção** de dados incompletos, inexatos ou desatualizados;
- **Anonimização, bloqueio ou eliminação** de dados desnecessários, excessivos ou tratados em desconformidade com a LGPD;
- **Portabilidade** dos dados a outro fornecedor de serviço;
- **Eliminação** dos dados pessoais tratados com base em seu consentimento, observadas as hipóteses previstas no art. 16 da LGPD;
- **Informação** sobre as entidades públicas e privadas com as quais compartilhamos seus dados;
- **Revogação do consentimento**, nos termos do § 5º do art. 8º da LGPD.

Para exercer qualquer destes direitos, envie um email para [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br) com o assunto **"[LGPD] Solicitação"**. Buscamos responder em até **15 dias** corridos a contar do recebimento, conforme prazo recomendado pela ANPD.

## 9. Segurança da informação e notificação de incidentes

Adotamos medidas técnicas e administrativas para proteger os dados pessoais contra acessos não autorizados e situações acidentais ou ilícitas de destruição, perda, alteração, comunicação ou difusão, em conformidade com o art. 46 da LGPD. Entre essas medidas:

- Criptografia em trânsito (TLS 1.2 ou superior) e em repouso (EBS, S3, RDS) para todos os dados pessoais;
- Autenticação JWT com rotação de tokens, autenticação multifatorial nos consoles administrativos da AWS e GitHub;
- Princípio do menor privilégio aplicado às credenciais de infraestrutura, gerenciadas via IAM Roles e federações OIDC;
- Banco de dados sem exposição pública à internet, acessível apenas via VPC privada;
- Monitoramento contínuo de erros (Sentry), métricas de latência e logs auditáveis (CloudWatch).

**Notificação de incidentes (LGPD art. 48):** caso ocorra incidente de segurança que possa acarretar risco ou dano relevante aos titulares, comunicaremos a Autoridade Nacional de Proteção de Dados (ANPD) e os titulares afetados em prazo razoável, com as informações exigidas pelo § 1º do art. 48 da LGPD. A comunicação aos titulares será feita via SMS para o telefone cadastrado, complementarmente por email quando disponível, e por aviso no próprio aplicativo.

## 10. Cookies e tecnologias similares

Atualmente o QuemFaz não utiliza cookies — o serviço é exclusivamente um aplicativo móvel (Android/iOS), sem versão web. Caso uma versão web seja lançada no futuro, esta política será atualizada e você será notificado dentro do aplicativo solicitando aceite expresso da nova versão.

## 11. Alterações nesta política

Quando alterações materiais forem feitas, o número da versão no topo desta página será atualizado e você será notificado dentro do aplicativo solicitando aceite expresso da nova versão antes de continuar a usar o serviço. Versões anteriores ficam arquivadas no histórico público do repositório do site, garantindo a transparência do tratamento ao longo do tempo.

## 12. Como entrar em contato

- **Suporte / dúvidas gerais:** [suporte@quemfaz.com.br](mailto:suporte@quemfaz.com.br)
- **Solicitações relativas a dados pessoais (LGPD):** mesmo email, com o assunto **"[LGPD] Solicitação"**
- **Encarregado pelo Tratamento de Dados (DPO):** mesmo email, com o assunto **"[LGPD] DPO"**
- **Autoridade Nacional de Proteção de Dados (ANPD):** [www.gov.br/anpd](https://www.gov.br/anpd) — você tem o direito de fazer reclamações diretamente à ANPD se entender que seus direitos não foram atendidos.
