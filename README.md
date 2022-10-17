Here you can easily access all information about vipsystem.

# Config

- The _Config.TebexLink_ part that appears when you first open the Config should be your tebex coin purchase address. Because in-game redirection is done here.
- The _Config.Day_ section determines how many days after the vehicles and workplaces you have purchased will be deleted.
- We decide which membership to add this reward to. We choose the regular or premium member.

# Config.CaseItem

- You can add only 4 safes to this section.

- The credit part indicates the coin that will be reduced when the user buys it.

- The image part indicates the photo of the safe you see below.
_https://ibb.co/zZ45kCN_

- You need to add 3 items in the Items section. Do not change the coin amounts of the items. If the item is a vehicle, you need to write "car" in the type section, if the item is an item, "item" in the type section. In the item section, write which item you want to give. If it is a vehicle, write the vehicle model there.

# Config.Cases

- As it is written in the config section, the first 4 crates here are both equal to the 4 crates in the starter pack and the first 4 crates on the left, respectively. The others are the other crates on the left.

- If you change your safe pictures and the pictures are corrupted, you can easily play left and right, up and down, from the style section. Examples are on Config.

# Config.Table

- What the titles here do are written next to them in the config as an explanation. (Example : _https://ibb.co/VHKPGP5_)

- You can easily change the names, nicknames, pictures and required amount of coins of vehicles and items in seconds.

- In addition, if the photos are corrupted while adding photos to items or vehicles, you can easily change them via the config as you can see in the example.  (Example : _https://ibb.co/2y9gHHz_)

[Alt text](relative/path/to/https://ibb.co/2y9gHHz?raw=true "Title")
[Alt text](https://ibb.co/2y9gHHz/2y9gHHz?raw=true "Title")

# How is the system connected to tebex?

- Step 1
Login to Tebex

- Step 2 
Click Game Servers
https://im.ge/i/OBBaRc

- Step 3
Click Add Command
https://im.ge/i/OBBILG


- Step 4
Write them in the places you see in the picture and press the update button. That's it.
```buypack {"tid": "{transaction}",  "mail": "{email}", "pname": "{packageName}", "price": "{price}"}```
https://im.ge/i/OBBU4a

- Step 5
After purchasing, such a code will appear on the screen. tbx-4235671352a39516-02b362. He will write this code in the menu in the game after an average of 10 minutes and get his coin.
https://im.ge/i/OBBy48


# Premium Member Discount System

- As you know, if you become a premium member, you can make discounts wherever you want.
- For example, I want premium members to get a discount when buying gas, let's do that.

Let's say you have such a money wipe command for a gas station.
```
RegisterNetEvent("frkn-fuelstation:server:PayForFuel", function(amount)
    local src = source
    if not src then return end
    local player = ESX.GetPlayerFromId(src)
    if not player then return end
    player.removeMoney(amount)
end)
```
All you have to do is delete the player.removeMOney(amount) part and add TriggerServerEvent('frkn-vipsystemv2:percent',amount).
so it should look like below

```
RegisterNetEvent("frkn-fuelstation:server:PayForFuel", function(amount)
    local src = source
    if not src then return end
    local player = ESX.GetPlayerFromId(src)
    if not player then return end
    TriggerServerEvent('frkn-vipsystemv2:percent',amount)
end)
The amount written here may vary depending on your code. If you can't, you can contact me at the addresses at the bottom of the page.


# CONTACT

If there is a problem or you want to ask a question Discord: Furkann#4645 or [Discord 0RESMON](discord.gg/0resmon)
