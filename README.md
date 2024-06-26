> [!IMPORTANT]
> 
> By using this project, you acknowledge and agree that the [Minecraft EULA](https://account.mojang.com/documents/minecraft_eula) is automatically set to TRUE.
>
> 使用本项目即表示您承认并同意 [Minecraft EULA](https://account.mojang.com/documents/minecraft_eula) 已自动设置为 TRUE。

<div align="center">
	<img src="https://github.com/OPDMC/1.19.2-OPDModCreate/raw/main/docs/%23README/icon_320.png" width="20%"/>
    <h1>1.19.2-OPDModCreate <code>v1.2</code></h1>
	<a href='https://github.com/OPDMC/1.19.2-OPDModCreate'><img src="https://img.shields.io/badge/-GitHub-3A3A3A?style=flat&amp;logo=GitHub&amp;logoColor=white" referrerpolicy="no-referrer" alt="GitHub"></a>
	<a href='https://github.com/OPDMC/1.19.2-OPDModCreate/pkgs/container/1.19.2-opdmodcreate'><img src="https://img.shields.io/badge/Ghcr.io-v1.2-555555?labelColor=8957E5&style=flat&amp;logo=GitHub&amp;logoColor=white" referrerpolicy="no-referrer" alt="Ghcr.io"></a>
	<a href='https://hub.docker.com/r/opdmc/1.19.2-opdmodcreate'><img src="https://img.shields.io/badge/DockerHub-v1.2-555555?labelColor=1c90ed&style=flat&amp;logo=Docker&amp;logoColor=white" referrerpolicy="no-referrer" alt="DockerHub"></a>

![Docker Image Size](https://img.shields.io/docker/image-size/opdmc/1.19.2-opdmodcreate?arch=amd64&label=AMD64&color=006688) ![Docker Image Size](https://img.shields.io/docker/image-size/opdmc/1.19.2-opdmodcreate?arch=arm64&label=ARM64&color=008866)
  </tr>
</div>


## 1 Description

这是OPDMC群友自用的Docker化MC机械动力服务器。整合的插件/模组作者在下方的 `3 Reference` 中注明了，请尊重原作者版权。

This is a Dockerized Minecraft server specialized for Create Mod for personal use by OPDMC group members. The authors of the integrated plugins/mods are credited in the `3 Reference` section below. Please respect the original authors' copyrights.

### 1.1 Update Rule

版本号用 `vA.B` 表示 (eg: `v1.0`, `v1.1`, `v2.0`)，其中 `A` 的改变表示用 `-v /path/to/store/data:/minecraft` 挂载的持久性文件中需要手动做出一些改变。而 `B` 表示小版本更新，理论上 `v1.0` 可以直接升级到 `v1.1` 因为它们的大版本是相同的。

Version numbers are represented as `vA.B` (eg: `v1.0`, `v1.1`, `v2.0`), where changes to `A` indicate that some manual modifications are required in the persistent files mounted with `-v /path/to/store/data:/minecraft`. On the other hand, `B` represents minor version updates; theoretically, `v1.0` can be directly upgraded to `v1.1` because they share the same major version.

## 2 Usage

```shell
# DockerHub
docker pull opdmc/1.19.2-opdmodcreate:latest
# Ghcr.io
docker pull ghcr.io/opdmc/1.19.2-opdmodcreate:latest
```

```shell
docker run -d \
  --name=1.19.2-opdmodcreate \
  -p 127.0.0.1:80:25565/tcp \
  -v /path/to/store/data:/minecraft \
  opdmc/1.19.2-opdmodcreate
```

| Parameter                             | Function                                                        |                                  |
|---------------------------------------|-----------------------------------------------------------------|----------------------------------|
| `-p 127.0.0.1:80:25565/tcp`           | Minecraft server port                                           | MC服务器端口                          |
| `-v /path/to/store/data:/minecraft`   | To store data in local, auto initialize if `start.sh` NOT exist | 服务器文件映射路径, `start.sh` 存在时将不进行初始化 |

---

**`-v /path/to/store/data:/minecraft` The `bin` directory under contains scripts for other docker services (此路径下的 `bin` 目录包含其他 docker 服务脚本):**

- `docker_server.bat` Quick start MC server (快捷启动 MC 服务器)
- `docker_overviewer.bat` Compile Overviewer map (编译 Overviewer 地图)
- `frpc/frpc.bat` `frpc/frpc.toml` Quick start frpc proxy (快捷启动 frpc 代理)
- `frpc_sakure.bat` Quick start SakuraFrp proxy (快捷启动樱花 SakuraFrp 代理)


## 3 Reference

- **Fabric**
  - https://fabricmc.net/
- **Create-Fabric**
  - https://github.com/Creators-of-Create/Create
  - https://www.curseforge.com/minecraft/mc-mods/create-fabric
- **Apple Skin**
  - https://github.com/squeek502/AppleSkin
  - https://www.curseforge.com/minecraft/mc-mods/appleskin
- **Controlling**
  - https://github.com/jaredlll08/Controlling
  - https://www.curseforge.com/minecraft/mc-mods/controlling
- **Inventory Profiles Next (IPN) & libIPN & Fabric Language Kotlin**
  - https://github.com/blackd/Inventory-Profiles
  - https://www.curseforge.com/minecraft/mc-mods/inventory-profiles-next
  - https://github.com/blackd/libIPN
  - https://www.curseforge.com/minecraft/mc-mods/libipn
  - https://github.com/FabricMC/fabric-language-kotlin
  - https://www.curseforge.com/minecraft/mc-mods/fabric-language-kotlin
- **Iris Shaders**
  - https://github.com/IrisShaders/Iris
  - https://www.curseforge.com/minecraft/mc-mods/irisshaders
- **Jade**
  - https://github.com/Snownee/Jade
  - https://www.curseforge.com/minecraft/mc-mods/jade
- **Just Enough Items (JEI)**
  - https://github.com/mezz/JustEnoughItems
  - https://www.curseforge.com/minecraft/mc-mods/jei
- **Just Enough Resources (JER)**
  - https://github.com/way2muchnoise/JustEnoughResources
  - https://www.curseforge.com/minecraft/mc-mods/just-enough-resources-jer
- **Journey Map**
  - https://teamjm.github.io/journeymap-docs/latest/
  - https://www.curseforge.com/minecraft/mc-mods/journeymap
- **Mouse Tweaks**
  - https://github.com/YaLTeR/MouseTweaks
  - https://www.curseforge.com/minecraft/mc-mods/mouse-tweaks
- **Sodium-Fabric**
  - https://github.com/CaffeineMC/sodium-fabric
  - https://www.curseforge.com/minecraft/mc-mods/sodium
- **World Edit**
  - https://github.com/enginehub/WorldEdit
  - https://www.curseforge.com/minecraft/mc-mods/worldedit


## 4 License

By using this project, you agree to the Minecraft End User License Agreement (EULA). The EULA can be found at the following link: [Minecraft EULA](https://account.mojang.com/documents/minecraft_eula).  This project automatically sets the EULA to true in the Minecraft configuration. By continuing to use this project, you acknowledge that you have read, understood, and agreed to the terms of the Minecraft EULA.

使用本项目即表示您同意《Minecraft 最终用户许可协议》（EULA）。EULA 可通过以下链接查看：[Minecraft EULA](https://account.mojang.com/documents/minecraft_eula)。 本项目会自动在 Minecraft 配置中将 EULA 设置为 true。继续使用本项目即表示您已阅读、理解并同意 Minecraft EULA 的条款。

Apache License 2.0
