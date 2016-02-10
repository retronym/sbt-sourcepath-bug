Demo project for SBT bug

```
⚡ sbt clean compile
[info] Loading global plugins from /Users/jason/.sbt/0.13/plugins
[info] Loading project definition from /Users/jason/code/sbt-sourcepath-bug/project
[info] Set current project to sbt-sourcepath-bug (in build file:/Users/jason/code/sbt-sourcepath-bug/)
[success] Total time: 0 s, completed 10/02/2016 10:32:45 PM
[info] Updating {file:/Users/jason/code/sbt-sourcepath-bug/}sbt-sourcepath-bug...
[info] Resolving jline#jline;2.12.1 ...
[info] Done updating.
[info] Compiling 1 Scala source to /Users/jason/code/sbt-sourcepath-bug/target/scala-2.11/classes...
java.lang.ClassCastException: xsbt.API$ApiPhase cannot be cast to scala.tools.nsc.Global$GlobalPhase
	at scala.tools.nsc.Global$Run$$anonfun$compileLate$2$$anonfun$apply$1.apply(Global.scala:1609)
	at scala.tools.nsc.Global$Run$$anonfun$compileLate$2$$anonfun$apply$1.apply(Global.scala:1609)
	at scala.reflect.internal.SymbolTable.enteringPhase(SymbolTable.scala:235)
	at scala.tools.nsc.Global$Run$$anonfun$compileLate$2.apply(Global.scala:1609)
	at scala.tools.nsc.Global$Run$$anonfun$compileLate$2.apply(Global.scala:1608)
	at scala.collection.Iterator$class.foreach(Iterator.scala:742)
	at scala.collection.AbstractIterator.foreach(Iterator.scala:1194)
	at scala.tools.nsc.Global$Run.compileLate(Global.scala:1608)
	at scala.tools.nsc.Global$Run.compileLate(Global.scala:1598)
	at scala.tools.nsc.GlobalSymbolLoaders.compileLate(GlobalSymbolLoaders.scala:29)
	at scala.tools.nsc.symtab.SymbolLoaders$SourcefileLoader.doComplete(SymbolLoaders.scala:368)
	at scala.tools.nsc.symtab.SymbolLoaders$SymbolLoader.complete(SymbolLoaders.scala:211)
	at scala.reflect.internal.Symbols$Symbol.info(Symbols.scala:1489)
	at scala.reflect.internal.Symbols$TypeSymbol.isNonBottomSubClass(Symbols.scala:3104)
	at scala.reflect.internal.AnnotationInfos$AnnotationInfo.matches(AnnotationInfos.scala:304)
	at scala.reflect.internal.AnnotationInfos$Annotatable$class.dropOtherAnnotations(AnnotationInfos.scala:67)
	at scala.reflect.internal.AnnotationInfos$Annotatable$class.hasAnnotation(AnnotationInfos.scala:52)
	at scala.reflect.internal.Symbols$Symbol.hasAnnotation(Symbols.scala:176)
	at scala.reflect.internal.Symbols$Symbol.isDeprecated(Symbols.scala:858)
	at scala.tools.nsc.typechecker.RefChecks$RefCheckTransformer.checkUndesiredProperties(RefChecks.scala:1291)
```
