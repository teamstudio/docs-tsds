# Matching Accented Characters

<figure markdown="1">
  ![Accented](img/accented.png)
</figure>

If the **Accent** check box is selected, and the search contains accented characters (for example, à ä ç é ë ï ô), Configurator will only match the search string if the characters in the matched string have the same accenting.

For example, without the **Accent** check box selected, replacing the string "Naïve" with the string "Innocent" would have the following results:
<table>
  <tr><td>"Naïve"</td><td>would be changed to</td><td>"Innocent"</td></tr>
  <tr><td>"Naive"</td><td>would be changed to</td><td>"Innocent"</td></tr>
</table>

With the **Accent** check box selected, the same search/replace operation would have the following results:
<table>
  <tr><td>"Naïve"</td><td>would be changed to</td><td>"Innocent"</td></tr>
  <tr><td>"Naive"</td><td>would remain as</td><td>"Naive"</td></tr>
</table>
