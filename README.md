Peddler
=======

WoW addon that allows you to automatically sell any unwanted items, hassle-free!

*ped·dler
n.
One who travels about selling wares for a living.*

##Description

*Peddler* simply allows you to flag items that you plan to sell, automatically selling them later when you interact with a vendor. It automatically flags grey items you loot to be sold, but you're free to un-flag them.

While going back to complete low-level quests with regards to getting a few quest achievements, I found my bags full of green quest rewards that I would try to sell whenever I could. However, after leaving a vendor I would notice that I'd missed one or two items; I made this addon so that I could immediately mark the newly received items without having to scour my bags for them later on!



##Usage

*CTRL+Right-click* on an item in your inventory and it will be flagged for peddling at your next trip to a vendor! A small set of coins appears in the item's icon to highlight that it will be automatically sold.

*/peddler displays* the interface's options:

*Modifier Key* - allows the user to change the marking modifier from the CTRL-key.

*Sell Limit* - toggles whether or not Peddler should sell items in sets of 12, allowing the user to buyback any mistakenly marked items.

*Silent Mode* - toggles whether or not Peddler will print anything to the chat-log when selling items.


##WoW Forever and EllesmereUI

This fork (originally by Cartas) runs on the WoW Forever client (`## Interface: 16001`) as well as Classic Era.

- Item buttons are located through `EnumerateValidItems`/`GetBagID` on the default bag frames, and the modifier-click is hooked on each button, as the modern client has no `ContainerFrameItemButton_OnModifiedClick`.
- Items are sold with `C_Container.UseContainerItem`.
- *EllesmereUI Bags* is supported through its overlay API (`EUI_Bags.RegisterItemOverlayIcon`): the coin overlay and the modifier-click marking work in its grid and list views. With EllesmereUI Bags disabled (or switched back to the default bags), the default bags are used. Saved variables are unchanged.
