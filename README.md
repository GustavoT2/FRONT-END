liçoes de terça (Front-end-JavaScript) 



using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Aula_Quarta_18_10
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        int pontos;



        private void button1_Click(object sender, EventArgs e)
        {
            int x;
            Random sorteio = new Random();
            x = sorteio.Next(1,14);
            
            switch (x) 
            
            {
                case 1:
                    pictureBox1.Image = Properties.Resources.A;
                    pontos += 1;
                    break;


                case 2:
                    pictureBox1.Image = Properties.Resources._2;
                    pontos += 2;
                    break;


                case 3:
                    pictureBox1.Image = Properties.Resources._3;
                    pontos += 3;
                    break;


                case 4:
                    pictureBox1.Image = Properties.Resources._4;
                    pontos += 4;
                    break;


                case 5:
                    pictureBox1.Image = Properties.Resources._5;
                    pontos += 5;
                    break;


                case 6:
                    pictureBox1.Image = Properties.Resources._6;
                    pontos += 6;
                    break;


                case 7:
                    pictureBox1.Image = Properties.Resources._7;
                    pontos += 7;
                    break;


                case 8:
                    pictureBox1.Image = Properties.Resources._8;
                    pontos += 8;
                    break;


                case 9:
                    pictureBox1.Image = Properties.Resources._9;
                    pontos += 9;
                    break;


                case 10:
                    pictureBox1.Image = Properties.Resources.J;
                    pontos += 10;
                    break;

                case 11:
                    pictureBox1.Image = Properties.Resources.K;
                    pontos += 10;
                    break;

                case 12:
                    pictureBox1.Image = Properties.Resources.Q;
                    pontos += 10;
                    break;

            }
        }

        private void pictureBox1_Click(object sender, EventArgs e)
        {
            if(pontos <=21)
            {
                lbl_Pontos.Text = Convert.ToString(pontos);
                if (pontos ==21)
                {
                    lbl_Pontos.Text = "GANHOU!!!!";
                    btJogar.Enabled = false;
                    btReiniciar.Enabled = true;
                }
            }
            else
            {
                lbl_Pontos.Text = "PERDEU!!! (" + Convert.ToString(pontos) + " pontos)";
                btJogar.Enabled = true;
                btReiniciar.Enabled = false;
            }
        }
    }
}

