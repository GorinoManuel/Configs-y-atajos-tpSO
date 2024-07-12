# Configs-y-atajos-tpSO
git clone https://github.com/sisoputnfrba/so-deploy.git

cd so-deploy

./deploy.sh -r=release -p=utils -p=kernel -p=cpu -p=memoria -p=entradasalida "tp-2024-1c-LocosPorLaPromo"

git clone https://github.com/sisoputnfrba/c-comenta-pruebas.git


# PRUEBA_PLANI

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_PLANI

FINALIZAR_PROCESO 3

KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/kernel_FIFO.config

        ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/kernel_RR.config

        ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/kernel_VRR.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/memoria.config

SLP1: ./bin/entradasalida SLP1 ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/SLP1.config

CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_PLANI/cpu.config

# PRUEBA_DEADLOCK

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_DEADLOCK

FINALIZAR_PROCESO X

KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_DEADLOCK/kernel.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_DEADLOCK/memoria.config

ESPERA: ./bin/entradasalida ESPERA ../../Configs-y-atajos-tpSO/PRUEBA_DEADLOCK/ESPERA.config

CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_DEADLOCK/cpu.config

# PRUEBA_MEMORIA

Ejecutar una con LRU y otra con FIFO en 1

INICIAR_PROCESO /scripts_memoria/MEMORIA_1

INICIAR_PROCESO /scripts_memoria/MEMORIA_2

INICIAR_PROCESO /scripts_memoria/MEMORIA_3

KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_MEMORIA/kernel.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_MEMORIA/memoria.config

IO_GEN_SLEEP: ./bin/entradasalida IO_GEN_SLEEP ../../Configs-y-atajos-tpSO/PRUEBA_MEMORIA/IO_GEN_SLEEP.config

CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_MEMORIA/cpu_FIFO.config

     ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_MEMORIA/cpu_LRU.config

# PRUEBA_IO

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_IO

Para IO_A (0):WAR NEVER CHANGES...

Para IO_C (2):Sistemas Operativos 1c2024


KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_IO/kernel.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_IO/memoria.config

ENTRADASALIDA: ./bin/entradasalida GENERICA ../../Configs-y-atajos-tpSO/PRUEBA_IO/GENERICA.config

               ./bin/entradasalida TECLADO ../../Configs-y-atajos-tpSO/PRUEBA_IO/TECLADO.config

               ./bin/entradasalida MONITOR ../../Configs-y-atajos-tpSO/PRUEBA_IO/MONITOR.config
               
CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_IO/cpu.config

# PRUEBA_FS

INICIAR_PROCESO /scripts_memoria/FS_1

INICIAR_PROCESO /scripts_memoria/FS_2

Escribir: Fallout 1 Fallout 2 Fallout 3 Fallout: New Vegas Fallout 4 Fallout 76

Terminar prueba parte 1

INICIAR_PROCESO /scripts_memoria/FS_3

INICIAR_PROCESO /scripts_memoria/FS_4

KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_FS/kernel.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_FS/memoria.config

ENTRADASALIDA: ./bin/entradasalida FS ../../Configs-y-atajos-tpSO/PRUEBA_FS/FS.config

               ./bin/entradasalida TECLADO ../../Configs-y-atajos-tpSO/PRUEBA_FS/TECLADO.config

               ./bin/entradasalida MONITOR ../../Configs-y-atajos-tpSO/PRUEBA_FS/MONITOR.config
               
CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_FS/cpu.config

# PRUEBA_SALVATIONS_EDGE

EJECUTAR_SCRIPT ../../c-comenta-pruebas/scripts_kernel/PRUEBA_SALVATIONS_EDGE

MULTIPROGRAMACION 100


DETENER_PLANIFICACION

PROCESO_ESTADO

INICIAR_PLANIFICACION


KERNEL: ./bin/kernel ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/kernel.config

MEMORIA: ./bin/memoria ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/memoria.config

ENTRADASALIDA: ./bin/entradasalida GENERICA ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/GENERICA.config

               ./bin/entradasalida TECLADO ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/TECLADO.config

               ./bin/entradasalida MONITOR ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/MONITOR.config

               ./bin/entradasalida ESPERA ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/ESPERA.config

               ./bin/entradasalida SLP1 ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/SLP1.config
               
CPU: ./bin/cpu ../../Configs-y-atajos-tpSO/PRUEBA_SALVATIONS_EDGE/cpu.config
