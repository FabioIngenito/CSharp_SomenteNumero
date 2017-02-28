# CSharp_SomenteNumero

if (!(e.KeyChar >= '0' &amp;&amp; e.KeyChar &lt;= '9') &amp;&amp; e.KeyChar != 8) e.Handled = true;


    Private Sub TextBox1_KeyPress(sender As Object, e As KeyPressEventArgs) Handles TextBox1.KeyPress

        //Escreve-se em VB 6 assim:

        //Written in VB 6 as follows:

        //If InStr("0123456789", Chr(KeyAscii)) = 0 nd KeyAscii <> 8 Then KeyAscii = 0

        //Migrado para VB.NET:

        //Migrated to VB.NET:

        //If InStr("0123456789", e.KeyChar) = 0 And Not Convert.ToInt32(e.KeyChar) = Keys.Back Then e.Handled = True

        //Melhorada a Migração:	

        //Improved the migration:

        //If Not Char.IsNumber(e.KeyChar) And Not Convert.ToInt32(e.KeyChar) = Keys.Back Then e.Handled = True


        //E C#

        //And C#

        if (!(e.KeyChar >= '0' && e.KeyChar <= '9') && e.KeyChar != 8) e.Handled = true;

    End Sub