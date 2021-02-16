---- Minecraft Crash Report ----
// Uh... Did I do that?

Time: 2/16/21 3:45 AM
Description: Initializing game

java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'imm_ptl_core'!
	at Not Enough Crashes deobfuscated stack trace.(1.16.5+build.4)
	at net.fabricmc.loader.entrypoint.minecraft.hooks.EntrypointUtils.invoke0(EntrypointUtils.java:53)
	at net.fabricmc.loader.entrypoint.minecraft.hooks.EntrypointUtils.invoke(EntrypointUtils.java:36)
	at net.fabricmc.loader.entrypoint.minecraft.hooks.EntrypointClient.start(EntrypointClient.java:33)
	at net.minecraft.client.MinecraftClient.redirect$bab000$catchFabricInit(MinecraftClient:8377)
	at net.minecraft.client.MinecraftClient.<init>(MinecraftClient:437)
	at net.minecraft.client.main.Main.main(Main:177)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at net.fabricmc.loader.game.MinecraftGameProvider.launch(MinecraftGameProvider.java:226)
	at net.fabricmc.loader.launch.knot.Knot.init(Knot.java:139)
	at net.fabricmc.loader.launch.knot.KnotClient.main(KnotClient.java:27)
Caused by: java.lang.NoClassDefFoundError: me/jellysquid/mods/sodium/client/SodiumHooks
	at com.qouteall.hiding_in_the_bushes.sodium_compatibility.SodiumInterfaceInitializer.init(SodiumInterfaceInitializer.java:32)
	at com.qouteall.hiding_in_the_bushes.ModEntryClient.onInitializeClient(ModEntryClient.java:71)
	at net.fabricmc.loader.entrypoint.minecraft.hooks.EntrypointClient$$Lambda$2588/1910004563.accept(Unknown Source)
	at net.fabricmc.loader.entrypoint.minecraft.hooks.EntrypointUtils.invoke0(EntrypointUtils.java:50)
	... 12 more
Caused by: java.lang.ClassNotFoundException: me.jellysquid.mods.sodium.client.SodiumHooks
	at java.net.URLClassLoader.findClass(URLClassLoader.java:381)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:424)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:331)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:357)
	at net.fabricmc.loader.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:168)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:357)
	... 16 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Initialization --
Details:
Stacktrace:
	at fudge.notenoughcrashes.mixinhandlers.EntryPointCatcher.handleEntryPointError(EntryPointCatcher.java:31)
	at net.minecraft.class_310.redirect$bab000$catchFabricInit(class_310.java:8379)
	at net.minecraft.class_310.<init>(class_310.java:437)
	at net.minecraft.client.main.Main.main(Main.java:177)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at net.fabricmc.loader.game.MinecraftGameProvider.launch(MinecraftGameProvider.java:226)
	at net.fabricmc.loader.launch.knot.Knot.init(Knot.java:139)
	at net.fabricmc.loader.launch.knot.KnotClient.main(KnotClient.java:27)
