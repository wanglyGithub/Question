##AndroidStudio 常见问题

##类表
- Q1：
	 >Error:Execution failed for task ':app:transformClassesWithDexForDebug'.
	
	 >com.android.build.api.transform.TransformException: com.android.ide.common.process.ProcessException:java.util.concurrent.ExecutionException:
	  java.lang.OutOfMemoryError: GC overhead limit exceeded

  解决方式： 在.gradle的gradle.properties的 org.gradle.jvmargs=-Xmx512m调大

- Q2：
	  >Error:trouble processing "java/lang/BuildConfig.class":
	  >
	  >Error:Ill-advised or mistaken usage of a core class (java.* or javax.*)
	  >
	  >Error:when not building a core library.
	  >
	  >Error:This is often due to inadvertently including a core library file
	  >
	  >Error:in your application's project, when using an IDE (such as
	  >
	  >Error:Eclipse). If you are sure you're not intentionally defining a
	  >
	  >Error:core class, then this is the most likely explanation of what's
	  >
	  >Error:going on.
	  >
	  >Error:However, you might actually be trying to define a class in a core
	  >
	  >Error:namespace, the source of which you may have taken, for example,
	  >
	  >Error:from a non-Android virtual machine project. This will most
	  >
	  >Error:assuredly not work. At a minimum, it jeopardizes the
	  >
	  >Error:compatibility of your app with future versions of the platform.
	  >
	  >Error:It is also often of questionable legality.

解决方式：出现该原因是项目中引用了以 **java 开头的包名**

- Q3：
 	 >/lib/arm64, /vendor/lib64, /system/lib64]]] couldn't find "libgotyeapi.so"

解决方式：在64位手机上会自动寻找jni里面arm64-v8a文件夹里面的so文件，如果找不到则报这个错误，如果把32位的so放进去则报位数不匹配的错误，解决方法是放入64位的so或者删除该文件夹,只留armeabi





















