# Building Configurable Database Designs

When you build configurable texts into your database design, you can use Configurator to make quick changes, tailoring your application to meet individual customer needs.

Say, for example, you’re building a sales force automation system you will sell to a number of clients.You may have a field that captures the status of an account. When you define the static text for the field label as “[#Status#]”, you can use Configurator to easily customize this static text for a client, who, for example, prefers the text label “Phase”.

Similarly, the keyword list behind the Status field may consist of the following entries: “[#Prospect#]”; “[#Customer#]”; and “[#Ex-customer#]”, which you can easily re-configure to meet your customer’s requirements.

You can even make your application entirely configurable by creating completely generalized keyword lists that define list members as “[#Item1#]”; “[#Item2#]”, and so on.

Using Configurator you can build a form where every piece of static text is configurable. Your application runs significantly more quickly and efficiently when you use Configurator than when you use run-time @DBLookup commands.