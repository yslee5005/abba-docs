---
layout: default
title: Política de Privacidade — Abba
---

# Política de Privacidade

**Última atualização: 22 de abril de 2026**

## 1. Introdução

Abba («nós», «nosso», «o aplicativo») é um companheiro móvel de oração e Tempo Devocional (Quiet Time) criado para cristãos que desejam orar mais profundamente. Esta Política de Privacidade descreve como o Abba coleta, usa, armazena e protege suas informações quando você usa o aplicativo iOS (Bundle ID: `com.ystech.abba`).

O Abba é atualmente operado como um projeto de desenvolvedor independente. Quando nos referimos a «nós» nesta política, queremos dizer a equipe do Abba. Se o Abba se tornar uma empresa registrada no futuro, esta política será atualizada de acordo.

Esta política aplica-se em todo o mundo. Seguimos os princípios do Regulamento Geral de Proteção de Dados da UE (RGPD), da California Consumer Privacy Act (CCPA) e da Lei de Proteção de Informações Pessoais da Coreia (PIPA), onde aplicável.

## 2. Informações que coletamos

### 2.1 Informações da conta
O Abba é **anônimo por padrão**. Quando você abre o aplicativo pela primeira vez, criamos um ID de usuário anônimo (UUID) para que suas orações e configurações possam ser sincronizadas entre sessões. Você não precisa fornecer nome, e-mail ou número de telefone para usar o Abba.

Você pode, opcionalmente, entrar com **Apple Sign-In** ou **Google Sign-In** para fazer backup dos seus dados. Nesse caso, recebemos seu endereço de e-mail e um identificador único da Apple ou do Google. Você pode usar «Ocultar Meu E-mail» com o Apple Sign-In se preferir.

### 2.2 Conteúdo das orações (dados principais)
Quando você usa o Abba, coletamos:
- **Gravações de áudio** das suas orações faladas
- **Transcrições** geradas a partir dessas gravações
- **Textos de meditação e reflexões** que você escreve ou gera
- **Passagens bíblicas** que você marca como favoritas

Estes são os dados mais sensíveis que o Abba trata, e os tratamos com cuidado. Seu áudio é armazenado em sua própria pasta privada em nosso armazenamento seguro. Apenas você pode acessá-lo. Não o ouvimos, não o compartilhamos e não o usamos para marketing.

### 2.3 Informações de assinatura
Se você assinar o Abba Pro, um serviço terceirizado chamado **RevenueCat** registra seu status de assinatura (ativa, expirada, avaliação, etc.) junto com o ID anônimo. **Não** recebemos o número do seu cartão de crédito — ele permanece com a Apple.

### 2.4 Informações técnicas
- Idioma do dispositivo (para definir seu idioma padrão do aplicativo)
- Registros de falhas com dados pessoais mascarados (via Sentry)
- Token de notificação push (FCM, opcional — apenas se você habilitar notificações)
- Versão do aplicativo e versão do iOS (para depuração)

## 3. Como usamos suas informações

Usamos suas informações para:
- **Fornecer análise de IA** das suas orações e reflexões de Tempo Devocional (Google Gemini)
- **Sincronizar seus dados** entre sessões e dispositivos
- **Gerenciar sua assinatura** e direitos
- **Corrigir erros e melhorar o aplicativo** através de relatórios de falhas
- **Enviar notificações push opcionais** (lembretes diários de Tempo Devocional) se você aceitar

**Não**:
- Exibimos publicidade de qualquer tipo
- Vendemos seus dados a ninguém
- Compartilhamos o conteúdo das suas orações com terceiros (exceto o processamento de IA descrito abaixo)
- Usamos seu conteúdo para treinar modelos de IA

## 4. Serviços de terceiros

O Abba depende de um pequeno número de serviços confiáveis para funcionar.

| Serviço | Finalidade | Dados enviados | Região |
|---|---|---|---|
| **Supabase** | Banco de dados e autenticação | ID anônimo, orações, metadados | EUA / UE |
| **Google Gemini API** | Análise de IA de orações | Apenas texto da oração | Google Cloud |
| **RevenueCat** | Gerenciamento de assinaturas | ID anônimo, recibos de compra | EUA |
| **Sentry** | Relatórios de falhas (PII mascarada) | Rastreamentos de erro sem e-mails, transcrições longas, JWTs removidos | EUA / UE |
| **Firebase Cloud Messaging** | Notificações push (opcional) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Vinculação de conta opcional | E-mail, ID do provedor | Apple / Google |

