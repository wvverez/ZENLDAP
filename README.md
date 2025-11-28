## 🛜🔐 ZENLDAP

LDAP en AD es el protocolo estándar utilizado para buscar, administrar y acceder a la información almacenada en el directorio, como usuarios ,grupos y equipos. Facilita la comunicación entre aplicaciones y AD.
<img width="552" height="316" alt="image" src="https://github.com/user-attachments/assets/96a99f11-6dcd-40fd-873b-51ef2524b9c8" />
Este repositorio contiene un script echo en powershell diseñado para enumerar consultas de AD usando consultas LDAP paginadas.

## 🔎 Extrae información de:
🧬Grupos del dominio

👥Usuarios 

💻Equipos 

📔Política principal del dominio (password policy)

y exporta todo en archivos CSV.

## 📭 Características principales

↪️ Conexión LDAP autenticada (Secure/ LDAPS)

↪️ Consultas paginadas para dominios grandes 

↪️ Exportación a CSV por categoría 

↪️ Compatible con entornos Windows, PowerShell 5+ y .NET


## 📌 Requisitos previos
🔐 Windows PowerShell 5.1+

🧨 Permisos para leer Active Directory (no requiere privilegios especiales)

💻 Conectividad a un DC vía:

    ·LDAP(389) o
    ·LDAPS (636) si se usa SecureSocketsLayer

## 🔋 Instalación 