-- System Details --
Details:
	Minecraft Version: 1.16.5
	Minecraft Version ID: 1.16.5
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_51, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 2475583104 bytes (2360 MB) / 4026531840 bytes (3840 MB) up to 5368709120 bytes (5120 MB)
	CPUs: 16
	JVM Flags: 9 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xss1M -Xmx5G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
	Suspected Mods: Fabric Loader (fabricloader), Immersive Portals Core (imm_ptl_core)
	Fabric Mods: 
		appleskin: AppleSkin 1.0.11
		autoconfig1u: Auto Config v1 Updated 3.3.1
		chunkpregen: Fabric Chunk Pregenerator 0.3.3
		cloth-basic-math: Cloth Basic Math 0.5.1
		cloth-client-events-v0: Cloth Client Events v0 1.5.47
		cloth-config2: Cloth Config v4 4.10.13
		com_moandjiezana_toml_toml4j: toml4j 0.7.2
		ctm: ConnectedTexturesMod for Fabric 0.3.0
		dynamicfps: Dynamic FPS 2.0.1
		fabric: Fabric API 0.30.0+1.16
		fabric-api-base: Fabric API Base 0.2.0+daa38b3d7d
		fabric-biome-api-v1: Fabric Biome API (v1) 3.1.1+ca58154a7d
		fabric-blockrenderlayer-v1: Fabric BlockRenderLayer Registration (v1) 1.1.5+ca58154a7d
		fabric-command-api-v1: Fabric Command API (v1) 1.0.10+ca58154a7d
		fabric-commands-v0: Fabric Commands (v0) 0.2.2+ca58154a7d
		fabric-containers-v0: Fabric Containers (v0) 0.1.10+ca58154a7d
		fabric-content-registries-v0: Fabric Content Registries (v0) 0.2.1+ca58154a7d
		fabric-crash-report-info-v1: Fabric Crash Report Info (v1) 0.1.3+ca58154a7d
		fabric-dimensions-v1: fabric-dimensions-v1 2.0.2+ca58154a7d
		fabric-entity-events-v1: Fabric Entity Events (v1) 1.0.3+ca58154a7d
		fabric-events-interaction-v0: Fabric Events Interaction (v0) 0.4.2+ca58154a7d
		fabric-events-lifecycle-v0: Fabric Events Lifecycle (v0) 0.2.1+ca58154a7d
		fabric-game-rule-api-v1: Fabric Game Rule API (v1) 1.0.6+ca58154a7d
		fabric-item-api-v1: Fabric Item API (v1) 1.2.1+ca58154a7d
		fabric-item-groups-v0: Fabric Item Groups (v0) 0.2.3+ca58154a7d
		fabric-key-binding-api-v1: Fabric Key Binding API (v1) 1.0.2+ca58154a7d
		fabric-keybindings-v0: Fabric Key Bindings (v0) 0.2.1+ca58154a7d
		fabric-lifecycle-events-v1: Fabric Lifecycle Events (v1) 1.2.1+ca58154a7d
		fabric-loot-tables-v1: Fabric Loot Tables (v1) 1.0.2+ca58154a7d
		fabric-mining-levels-v0: Fabric Mining Levels (v0) 0.1.3+ca58154a7d
		fabric-models-v0: Fabric Models (v0) 0.2.1+ca58154a7d
		fabric-networking-api-v1: Fabric Networking API (v1) 1.0.1+ca58154a7d
		fabric-networking-blockentity-v0: Fabric Networking Block Entity (v0) 0.2.8+ca58154a7d
		fabric-networking-v0: Fabric Networking (v0) 0.3.2+ca58154a7d
		fabric-object-builder-api-v1: Fabric Object Builder API (v1) 1.9.3+ca58154a7d
		fabric-object-builders-v0: Fabric Object Builders (v0) 0.7.2+ca58154a7d
		fabric-particles-v1: Fabric Particles (v1) 0.2.4+ca58154a7d
		fabric-registry-sync-v0: Fabric Registry Sync (v0) 0.7.4+ca58154a7d
		fabric-renderer-api-v1: Fabric Renderer API (v1) 0.4.1+ca58154a7d
		fabric-renderer-indigo: Fabric Renderer - Indigo 0.4.4+ca58154a7d
		fabric-renderer-registries-v1: Fabric Renderer Registries (v1) 2.2.1+ca58154a7d
		fabric-rendering-data-attachment-v1: Fabric Rendering Data Attachment (v1) 0.1.5+ca58154a7d
		fabric-rendering-fluids-v1: Fabric Rendering Fluids (v1) 0.1.13+ca58154a7d
		fabric-rendering-v0: Fabric Rendering (v0) 1.1.2+ca58154a7d
		fabric-rendering-v1: Fabric Rendering (v1) 1.5.1+ca58154a7d
		fabric-resource-loader-v0: Fabric Resource Loader (v0) 0.4.2+ca58154a7d
		fabric-screen-api-v1: Fabric Screen API (v1) 1.0.0+c045166c7d
		fabric-screen-handler-api-v1: Fabric Screen Handler API (v1) 1.1.1+ca58154a7d
		fabric-structure-api-v1: Fabric Structure API (v1) 1.1.4+ca58154a7d
		fabric-tag-extensions-v0: Fabric Tag Extensions (v0) 1.1.1+ca58154a7d
		fabric-textures-v0: Fabric Textures (v0) 1.0.6+ca58154a7d
		fabric-tool-attribute-api-v1: Fabric Tool Attribute API (v1) 1.2.6+ca58154a7d
		fabricloader: Fabric Loader 0.11.1
		imm_ptl_core: Immersive Portals Core 0.68
		immersive_portals: Immersive Portals 0.68
		java: Java HotSpot(TM) 64-Bit Server VM 8
		lambdynlights: LambDynamicLights 1.3.4+1.16
		lithium: Lithium 0.6.3
		logical_zoom: Logical Zoom 0.0.8
		minecraft: Minecraft 1.16.5
		modmenu: Mod Menu 1.16.7
		notenoughcrashes: Not Enough Crashes 3.1.5
		org_aperlambda_lambdajcommon: lambdajcommon 1.8.1
		phosphor: Phosphor 0.7.0+build.10
		pling: Pling 1.3.0
		roughlyenoughitems: Roughly Enough Items 5.10.181
		roughlyenoughitems-api: REI (API) 5.10.181
		roughlyenoughitems-default-plugin: REI (Default Plugin) 5.10.181
		roughlyenoughitems-runtime: REI (Runtime) 5.10.181
		sodium: Sodium 0.1.0
		spruceui: SpruceUI 2.0.4+1.16
		voxelmap: VoxelMap 1.10.15
		waila: Hwyla 1.9.22
	Launched Version: 1.16.5
	Backend library: LWJGL version 3.2.2 build 10
	Backend API: NO CONTEXT
	GL Caps: 
	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fabric'
	Type: Client (map_client.txt)
	CPU: <unknown>