**Google Gemini:** Conforme a política publicada do Google para uso pago da API, o conteúdo das orações enviado ao Gemini **não é usado para treinar os modelos de IA do Google**. O processamento é transitório.

**Mascaramento PII do Sentry:** Aplicamos regras de mascaramento antes de enviar relatórios de falhas — e-mails, transcrições coreanas com mais de 50 caracteres, JWTs e outros identificadores são removidos.

## 5. Armazenamento e segurança de dados

- Todos os dados em trânsito são criptografados via HTTPS (TLS 1.2+).
- Os dados em repouso são protegidos pela criptografia do nosso provedor de banco de dados.
- A **Row-Level Security (RLS)** no Supabase garante que você só possa acessar seus próprios dados.
- Arquivos de áudio são armazenados em pastas por usuário com acesso controlado pelo seu token de autenticação.
- Tokens de acesso são armazenados no Secure Enclave do iOS (`flutter_secure_storage`), nunca em preferências em texto puro.

Retemos seus dados enquanto sua conta estiver ativa. Se você excluir sua conta, removemos seus dados dentro de **30 dias**, exceto quando legalmente obrigados a manter registros (como registros fiscais de compras de assinatura, que Apple/RevenueCat mantêm conforme suas próprias políticas).

## 6. Seus direitos

Você tem os seguintes direitos sobre seus dados pessoais:

- **Acesso** — solicitar uma cópia dos dados que temos sobre você
- **Retificação** — pedir que corrijamos informações imprecisas
- **Exclusão** — pedir que excluamos sua conta e dados (disponível no app: Configurações → Conta → Excluir conta, ou por e-mail)
- **Portabilidade** — solicitar uma exportação dos seus dados em formato legível por máquina
- **Oposição** — opor-se a determinados processamentos
- **Retirar o consentimento** — você pode revogar o consentimento para notificações push, processamento de IA ou vinculação de contas a qualquer momento

Para residentes do RGPD (UE) e CCPA (Califórnia), esses direitos são garantidos por lei. Para exercer qualquer direito, envie um e-mail para **rrallvv@gmail.com**. Respondemos em até 30 dias.

## 7. Privacidade das crianças

O Abba é classificado 4+ na App Store. Não coletamos intencionalmente informações de crianças menores de 13 anos (COPPA) ou menores de 16 anos (RGPD, em alguns países da UE) sem consentimento parental verificável. Se você acredita que uma criança forneceu informações pessoais, entre em contato conosco e as excluiremos imediatamente.

## 8. Transferências internacionais de dados

Nossa infraestrutura está hospedada nos Estados Unidos e na União Europeia. Ao usar o Abba, você consente com a transferência e processamento dos seus dados nessas regiões. Baseamo-nos em Cláusulas Contratuais Padrão (SCCs) quando exigido.

## 9. Solicitações governamentais e legais

Divulgamos dados dos usuários apenas quando legalmente exigido (intimação válida, ordem judicial ou equivalente). Ainda não publicamos relatório de transparência, mas nos comprometemos a notificar os usuários afetados quando legalmente permitido.

## 10. Alterações nesta política

Podemos atualizar esta Política de Privacidade conforme o Abba evolui. Quando fizermos alterações substanciais, notificaremos você no aplicativo e atualizaremos a data de «Última atualização» no topo. O uso continuado do Abba após as alterações significa que você aceita a política atualizada.

## 11. Contacte-nos

Dúvidas, solicitações ou reclamações?

- **E-mail:** rrallvv@gmail.com
- **Tempo de resposta:** em até 30 dias (geralmente antes)

Você também tem o direito de apresentar reclamação à sua autoridade local de proteção de dados (por exemplo, a CNPD em Portugal, a ANPD no Brasil, a DPA do seu estado membro da UE, o Procurador-Geral da Califórnia ou a PIPC da Coreia).

---

⚠️ **Aviso de tradução**: Esta é uma tradução fornecida por conveniência. Em caso de discrepância, prevalecerá a [versão em inglês](../privacy.html).
