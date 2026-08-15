# Ritmo — Planner de equipo

Reglas fijas de este proyecto. Léelas antes de tocar código.

## Qué es
Planner de pendientes para un equipo chico en Perú. Cada persona ve sus propios
pendientes; quien entra como líder también ve el tablero del equipo.

## Decisiones fijas (no cambiar sin preguntar)

- **Sin login ni contraseñas.** Se entra solo escribiendo el nombre. La dueña del
  proyecto aceptó conscientemente el riesgo: cualquiera con el link puede entrar
  como cualquier persona del equipo. No agregar autenticación sin que ella lo pida.
- **Presupuesto: cero.** Solo usar servicios gratuitos (Supabase plan free, Vercel
  plan free). No sugerir upgrades pagos salvo que ella pregunte.
- **Sin restricción de residencia de datos.** El equipo está en Perú pero no hay
  obligación legal de que los datos vivan ahí. Cualquier región de Supabase/Vercel
  sirve.
- **Base de datos: Supabase**, tablas `people` y `tasks`. Como no hay login real,
  las políticas de acceso (RLS) son abiertas (permiten lectura y escritura con la
  llave pública `anon`). Esto es intencional, no un descuido.

## Tecnología

- Frontend: HTML + CSS + JavaScript simple (sin framework), tal como el prototipo
  original en `plannerequipo.html`.
- Base de datos: Supabase.
- Hosting: Vercel.

## Arnés de este proyecto

- Respaldo en GitHub: este mismo repositorio.
- Ambiente de prueba: proyecto Supabase separado para pruebas, antes de tocar el
  de producción (obligatorio porque la app guarda datos de otras personas).
- Revisión de seguridad antes de publicar (obligatoria por el mismo motivo).
- Sin pruebas automáticas ni hooks todavía; se agregan si ella los pide.
