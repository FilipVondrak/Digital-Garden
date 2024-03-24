---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Návrhové vzory/","created":"2023-12-19T09:15:02.441+01:00","updated":"2024-03-24T17:50:54.298+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Interface
![[InterfaceCsharp\|InterfaceCsharp]]
# Servant
![[ServantPattern\|ServantPattern]]
# Generické třídy
![[GenericClassCsharp\|GenericClassCsharp]]
# Messenger
![[MessangerPattern\|MessangerPattern]]
# Factory

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

# Builder
![[BuilderPattern\|BuilderPattern]]
# Singleton

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




Díky singletonu lze vytvořit pouze jednu instanci z třídy.
# Ukázka:
```CSharp
public class Singleton  
{  
    private static Singleton? _instance;  
    public static Singleton Instance { get => _instance ??=new UserPreferences(); }  
}
```

</div></div>
