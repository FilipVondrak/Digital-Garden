---
{"dg-publish":true,"permalink":"/Osobní/Programování/Patterny/UtilityPattern/","created":"2024-03-29T15:26:42.316+01:00","updated":"2024-05-17T15:35:02.399+02:00"}
---

- vzor utility/helper je užitečný pro vytvoření neinicializovatelné třídy
- obvykle pomáhá udržet nejrůznější nesouvisející metody na jednom místě
- měly by být ==všechny metody deklarované ve třídě statické==
-  jediným způsobem, jak zajistit neinstantnost, je deklarovat konstruktor jako **private**
- v C# je to například třída **Console**

> [!Showcase]- Ukázka implementace utility vzoru v Javě
>```Java
>public class Utility {
>   private Utility(){
>
>   }
> 
>   public static Boolean compareSomething(){
>      // ...
>      return false;
>   }
>
>   public static void shuffleTheList(List\<String> list){
>      // ...
>   }
>
>   public static void doSomething(){
>      // ...
>   }
>}
>```