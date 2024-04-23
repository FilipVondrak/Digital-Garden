---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Praktické/Projekt v oblasti programování/","created":"2023-12-19T09:21:41.658+01:00","updated":"2024-04-23T08:30:40.324+02:00"}
---

# Zadání 2024
## Delegát (Žárovka)
### Zadání
- Ve winforms vytvořit aplikaci, která bude zapínat/vypínat žárovku.
- Musí na změnu stavu použít delegáta a ne click event
### Řešení
Form1.cs
```CSharp
namespace Zarovka__delegat_
{
    public delegate void ZmenStav(bool stav);

    public partial class Form1 : Form
    {
        private ZmenStav _zmenStav;

        public Form1()
        {
            InitializeComponent();
            _zmenStav = ZmenZarovku;
        }

        public void ZmenZarovku(bool stav) => zarovka.BackColor = stav ? Color.Yellow : Color.Black;

        private void button1_Click(object sender, EventArgs e) => _zmenStav(true);

        private void button2_Click(object sender, EventArgs e) => _zmenStav(false);
    }
}
```

UI formu1
![Pasted image 20240423081315.png](/img/user/Images/Pasted%20image%2020240423081315.png)
## Práce s databází
### Zadání
- ve winforms vytvořit aplikaci, který bude používat SQLite databázi a vytvoří v ní tabulku
- bude číst a zapisovat do tabulka údaje, např. ID, text a čas
### Řešení
- je potřeba stáhnout **System.Data.Sqlite** nuget, pozor - je jich na výběr několik se stejným jménem a je potřeba tenhle konkrétní
![Pasted image 20240423082553.png](/img/user/Images/Pasted%20image%2020240423082553.png)

Form1.cs
```CS
using System.Data;

namespace Databaze
{
    public partial class Form1 : Form
    {
        private Databaze databaze;
        public Form1()
        {
            InitializeComponent();
            databaze = Databaze.Singleton.Instance;
            ShowAllData();

            dataGridView1.Columns[0].Width = 165;
            dataGridView1.Columns[1].Width = 200;
            dataGridView1.Columns[2].Width = 500;

        }

        private void button2_Click(object sender, EventArgs e)
        {
            string query = $"INSERT INTO databaze (time, entry) VALUES ('{DateTime.Now}', '{inputTextBox.Text}')";
            databaze.ExecuteQuery(query);
            inputTextBox.Text = "";
            ShowAllData();
        }

        private void ShowAllData()
        {
            string query = "SELECT * FROM databaze";
            DataTable dt = databaze.ExecuteQuery(query);
            dataGridView1.DataSource = dt;
        }

        private void ReadEntry()
        {
            string id = textBox4.Text;
            string query = $"SELECT * FROM databaze WHERE id = {id}";
            DataTable dt = databaze.ExecuteQuery(query);
            if (dt.Rows.Count == 0)
            {
                MessageBox.Show("Záznam nenalezen");
                return;
            }
            DataRow row = dt.Rows[0];
            idTextBox.Text = row["id"].ToString();
            timeTextBox.Text = row["time"].ToString();
            messageTextBox.Text = row["entry"].ToString();
        }

        private void button1_Click(object sender, EventArgs e) => ReadEntry();

        private void deleteButton_Click(object sender, EventArgs e)
        {
            string id = idTextBox.Text;
            string query = $"DELETE FROM databaze WHERE id = {id}";
            databaze.ExecuteQuery(query);

            idTextBox.Text = string.Empty;
            timeTextBox.Text = string.Empty;
            messageTextBox.Text = string.Empty;

            ShowAllData();
        }
    }
}
```

UI formu1
![Pasted image 20240423081812.png](/img/user/Images/Pasted%20image%2020240423081812.png)

Databaze.cs
```Cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System;
using System.Text;
using System.Data;
using System.Data.SQLite;

namespace Databaze
{
    internal class Databaze
    {
        private static Databaze? _instance;
        public static Databaze Instance { get => _instance ??= new Databaze(); }

        private SQLiteConnection sqlite;

        private Databaze()
        {
            try
            {
                sqlite = new SQLiteConnection("Data Source=databaze.db;New=False;");
            }
            catch (Exception e)
            {
                MessageBox.Show(e.Message);
            }
            CreateTable();
        }

        private void CreateTable()
        {
            string query = "CREATE TABLE IF NOT EXISTS databaze (id INTEGER PRIMARY KEY AUTOINCREMENT, time TEXT, entry TEXT)";
            try
            {
                SQLiteCommand cmd = new SQLiteCommand(query, sqlite);
                sqlite.Open();
                cmd.ExecuteNonQuery();
            }
            catch (Exception e)
            {
                MessageBox.Show(e.Message);
            }
            finally
            {
                sqlite.Close();
            }
        }

        public DataTable ExecuteQuery(string query)
        {
            DataTable dt = new DataTable();
            try
            {
                SQLiteCommand cmd = new SQLiteCommand(query, sqlite);
                sqlite.Open();
                SQLiteDataReader reader = cmd.ExecuteReader();
                dt.Load(reader);
                reader.Close();
            }
            catch (Exception e)
            {
                MessageBox.Show(e.Message);
            }
            finally
            {
                sqlite.Close();
            }
            return dt;
        }
    }
}
```
## Photoshop
### Zadání
- vytvořit winforms aplikaci, která bude sloužit jako photoshop
- mít základní funkce jako:
	- Otáčení a zrcadlení obrázku
	- Kreslit do obrázku pomocí grafiky
	- Převést obrázek do černobíle, odstranit obrázku pozadí
