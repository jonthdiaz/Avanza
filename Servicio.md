#Avanza Servicio 

##Operaciones realizadas por los usuarios en el servicio

+ **Promotor**
    1. Personsa
    2. Microemprsa
    3. Conyugue (si existe)
    4. Solicitud
    5. Solicitud viabilidad
    6. Solicitud Referencias
        1. Zonales 
        2. Comerciales
    7. Solicitud referencias Zonales

+ **Analista**
    * Proceso 1
        1. Persona
        2. Microempresa
        3. Conyugue (si existe)
        4. Solicitud
        5. Solicitud viabilidad comercial
        6. Solicitud referencias
            1. Zonales
            2. Comerciales
        7. Solicitud Referencias zonales
        8. Solicitud Datos PYG
        9. Solicitud Datos Balance
        10. Solicitud datos adicionales
    * Proceso 2
        1. Solicitud referencias
            1. Zonales
            2. Comerciales (son las mismas del promotor)
        2. Solicitud referencias zonales
        3. Solicitud datos PYG
        4. Solicitud datos balance
        5. solicitud datos adicionales

Estas serian las tablas que se permiten sincronizar por cada perfil.

###Proceso
El promotor crea la información en las pantallas de cliente, viabilidad y solicitud, despues de esto sincroniza la información para que el coordinador asigne un analista en campo,  el cual va continuar con la operación.

Despues de la sincronización del promotor el analista puede obtener la información de las operaciones que el coordinador ha asignado a él.


##Operaciones del servicio para la obtención de información por parte del analista

Se creo una nueva operación en el servicio.

```shell
  _AvanzaService.ObtenerOperacionesAnalista();
```
Devuelve una lista de 

```shell
    List<SolicitudEntitiesDTO>
```

que contiene las siguientes propiedades

```shell
PersonasDTO 
MicroempresaDTO 
SolicitudCreditoDTO 
SolicitudViabilidadComercialDTO 
ConyugueDTO 
SolicitudDatosPYG_DTO 
SolicitudDatosBalanceDTO 
List<SolicitudReferenciasDTO> 
List<SolicitudReferenciasZonalesDTO> 
```

cada una de estas entidades contiene la informacion que se debe actualizar en la aplicación fuera de linea.
