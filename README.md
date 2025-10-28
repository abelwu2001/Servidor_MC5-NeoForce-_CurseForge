# Actualizaciones del mod MC5-neoforge Medieval

## Pasos para actualizar cada version del mod en minecraft:


### Pasos fundamentales:
1. Crear un "download server pack" desde la curseforge la nueva versión.

2. Pasar las carpetas config, defaultconfigs y mods a la carpeta de la vieja versión.

3. "F:\Ser\server\SERVER_ONLY_MMC5_v24\server.properties" cambiar el nombre de la carpeta "world" [o con el nombre que tenga] por otro nuevo para un renicio total.

4. Iniciar el start.ps1 por primera vez, ya iniciado todo (comprobar con algún comando si inicio el mundo) cerramos el powershell.

5. Abrimos otra vez el powershell en el directorio de la carpeta con el server viejo (ya actualizado) y seguimos los siguientes items en orden:

- eliminación de librerias antiguas rmdir /s /q .\libraries del .\user_jvm_args.txt
[eliminar la carpeta libreries y el archivo user_jvm_args.txt]

- descarga de la nueva version de neoforce:
> [!NOTE]
> ```bash
> echo "Invoke-WebRequest -Uri https://maven.neoforged.net/releases/net/neoforged/neoforge/21.1.[version actual]/neoforge-21.1.[la version actual]-installer.jar -OutFile neoforge-installer.jar"
> ```

Modificar -----> [version actual]

- Instalacion

java -jar .\neoforge-installer.jar --installServer


- java -Xms4G -Xmx12G @libraries\net\neoforged\neoforge\21.1.211\win_args.txt nogui

Abrí eula.txt y poné eula=true. 

6. en "F:\Ser\server\SERVER_ONLY_MMC5_v24\variables.txt" 
MODLOADER=NeoForge
MODLOADER_VERSION=21.1.211

7. "F:\Ser\server\SERVER_ONLY_MMC5_v24\run.bat"
cambiar la referencia al 211 o la mas nueva

--- 

## PASOS POSTERIORES PARA MODIFICAR SEEDS O VALORES DE MODS EN GENERAL [Partidas nuevas]:

1. cambiar los valores de los siguientes archivos:
F:\Ser\server\SERVER_ONLY_MMC5_v24\config\paxi\datapacks\mmc_apotheosis\data
por esto:
https://drive.google.com/drive/folders/1wl_gRjC7YuPAmfvBZ8ETmutOPdvWgdLN

2. "F:\Ser\server\SERVER_ONLY_MMC5_v24\config\tectonic.json"
cambiar los valores del archivo por estos:
{
  "biomes": {
    "temperature_multiplier": 1.0,
    "temperature_offset": 0.0,
    "temperature_scale": 0.10,
    "vegetation_multiplier": 1.0,
    "vegetation_offset": 0.0,
    "vegetation_scale": 0.10
  },
  "continents": {
    "continents_scale": 0.13,
    "erosion_scale": 0.25,
    "flat_terrain_skew": 0.1,
    "jungle_pillars": true,
    "ocean_offset": -0.8,
    "ridge_scale": 0.25,
    "river_lanterns": true,
    "rolling_hills": true,
    "underground_rivers": true
  },
  "general": {
    "mod_enabled": true,
    "snow_start_offset": 128
  },
  "global_terrain": {
    "increased_height": false,
    "lava_tunnels": true,
    "ultrasmooth": false,
    "vertical_scale": 1.125
  },
  "islands": {
    "enabled": true,
    "noise_multiplier": 1.0,
    "noise_offset": 0.0,
    "noise_scale": 0.11
  },
  "minor_version": 1,
  "oceans": {
    "deep_ocean_depth": -1.10,
    "monument_offset": -30,
    "ocean_depth": -0.22,
    "remove_frozen_ocean_ice": false
  }
}

3. Nieve:

creando un nuevo mundo y desactivarlo en 0

---

## Datos extra

- Playit.gg para gente fuera de Argentina (Tunel Directo)

- Radmin VPN para Argentina

- Tutorial para pasar versiones en CurseForge: https://youtu.be/9dLMOiPp_Vk
