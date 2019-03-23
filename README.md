# my-lab
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace WindowsFormsApplication1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
             double per, vt, tr, p,s;
            per = double.Parse(textBox1.Text);
            vt = double.Parse(textBox2.Text);
            tr = double.Parse(textBox3.Text);

            p = (per + vt + tr) / 2;
           
            s = Math.Sqrt(p * (p - per) * (p - vt) * (p - tr));
            
            label6.Text = s.ToString();




        }

        private void textBox1_KeyPress(object sender, KeyPressEventArgs e)
        {

 char number = e.KeyChar;

 if (!Char.IsDigit(number) && number != 8 && number != 44)
 {
    e.Handled = true;
 }
        }

        private void textBox2_KeyPress(object sender, KeyPressEventArgs e)
        {
            char number = e.KeyChar;

            if (!Char.IsDigit(number) && number != 8 && number != 44)
            {
                e.Handled = true;
            }
        }

        private void textBox3_KeyPress(object sender, KeyPressEventArgs e)
        {
            char number = e.KeyChar;

            if (!Char.IsDigit(number) && number != 8 && number != 44)
            {
                e.Handled = true;
            }
        }
    }
}
