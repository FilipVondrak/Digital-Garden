---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/WinForms – standardní ovládací prvky/","created":"2023-12-19T09:12:16.249+01:00","updated":"2024-03-19T15:11:19.280+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Komponenty
- speciální třídy, které se vykreslují
- jsou to [[UI\|UI]] prvky
- vytvořené instance jsou zobrazeny v designeru
- má události se kterými může reagovat na změny stavů (eventy)
	- např. změny stavy
		- změna velikosti
		- posunutí
		- hover myši nad komponentem
		- kliknutí na komponent

> [!Showcase]- Ukázka kódu eventu
>```CSharp
> public partial class Form1 : Form
>{
>    public Form1()
>    {
>        InitializeComponent();
>    }
>
>    private void button1_Click(object sender, EventArgs e)
>    {
>        button1.Text = "Tlačítko bylo kliknuté";
>    }
>}
>```

# Formulář
- vznikne třída Form1 která dědí z Form pomocí dvojtečky

> [!Showcase]- Ukázka kódu
> ```CSharp
>public partial class Form1 : Form
>{
> 	 public Form1()
> 	 {
> 	     InitializeComponent();
> 	 }
>} 
>```

