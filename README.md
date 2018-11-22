# Csharp-esimerkkeja
Seuraavassa koodissa esimerkkä taulukoista, listoista ja niiden läpikäymisestä foreach ja for-rakenteilla
```csharp
using System;
using System.Collections.Generic;

namespace listat_ja_taulukot
{
    class Program
    {
        static void Main(string[] args)
        {
            // Muuttujien alustus
            // Muuttujissa on aina tyyppi, nimi (ja arvo)
            int lisänumero1 = 15;
            int lisänumero2 = 30;
            // Taulukkomuuttuja
            //                     0  1  2  3  4   5  6  yhteensä 7 numeroa
            int[] lottonumerot = { 1, 3, 5, 8, 9, 14, 23 };
                      
            Console.WriteLine(lisänumero1);// Tulostaa yhden numeron
            // Miten tulostetaan taulukkomuuttujan sisältö?
            // Eli siis tämä :
            //1
            //3
            //5
            //8
            //9
            //14
            //23
            // TAPA 1:
            Console.WriteLine("Päivän lottonumerot ovat:");
            for (int i = 0 ; i < lottonumerot.Length ; i++ ) {
                   int alkio = lottonumerot[i];
                Console.WriteLine(alkio);
            }
            // TAPA 2:
            foreach( int alkio in lottonumerot)
            {
                Console.WriteLine(alkio);
            }
            //HARJOITUS, tulosta seuraava muuttuja käytteän foreach-silmukkaa
            string[] lomaTonni2 = { "Pariisi", "Budabest", "Vantaa", "Malmö", };

            // Koittakaa tulostaa lomaTonni2-kaupungit foreachilla

            // Listat
            // https://www.dotnetperls.com/list
            // Luodaan lista MarkkaJackpot
            List<int> markkajakkipotti = new List<int>();
            // TEHTÄVÄ 1 
            // Tehtävä lisää markkajakkipottiin 4 numeroa
            markkajakkipotti.Add(2);
            markkajakkipotti.Add(6);
            markkajakkipotti.Add(9);
            markkajakkipotti.Add(15);
            // TEHTÄVÄ 2
            // tulosta listan markkajakkipotti arvot foreachilla
            Console.WriteLine("Markkajakkipotin oikeat numerot ovat");
            foreach ( int luku in markkajakkipotti)
            {
                Console.WriteLine(luku);
            }
            // Luo lista kruunulotto ilman Add-funktioita
            List<int> kruunulotto = new List<int>(new int[] { 3, 6, 8 });
            // tulosta sen sisältö käyttäen for:ia
            Console.WriteLine("Kruunuloton oikeat numerot ovat");
            for (int i = 0; i < kruunulotto.Count; i++) // Huom! ei length
            {
                Console.WriteLine((i + 1) + ". oikea numero on " + kruunulotto[i]);
            }

            // Eli mikä hyöty listasta on?
            kruunulotto.Add(5); // listaan voidaan lisätä alkioita helposti
            // taulukkoon (array ei voi )
            }
    }
}
```
