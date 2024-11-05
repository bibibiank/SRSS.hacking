## Objetivo 

You will find the flag after analysing this apk Download [here](https://artifacts.picoctf.net/c/449/timer.apk).

## Solución  

```java 

┌──(kali㉿kali)-[~/Downloads/timer]
└─$ wget https://artifacts.picoctf.net/c/449/timer.apk                 
--2024-11-04 15:12:24--  https://artifacts.picoctf.net/c/449/timer.apk
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4678467 (4.5M) [application/octet-stream]
Saving to: ‘timer.apk’

timer.apk                     100%[================================================>]   4.46M  7.88MB/s    in 0.6s    

2024-11-04 15:12:33 (7.88 MB/s) - ‘timer.apk’ saved [4678467/4678467]

                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$ ls
timer.apk
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$ file timer.apk       
timer.apk: Android package (APK), with zipflinger virtual entry, with APK Signing Block
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$ unzip timer.apk 
Archive:  timer.apk
  inflating: META-INF/com/android/build/gradle/app-metadata.properties  
  inflating: classes3.dex            
  inflating: classes2.dex            
  inflating: AndroidManifest.xml     
  inflating: res/anim/abc_fade_in.xml  
  inflating: res/anim/abc_fade_out.xml  
  inflating: res/anim/abc_grow_fade_in_from_bottom.xml  
  inflating: res/anim/abc_popup_enter.xml 
 extracting: META-INF/androidx.lifecycle_lifecycle-livedata-core.version  
 extracting: META-INF/androidx.lifecycle_lifecycle-livedata.version  
 extracting: META-INF/androidx.lifecycle_lifecycle-process.version  
 extracting: META-INF/androidx.lifecycle_lifecycle-runtime.version  
 extracting: META-INF/androidx.lifecycle_lifecycle-viewmodel-savedstate.version  
 extracting: META-INF/androidx.lifecycle_lifecycle-viewmodel.version  
 extracting: META-INF/androidx.loader_loader.version  
 extracting: META-INF/androidx.localbroadcastmanager_localbroadcastmanager.version  
 extracting: META-INF/androidx.print_print.version  
 extracting: META-INF/androidx.recyclerview_recyclerview.version  
 extracting: META-INF/androidx.savedstate_savedstate.version  
 extracting: META-INF/androidx.startup_startup-runtime.version  
 extracting: META-INF/androidx.tracing_tracing.version  
 extracting: META-INF/androidx.transition_transition.version  
 extracting: META-INF/androidx.vectordrawable_vectordrawable-animated.version  
 extracting: META-INF/androidx.vectordrawable_vectordrawable.version  
 extracting: META-INF/androidx.versionedparcelable_versionedparcelable.version  
 extracting: META-INF/androidx.viewpager2_viewpager2.version  
 extracting: META-INF/androidx.viewpager_viewpager.version  
 extracting: META-INF/com.google.android.material_material.version  
  inflating: kotlin/annotation/annotation.kotlin_builtins  
  inflating: kotlin/collections/collections.kotlin_builtins  
  inflating: kotlin/coroutines/coroutines.kotlin_builtins  
  inflating: kotlin/internal/internal.kotlin_builtins  
  inflating: kotlin/kotlin.kotlin_builtins  
  inflating: kotlin/ranges/ranges.kotlin_builtins  
  inflating: kotlin/reflect/reflect.kotlin_builtins  
  inflating: classes.dex             
  inflating: META-INF/CERT.SF        
  inflating: META-INF/CERT.RSA       
  inflating: META-INF/MANIFEST.MF    
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$  grep -R picoCTF 
grep: classes3.dex: binary file matches
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$ find . -name classes3.dex 

./classes3.dex
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/timer]
└─$ strings classes3.dex | grep picoCTF    
*picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

```

picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}
## Notas Adicionales 

### Referencias
