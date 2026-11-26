## Autorizaciones 

# Aplicacion dedicada a la autorizacion de sercivios de salud.
  Esta permite registrar, consultar, editar y eliminar(soft) autorizaciones medicas, administrar sus servicios asociados y calcular los montos correspondientes a cada participante (El cual es un tipo de gestor de autorizaciones).

# Features:
  - Creacion de autorizaciones medicas.
  - Actualizacion de autorizaciones medicas.
  - Consulta de autorizaciones medicas.
  - Consoluta detallada de Autorizaciones medicas por (ID,      
    codigo).
  - Eliminacion de autorizaciones medicas (soft, IsActive).

# Entidades
  - Autorizaciones
  - AutorizacionesDetalles
  - Afiliados
  - Intermediarios
  - Prestadores
  - Contratantes
  - TiposPrestadores
  - Tipos
  - Servicios
  
# Reglas de negocio
- Toda autorización deberá contener al menos un servicio        
  asociado.
- Cada servicio tendrá un monto reclamado.
- La ARS cubrirá el 70 % del monto reclamado y el afiliado 
  asumirá el 30 % restante.
- Los montos deberán ser consistentes y no podrán ser negativos.
- No podrán registrarse autorizaciones asociadas a entidades 
  inexistentes.
- Las autorizaciones inactivadas deberán conservarse para fines 
  históricos.
- Las operaciones deberán mantener la consistencia de la 
  información, incluso cuando ocurran errores o solicitudes simultáneas.
- No deberán generarse autorizaciones duplicadas como 
  consecuencia de solicitudes repetidas.
- La solución deberá permitir modificar en el futuro las reglas 
  de distribución de montos sin requerir cambios extensivos.

# Tecnologias utilizadas:
  .Net 10
  Entity Framework Core
  SQL Server
  Fluent Validation
  Docker
  kubernetes
