# TF2ServersidePlayerAttachmentFixer
Stops the engine from rendering entities parented to a player invisible, i.e. custom wearable models and such. This plugin was based around [an older version of a similar plugin created by MasterXykon](https://pastebin.com/jYF9XJFg), only without a hundred different `if` statements.

## Usage Instructions
Simple enough to use. Run the SMX and forget about it. It checks every entity that gets created for the `m_bValidatedAttachedEntity` netprop and if it finds it, sets its value to `1`. This is how Valve went about breaking serverside player attachments back in 2010. They just added the netprop, and set the engine up to change the rendering of a parented entity to invisible if the value of the netprop was `0`. That's why for most cases, custom weapon and hat models are invisible to other players. If you've noticed a server where custom weapon or hat models are being used and ***can*** be seen by other players, this is how.


## Frequently Asked Question *(yes, singular)*
**Q:** Isn't using this type of thing against Valve's TOS from 2010, and won't using it get your server blacklisted?

**A:** It technically *is* against the TOS, and using something like it could have potentially gotten your server blacklisted about 8-9 years ago. Nowadays, not so much. Many community servers in existence are using this system.

For example, Skial uses it for their "!items" system that allows you to equip any weapon or cosmetic you want *(even rare ones like the Wiki Cap, Top Notch, Golden Wrench, Golden Frying Pan, etc)* and they're visible to other players. What has changed in the past 8-9 years is that Valve is now more focused on CS:GO and Half Life: Alyx.

TF2 servers have not suffered any GLST token bans in many years. Even CS:GO servers, which were frequently hit by GLST token bans for using fake knife/gun/etc skin plugins, have slowly over time stopped being hit by GLST token bans. It seems Valve has either lightened up on former community "restrictions", or they're too busy with HL:A to notice.

***Basically, by using this plugin, you are acknowledging that there is still the possibility that Valve could come around one day and blacklist your server. Don't blame me if such a thing happens either.***
