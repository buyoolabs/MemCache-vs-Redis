MemCache vs Redis
=================

  Gestión distribuida de cache. Hash saber que servidor puede contener la clave. Otro hash para saber en que punto esta en el determinado servidor.

###MemCache

- Memoria Ram y base de datos (memCacheDB) (persistente)
- Clave valor. Clave 250 caracteres. Valor hasta 1 Mb
  Valor -> datos base de datos, APIs o páginas.
- session asp.net
- Unofficial Wwindows Server -> versiones más antiguas y no soportadas ( <a href="http://memcachedproviders.codeplex.com/">Downloads</a> )
- Cliente .net 

###Redis

- Memoria Ram y base de datos (persistente)
- Clave-valor
- Transacción
- Búsqueda con patron
- Session asp.net
- Replicación
- Operaciones atómicas ricas
- Unofficial windows - versiones más antiguas
- Velocidad similar al session in-proc pero puede ser distribuida

   <a href="http://try.redis.io/">Breve Documentación</a>

##Comparativa

<a href="http://oldblog.antirez.com/post/redis-memcached-benchmark.html">Benchmark1</a>
<a href="http://alekseykorzun.com/post/53283070010/benchmarking-memcached-and-redis-clients">Benchmark2</a>
##Opinión

- No veo recomendable implementarlo en servidores Windows. No esta preparados inicialmentea para este tipo de sistemas, van retrasados en versiones y son no oficiales por lo que no habría soporte. Puede ser una fuente de problemas.

- Los dos sistemas en cuanto a rendimiento ofrecen buenas opciones. Algo mejor Redis pero no es muy notable.

- Para sistemas muy sencillos de aplicar clave-valor pueden aplicarse cualquiera de las dos soluciones. Pero a la hora de querer algo más avanzado es recomendable Redis. Es más completo y ofrece más posibilidades para el futuro (crecimiento).

- Los dos pueden funcionar con un solo servidor de cache, pero donde más beneficios pueden ofrecer es a la hora de tener una granja de servidores de cache (distribuido).

- Para buyoo a día de hoy, creo que se queda grande todo esto. En un futuro puede...
