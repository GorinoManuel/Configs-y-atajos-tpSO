# Configs-y-atajos-tpSO
git clone https://github.com/sisoputnfrba/so-deploy.git

cd so-deploy

./deploy.sh -r=release -p=utils -p=kernel -p=cpu -p=memoria -p=entradasalida "tp-2024-1c-LocosPorLaPromo"

git clone https://github.com/sisoputnfrba/c-comenta-pruebas.git

cd tp-2024-1c-LocosPorLaPromo

cd so-deploy/tp-2024-1c-LocosPorLaPromo

cd so-deploy/tp-2024-1c-LocosPorLaPromo/kernel

cd entradasalida

cd so-deploy/tp-2024-1c-LocosPorLaPromo/entradasalida

# PRUEBA_PLANI

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_PLANI

FINALIZAR_PROCESO 3

KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

SLP1: ./bin/entradasalida SLP1 ./SLP1.config

CPU: ./bin/cpu ./cpu.config

# PRUEBA_DEADLOCK

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_DEADLOCK

FINALIZAR_PROCESO X

KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

ESPERA: ./bin/entradasalida ESPERA ./ESPERA.config

CPU: ./bin/cpu ./cpu.config

# PRUEBA_MEMORIA

Ejecutar una con LRU y otra con FIFO en 1

INICIAR_PROCESO /scripts_memoria/MEMORIA_1

INICIAR_PROCESO /scripts_memoria/MEMORIA_2

INICIAR_PROCESO /scripts_memoria/MEMORIA_3

KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

IO_GEN_SLEEP: ./bin/entradasalida IO_GEN_SLEEP ./IO_GEN_SLEEP.config

CPU: ./bin/cpu ./cpu.config

# PRUEBA_IO

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_IO

Para IO_A (0):WAR NEVER CHANGES...

Para IO_C (2):Sistemas Operativos 1c2024


KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

ENTRADASALIDA: ./bin/entradasalida GENERICA ./GENERICA.config

               ./bin/entradasalida TECLADO ./TECLADO.config

               ./bin/entradasalida MONITOR ./MONITOR.config
               
CPU: ./bin/cpu ./cpu.config

# PRUEBA_FS

INICIAR_PROCESO /scripts_memoria/FS_1

INICIAR_PROCESO /scripts_memoria/FS_2

Escribir: Fallout 1 Fallout 2 Fallout 3 Fallout: New Vegas Fallout 4 Fallout 76

Terminar prueba parte 1

INICIAR_PROCESO /scripts_memoria/FS_3

INICIAR_PROCESO /scripts_memoria/FS_4

KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

ENTRADASALIDA: ./bin/entradasalida FS ./FS.config

               ./bin/entradasalida TECLADO ./TECLADO.config

               ./bin/entradasalida MONITOR ./MONITOR.config
               
CPU: ./bin/cpu ./cpu.config

# PRUEBA_SALVATIONS_EDGE

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_SALVATIONS_EDGE

MULTIPROGRAMACION 100


DETENER_PLANIFICACION

PROCESO_ESTADO

INICIAR_PLANIFICACION


KERNEL: ./bin/kernel ./kernel.config

MEMORIA: ./bin/memoria ./memoria.config

ENTRADASALIDA: ./bin/entradasalida GENERICA ./GENERICA.config

               ./bin/entradasalida TECLADO ./TECLADO.config

               ./bin/entradasalida MONITOR ./MONITOR.config

               ./bin/entradasalida ESPERA ./ESPERA.config

               ./bin/entradasalida SLP1 ./SLP1.config
               
CPU: ./bin/cpu ./cpu.config
