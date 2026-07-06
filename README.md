# Base-de-datos-para-Consultorios-Medicos
📝Proyecto académico:

⚕️Sistema de Gestión para Consultorio Médico.

🧑‍🎓Contexto Académico:
 Este sistema fue desarrollado para la materia Base de datos II de la
 Tecnicatura Universitaria en Programación de la UTN-FRGP en el año 2026 por los integrantes:
- Guillermo Ezequiel Hernández.
- Máximo Rinaldelli.

⚙️ Descripción
La base permite a los usuarios:

- Sacar turnos médicos según el consultorio y las especialidades.
- Ver los médicos disponibles según direcciones y especialidades.
- Ver las obras sociales que atienden los doctores.
- Cancelar y reagendar turnos.

También respalda la lógica real de:
1. Doctores
2. Pacientes
3. Usuarios con sus roles
4. Consultorios
5. Obras Sociales
6. Especialidades médicas
7. Turnos médicos
   
🔧Funciones del sistema.

Procedimientos almacenados:

- sp_CancelarTurnos. -> Permite al paciente cancelar turnos correctamente.

- sp_FiltrarxEspecialidad. -> Permite que el paciente busque una especialidad médica y el sistema muestre los doctores y sus consultorios disponibles para esta.

- sp_AgendarTurno -> Permite al paciente agendar un turno para una fecha con un doctor y horario específico.

Triggers:

- TR_ImpedirTurnoDoble. -> Impide que haya dos turnos para un mismo horario.

- tr_CheckDoctorActivo. -> Revisa que el doctor solicitado se encuentre activo para atender.

- TR_ValidarCoberturaTurno. -> Valida que el doctor solicitado atienda la obra social del paciente.

Vistas:

- vw_TurnosDelDia. -> Muestra los turnos agendados para el día ingresado.

- vw_ConsultoriosxDoctor. -> Muestra la dirección de los consultorios en donde atiende cada doctor.

- vw_ObraSocialxDoctor -> Muestra qué obras sociales atiende cada doctor.

Se recomienda, antes de comenzar a probar la base de datos, cargar primero los valores de la sección de "Inserts de ejemplo" para corroborar que todo funcione correctamente.
