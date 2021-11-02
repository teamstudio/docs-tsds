# ワイルドカードの使用

<figure markdown="1">
  ![Wildcards](img/wildcards.png)
</figure>

**[ 検索文字列 ]** フィールドでワイルドカード検索を実行するには、**[ ワイルドカードを使用 ]** チェックボックスを選択します。ワイルドカード文字(*) を使用すると、最初のスペースまでの任意の文字列が検索対象になります。 ワイルドカード文字(?)を使用すると、最初のスペースまでの 1 文字が検索対象になります。

たとえば、「Lotus*」と入力すると、Lotus で始まるすべての単語が検索されます。「LotusScript」、および「LotusNotes」は検索されますが、「Lotus and HCL」は、スペースが入っているため検索されません。

「Lotus?otes」と入力すると、次の単語が検索されます。「LotusNotes」、および「LotusSotes」は検索されますが、「LotusNootes」は 検索されません。

「www.ives.*」と入力すると、「www.ives.com」および「www.ives.co.uk」をすべて検索して、これらを「www.teamstudio.com」に置換することができます。

「Field*」と入力すると、「FieldA」、「FieldB」、「FieldC」をすべて検索して、これらを「FieldZ」に置換することができます。