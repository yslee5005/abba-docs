---
layout: default
title: Política de Privacidad — Abba
---

# Política de Privacidad

**Última actualización: 22 de abril de 2026**

## 1. Introducción

Abba («nosotros», «nuestro», «la aplicación») es una aplicación móvil compañera de oración y Tiempo a Solas (Quiet Time) creada para cristianos que desean orar más profundamente. Esta Política de Privacidad describe cómo Abba recopila, utiliza, almacena y protege su información cuando usa la aplicación para iOS (Bundle ID: `com.ystech.abba`).

Abba se opera actualmente como un proyecto de desarrollador independiente. Cuando nos referimos a «nosotros» en esta política, nos referimos al equipo de Abba. Si Abba se convierte en una empresa registrada en el futuro, esta política se actualizará en consecuencia.

Esta política se aplica en todo el mundo. Seguimos los principios del Reglamento General de Protección de Datos de la UE (RGPD), la Ley de Privacidad del Consumidor de California (CCPA) y la Ley de Protección de Información Personal de Corea (PIPA), donde sea aplicable.

## 2. Información que recopilamos

### 2.1 Información de la cuenta
Abba es **anónimo por defecto**. Cuando abre la aplicación por primera vez, creamos un ID de usuario anónimo (UUID) para que sus oraciones y ajustes puedan sincronizarse entre sesiones. No necesita proporcionar un nombre, correo electrónico o número de teléfono para usar Abba.

Opcionalmente, puede iniciar sesión con **Apple Sign-In** o **Google Sign-In** para respaldar sus datos. En ese caso, recibimos su dirección de correo electrónico y un identificador único de Apple o Google. Puede usar «Ocultar mi correo electrónico» con Apple Sign-In si lo prefiere.

### 2.2 Contenido de oraciones (datos principales)
Cuando usa Abba, recopilamos:
- **Grabaciones de audio** de sus oraciones habladas
- **Transcripciones** generadas a partir de esas grabaciones
- **Textos de meditación y reflexiones** que escribe o genera
- **Pasajes bíblicos** que marca como favoritos

Estos son los datos más sensibles que maneja Abba, y los tratamos con cuidado. Su audio se almacena en su propia carpeta privada en nuestro almacenamiento seguro. Solo usted puede acceder a él. No lo escuchamos, compartimos ni utilizamos con fines de marketing.

### 2.3 Información de suscripción
Si se suscribe a Abba Pro, un servicio de terceros llamado **RevenueCat** registra su estado de suscripción (activa, expirada, prueba, etc.) junto con el ID anónimo. **No** recibimos el número de su tarjeta de crédito — ese permanece con Apple.

### 2.4 Información técnica
- Idioma del dispositivo (para establecer su idioma predeterminado de la aplicación)
- Registros de fallos con datos personales enmascarados (vía Sentry)
- Token de notificación push (FCM, opcional — solo si habilita las notificaciones)
- Versión de la aplicación y versión de iOS (para depuración)

## 3. Cómo usamos su información

Usamos su información para:
- **Proporcionar análisis de IA** de sus oraciones y reflexiones de Tiempo a Solas (Google Gemini)
- **Sincronizar sus datos** entre sesiones y dispositivos
- **Gestionar su suscripción** y derechos
- **Corregir errores y mejorar la aplicación** mediante informes de fallos
- **Enviar notificaciones push opcionales** (recordatorios diarios de Tiempo a Solas) si usted lo acepta

**No**:
- Mostramos publicidad de ningún tipo
- Vendemos sus datos a nadie
- Compartimos el contenido de sus oraciones con terceros (excepto el procesamiento de IA descrito a continuación)
- Usamos su contenido para entrenar modelos de IA

## 4. Servicios de terceros

Abba se basa en un pequeño número de servicios de confianza para operar.

| Servicio | Propósito | Datos enviados | Región |
|---|---|---|---|
| **Supabase** | Base de datos y autenticación | ID anónimo, oraciones, metadatos | EE. UU. / UE |
| **Google Gemini API** | Análisis de IA de oraciones | Solo texto de oración | Google Cloud |
| **RevenueCat** | Gestión de suscripciones | ID anónimo, recibos de compra | EE. UU. |
| **Sentry** | Informes de fallos (PII enmascarada) | Trazas de error sin correos, transcripciones largas, JWT eliminados | EE. UU. / UE |
| **Firebase Cloud Messaging** | Notificaciones push (opcional) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Vinculación de cuenta opcional | Correo, ID del proveedor | Apple / Google |