### Řešení
Form1.cs
```Cs
namespace Photoshop
{
    public partial class Form1 : Form
    {
        private Bitmap bitmap = null;
        private Graphics g;

        public Form1()
        {
            InitializeComponent();
            g = this.CreateGraphics();
        }

        private void otočitObrázekToolStripMenuItem_Click(object sender, EventArgs e) => Upravy.OtočitObrázek(bitmap, pictureBox, g);

        private void otevřítObrázekToolStripMenuItem_Click(object sender, EventArgs e)
        {
            using (OpenFileDialog dlg = new OpenFileDialog())
            {
                dlg.Title = "Open Image";
                dlg.Filter = "Image Files (*.bmp;*.jpg;*.jpeg,*.png)|*.BMP;*.JPG;*.JPEG;*.PNG";

                if (dlg.ShowDialog() == DialogResult.OK)
                {
                    bitmap = new Bitmap(Bitmap.FromFile(dlg.FileName));
                }
            }
            pictureBox.Image = bitmap;
        }

        private void uložitObrázeToolStripMenuItem_Click(object sender, EventArgs e)
        {
            using (SaveFileDialog dlg = new SaveFileDialog())
            {
                dlg.Title = "Save Image";
                dlg.Filter = "Image Files (*.bmp;*.jpg;*.jpeg,*.png)|*.BMP;*.JPG;*.JPEG;*.PNG";

                if (dlg.ShowDialog() == DialogResult.OK)
                {
                    bitmap.Save(dlg.FileName);
                }
            }
        }

        private void zavřítObázekToolStripMenuItem_Click(object sender, EventArgs e)
        {
            this.bitmap = null;
            this.pictureBox.Image = null;
        }

        private void otočitObrázekToolStripMenuItem_Click_1(object sender, EventArgs e) => Upravy.OtočitObrázek(bitmap, pictureBox, g);

        private void zrcadlitToolStripMenuItem_Click(object sender, EventArgs e) => Upravy.ZrcadlitObrázek(bitmap, pictureBox, g);

        private void toolStripMenuItem1_Click(object sender, EventArgs e) => Upravy.GrayScale(bitmap, pictureBox, g);

        private void toolStripButton2_CheckedChanged(object sender, EventArgs e)
        {
            if (MalovatButton.Checked)
            {
                pictureBox.MouseDown += pictureBox_MouseDown;
            }
            else
            {
                pictureBox.MouseDown -= pictureBox_MouseDown;
            }
        }

        private void pictureBox_MouseDown(object sender, MouseEventArgs e)
        {
            if (MalovatButton.Checked)
            {
                using (Pen pen = new Pen(Color.Black, 5))
                {
                    g.DrawLine(pen, e.Location, e.Location);
                }
            }
        }

        private void toolStripButton2_Click(object sender, EventArgs e) => MalovatButton.Checked = !MalovatButton.Checked;
    }
}

```

UI formu1
![Pasted image 20240423082801.png](/img/user/Images/Pasted%20image%2020240423082801.png)

Upravy.cs
```Cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Photoshop
{
    internal static class Upravy
    {

        public static void OtočitObrázek(Bitmap bitmap, PictureBox pBox, Graphics g)
        {
            // Otočení obrázku
            bitmap.RotateFlip(RotateFlipType.Rotate90FlipNone);
            pBox.Image = bitmap;
        }

        public static void ZrcadlitObrázek(Bitmap bitmap, PictureBox pBox, Graphics g)
        {
            // Zrcadlení obrázku
            bitmap.RotateFlip(RotateFlipType.RotateNoneFlipX);
            pBox.Image = bitmap;
        }

        public static void GrayScale(Bitmap bitmap, PictureBox pBox, Graphics g)
        {
            // Převod obrázku do černobílé
            for (int i = 0; i < bitmap.Width; i++)
            {
                for (int j = 0; j < bitmap.Height; j++)
                {
                    Color pixel = bitmap.GetPixel(i, j);
                    int avg = (pixel.R + pixel.G + pixel.B) / 3;
                    bitmap.SetPixel(i, j, Color.FromArgb(avg, avg, avg));
                }
            }
            pBox.Image = bitmap;
        }   
    }
}

```