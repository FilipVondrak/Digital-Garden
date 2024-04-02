---
{"dg-publish":true,"permalink":"/Osobní/Programování/Enum/","created":"2024-03-29T16:56:04.827+01:00","updated":"2024-04-02T12:06:27.788+02:00"}
---

- je to **speciální** "třída", která ==reprezentuje skupinu konstant== (neměnných)
- pro vytvoření enumu, stačí použít **keyword** enum

## Ukázka
### vytvoření enumu
```csharp
enum Level 
{
  Low,
  Medium,
  High
}
```
### použití enumu 
```csharp
Level myVar = Level.Medium;

switch (myVar)
{
  case Level.Low:
    System.out.println("Low level");
    break;
  case Level.Medium:
    System.out.println("Medium level");
    break;
  case Level.High:
    System.out.println("High level");
    break;
}
```