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

Clonar el repositorio: 
<pre>
    <code>
git clone https://github.com/wvverez/ZENLDAP.git
cd ZENLDAP.git
    </code>
</pre>


## 🖇️ Parámetros principales:

| Parámetro | Descripción |
|--------|-------------|
| `LDAPath` | Ruta LDAP con el DN base  |
| `Username` | Usuario de dominio   |
| `Password` | Contraseña de usuario  |
| `AuthType` | Tipo de autenticación: Secure, SocketsLayer   |
| `OutputPath` | Carpeta donde se guardarán los CSV   |

## 🗂️ Archivos generados

El script exporta automáticamente los siguientes reportes:

| Parámetro | Descripción |
|--------|-------------|
| `domain_groups.csv` | Listado de grupos y sus miembros  |
| `domain_users.csv` | Usuarios, correos, UAC, último inicio   |
| `domain_computers.csv` | Equipos y SO detectado  |
| `domain_policy.csv` | Parámetros clave de la política de contraseñas   |

Estos archivos pueden abrirse en Excel, PowerBI o cualquier herramienta SIEM/SOC

## 🔑 QUE INFORMACIÓN OBTIENE

🔷 Grupos (objectClass=group)
-Nombre del grupo
-Descripción 
-Miembros

🔷 Usuarios (objectClass=user)
-Nombre
-Correo
-Último inicio (lastLogonTimestamp)
-Cuenta dehsbilitada
-Contraseña nunca expira


🔷 Equipos (objectClass=computer)
-Nombre del equipo
-Sistema operativo
-Último inicio 

🔷 Política de dominio (domainsDNS)
-Longitud mínima de contraseña
-Umbral de bloqueo
-Edad máxima de contraseña 

## 🫸 Cómo ejecutarlo paso a paso 

1. Abrir PowerShell como administrador
2. Permitir ejecución de scripts si es necesario:

   <pre>
       <code>
Set-Execution Policy Bypass -Scope Process
       </code>
   </pre>

3. Ejecutar el script con los parámetros deseados:

<pre>
    <code>
   .\script.ps1 -LDAPPath "LDAP://DC=empresa,DC=com"
    </code>
</pre>

## ⚠️ Advertencia legal 

Este script es únicamente para fines educativos y auditorías en redes donde tengas autorización. El uso inapropiado no solo sería poco ético si no que además puede violar leyes de privacidad y seguridad informática. 


## 🤝 Contribuciones
Las contribuciones son bienvenidas! Puedes abrir un issue o un pull request.

## 🗣️💬 Contacto en caso de fallos





   
