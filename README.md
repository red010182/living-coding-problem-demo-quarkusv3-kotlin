# Live coding not work demo

1. Run the project with `mvn quarkus:dev`
2. Visit htpp://localhost:8080/hello
3. Edit code, for example, change return value from "Hello" to "hi"
4. Then you will see the following error:


```bash
java.lang.RuntimeException: Unable to invoke Kotlin compiler. java.lang.NoSuchMethodError: 'void org.jetbrains.kotlin.fir.extensions.FirExtensionRegistrar$Companion.registerExtension(com.intellij.openapi.project.Project, org.jetbrains.kotlin.fir.extensions.FirExtensionRegistrar)'
	at org.jetbrains.kotlin.allopen.AllOpenComponentRegistrar.registerProjectComponents(AllOpenPlugin.kt:57)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment$Companion.registerExtensionsFromPlugins$cli(KotlinCoreEnvironment.kt:671)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment$ProjectEnvironment.registerExtensionsFromPlugins(KotlinCoreEnvironment.kt:162)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment$Companion.configureProjectEnvironment(KotlinCoreEnvironment.kt:572)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment.<init>(KotlinCoreEnvironment.kt:192)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment.<init>(KotlinCoreEnvironment.kt:107)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment$Companion.createForProduction(KotlinCoreEnvironment.kt:442)
	at org.jetbrains.kotlin.cli.jvm.K2JVMCompiler.createCoreEnvironment(K2JVMCompiler.kt:202)
	at org.jetbrains.kotlin.cli.jvm.K2JVMCompiler.doExecute(K2JVMCompiler.kt:153)
	at org.jetbrains.kotlin.cli.jvm.K2JVMCompiler.doExecute(K2JVMCompiler.kt:53)
	at org.jetbrains.kotlin.cli.common.CLICompiler.execImpl(CLICompiler.kt:100)
	at org.jetbrains.kotlin.cli.common.CLICompiler.execImpl(CLICompiler.kt:46)
	at org.jetbrains.kotlin.cli.common.CLITool.exec(CLITool.kt:101)
	at io.quarkus.kotlin.deployment.KotlinCompilationProvider.compile(KotlinCompilationProvider.java:93)
	at io.quarkus.deployment.dev.QuarkusCompiler.compile(QuarkusCompiler.java:226)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.checkForChangedClasses(RuntimeUpdatesProcessor.java:725)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.doScan(RuntimeUpdatesProcessor.java:461)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.doScan(RuntimeUpdatesProcessor.java:441)
	at io.quarkus.vertx.http.runtime.devmode.VertxHttpHotReplacementSetup$4.handle(VertxHttpHotReplacementSetup.java:152)
	at io.quarkus.vertx.http.runtime.devmode.VertxHttpHotReplacementSetup$4.handle(VertxHttpHotReplacementSetup.java:139)
	at io.vertx.core.impl.ContextBase.lambda$null$0(ContextBase.java:137)
	at io.vertx.core.impl.ContextInternal.dispatch(ContextInternal.java:264)
	at io.vertx.core.impl.ContextBase.lambda$executeBlocking$1(ContextBase.java:135)
	at org.jboss.threads.ContextHandler$1.runWith(ContextHandler.java:18)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2513)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1538)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.base/java.lang.Thread.run(Thread.java:1589)

	at io.quarkus.kotlin.deployment.KotlinCompilationProvider.compile(KotlinCompilationProvider.java:99)
	at io.quarkus.deployment.dev.QuarkusCompiler.compile(QuarkusCompiler.java:226)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.checkForChangedClasses(RuntimeUpdatesProcessor.java:725)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.doScan(RuntimeUpdatesProcessor.java:461)
	at io.quarkus.deployment.dev.RuntimeUpdatesProcessor.doScan(RuntimeUpdatesProcessor.java:441)
	at io.quarkus.vertx.http.runtime.devmode.VertxHttpHotReplacementSetup$4.handle(VertxHttpHotReplacementSetup.java:152)
	at io.quarkus.vertx.http.runtime.devmode.VertxHttpHotReplacementSetup$4.handle(VertxHttpHotReplacementSetup.java:139)
	at io.vertx.core.impl.ContextBase.lambda$null$0(ContextBase.java:137)
	at io.vertx.core.impl.ContextInternal.dispatch(ContextInternal.java:264)
	at io.vertx.core.impl.ContextBase.lambda$executeBlocking$1(ContextBase.java:135)
	at org.jboss.threads.ContextHandler$1.runWith(ContextHandler.java:18)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2513)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1538)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.base/java.lang.Thread.run(Thread.java:1589)
```


## Build tool
```bash
Maven home: C:\apache-maven-3.9.0
Java version: 19.0.1, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-19
Default locale: en_US, platform encoding: UTF-8
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```