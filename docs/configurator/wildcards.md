# Using Wildcards

<figure markdown="1">
  ![Wildcards](img/wildcards.png)
</figure>

Select the **Use Wildcards** check box to perform a wildcard search from the **Find What** field. The **\*** wildcard character lets you search on 0 to *n* number of characters, up to the first space character. The **?** wildcard character lets you search on one character, up to the first space character.

For example, entering **Lotus\*** to find all instances of words starting with Lotus will find "LotusScript" and "LotusNotes" but not "Lotus and HCL" (intervening space.)

Entering **Lotus?otes** will find "LotusNotes" and "LotusSotes" but not "LotusNootes".

Entering **www.ives.\*** will find all instances of "www.ives.com" and "www.ives.co.uk", so that you can replace them with "www.teamstudio.com".

Entering **Field\*** will find all instances of FieldA, FieldB and FieldC, so that you can replace them with FieldZ.