# _**PROJECT INTHERITANCE**_

    OOP | Teknik Informatika | Universitas Pelita Bangsa
    ===================================================================
    Nama    : Sofyan Arif Widiatko
    NIM     : 312210093
    Kelas   : TI22B1

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace oop
{
class Pegawai
{
private string \_nama;
private double \_gajiPokok;

        public string Nama
        {
            get { return _nama; }
            set { _nama = value; }
        }
        public double Gaji
        {
            get { return _gajiPokok; }
            set { _gajiPokok = value; }
        }
        public void cetakInfo()
        {
            Console.WriteLine("PEGAWAI");
        }
    }
    class Manager : Pegawai
    {
        private double _tunjangan;
        public double Tunjangan
        {
            get { return _tunjangan; }
            set { _tunjangan = value; }
        }
        public void cetakTunjangan()
        {

            Console.WriteLine("Tujangan :");
        }

    }
    class Programmer : Pegawai
    {
        private double _bonus;
        public double Bonus
        {
            get { return _bonus; }
            set { _bonus = value; }
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus :");
        }

    }
    class Garnis : Pegawai
    {
        public Garnis()
        {
            Nama = "Garnis A";
            Gaji = 5000000;

        }
    }

    class Anton : Manager
    {
        public Anton()
        {
            Nama = "Anton Baskoro";
            Gaji = 10000000;
            Tunjangan = 100;
        }
        public void cetakInfo()
        {
            Console.WriteLine("MANAGER");
        }
    }
    class Malik : Programmer
    {
        public Malik()
        {
            Nama = "Malik A";
            Gaji = 12000000;
            Bonus = 80;
        }
        public void cetakInfo()
        {
            Console.WriteLine("PROGRAMMER");
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Inheritance");
            Console.WriteLine("---------------------");
            Garnis garnis = new Garnis();
            garnis.cetakInfo();
            Console.WriteLine("Nama : {0}", garnis.Nama);
            Console.WriteLine("Gaji : {0}", garnis.Gaji);
            Console.WriteLine("---------------------");
            Anton anton = new Anton();
            anton.cetakInfo();
            Console.WriteLine("Nama : {0}", anton.Nama);
            Console.WriteLine("Gaji : {0}", anton.Gaji);
            Console.WriteLine("Tunjangan : {0}", anton.Tunjangan);
            Console.WriteLine("---------------------");
            Malik malik = new Malik();
            malik.cetakInfo();
            Console.WriteLine("Nama : {0}", malik.Nama);
            Console.WriteLine("Gaji : {0}", malik.Gaji);
            Console.WriteLine("Bonus : {0}", malik.Bonus);
            Console.ReadKey();
        }
    }

}
