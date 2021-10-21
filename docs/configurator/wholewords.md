# Matching Whole Words

<figure markdown="1">
  ![Whole Words](img/wholewords.png)
</figure>

If you select the **Whole word** check box, Configurator matches the search string if the matched string is surrounded by spaces or punctuation.

For example, without the **Whole word** check box selected, replacing the string "Heading" with the string "Topic" would have the following results:
<table>
<tr><td>"Heading"</td><td>would be changed to</td><td>"Topic"</td></tr>
<tr><td>"Headings"</td><td>would be changed to</td><td>"Topics"</td></tr>
</table>

With the **Whole word** check box selected, the same search/replace operation would have the following results:
<table>
<tr><td>"Heading"</td><td>would be changed to</td><td>"Topic"</td></tr>
<tr><td>"Headings"</td><td>would remain as</td><td>"Headings"</td></tr>
</table>