**Google Gemini:** Según la política publicada por Google para el uso de API de pago, el contenido de oraciones enviado a Gemini **no se utiliza para entrenar los modelos de IA de Google**. El procesamiento es transitorio.

**Enmascaramiento PII de Sentry:** Aplicamos reglas de enmascaramiento antes de enviar los informes de fallos — los correos electrónicos, transcripciones coreanas de más de 50 caracteres, JWT y otros identificadores se eliminan.

## 5. Almacenamiento y seguridad de datos

- Todos los datos en tránsito están cifrados mediante HTTPS (TLS 1.2+).
- Los datos en reposo están protegidos por el cifrado de nuestro proveedor de base de datos.
- La **Seguridad a Nivel de Fila (RLS)** en Supabase garantiza que solo pueda acceder a sus propios datos.
- Los archivos de audio se almacenan en carpetas por usuario con acceso controlado por su token de autenticación.
- Los tokens de acceso se almacenan en el Secure Enclave de iOS (`flutter_secure_storage`), nunca en preferencias en texto plano.

Retenemos sus datos mientras su cuenta esté activa. Si elimina su cuenta, eliminamos sus datos en un plazo de **30 días**, excepto cuando estamos legalmente obligados a conservar registros (como registros fiscales de compras de suscripción, que Apple/RevenueCat conservan según sus propias políticas).

## 6. Sus derechos

Usted tiene los siguientes derechos sobre sus datos personales:

- **Acceso** — solicitar una copia de los datos que tenemos sobre usted
- **Rectificación** — pedirnos que corrijamos información inexacta
- **Supresión** — pedirnos que eliminemos su cuenta y datos (disponible en la aplicación: Ajustes → Cuenta → Eliminar cuenta, o por correo)
- **Portabilidad** — solicitar una exportación de sus datos en formato legible por máquina
- **Oposición** — oponerse a ciertos tratamientos
- **Retirar el consentimiento** — puede revocar el consentimiento para notificaciones push, procesamiento de IA o vinculación de cuentas en cualquier momento

Para los residentes del RGPD (UE) y CCPA (California), estos derechos están garantizados por la ley. Para ejercer cualquier derecho, envíe un correo a **rrallvv@gmail.com**. Respondemos en un plazo de 30 días.

## 7. Privacidad de los menores

Abba tiene clasificación 4+ en la App Store. No recopilamos conscientemente información de niños menores de 13 años (COPPA) o menores de 16 años (RGPD, en algunos países de la UE) sin consentimiento parental verificable. Si cree que un menor ha proporcionado información personal, contáctenos y la eliminaremos inmediatamente.

## 8. Transferencias internacionales de datos

Nuestra infraestructura está alojada en Estados Unidos y la Unión Europea. Al usar Abba, consiente que sus datos sean transferidos y procesados en estas regiones. Nos basamos en Cláusulas Contractuales Estándar (CCE) cuando se requieran.

## 9. Solicitudes gubernamentales y legales

Divulgamos datos de usuarios solo cuando lo exige la ley (citación válida, orden judicial o equivalente). Aún no publicamos informe de transparencia, pero nos comprometemos a notificar a los usuarios afectados cuando la ley lo permita.

## 10. Cambios en esta política

Podemos actualizar esta Política de Privacidad a medida que Abba evolucione. Cuando hagamos cambios sustanciales, se lo notificaremos en la aplicación y actualizaremos la fecha de «Última actualización» en la parte superior. El uso continuado de Abba tras los cambios significa que acepta la política actualizada.

## 11. Contáctenos

¿Preguntas, solicitudes o quejas?

- **Correo electrónico:** rrallvv@gmail.com
- **Tiempo de respuesta:** en un plazo de 30 días (generalmente antes)

También tiene derecho a presentar una queja ante su autoridad local de protección de datos (por ejemplo, la APD de su estado miembro de la UE, el Fiscal General de California o la PIPC de Corea).

---

⚠️ **Aviso de traducción**: Esta es una traducción proporcionada por conveniencia. En caso de discrepancia, prevalecerá la [versión en inglés](../privacy.html).
