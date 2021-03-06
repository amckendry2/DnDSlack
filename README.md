# DnDSlack
Google Sheets API for running D&amp;D games via Slack

The API is accessed using slash commands in a Slack chat. The commands can read and update a Google Sheets page containing various character stats, simulate dice rolls, and return messages containing the results of user actions. I created this to assist in running an actual text-based D&D campaign.

**COMMAND TEMPLATE**: 
<pre>
/:slash command [required params] (optional params) ("literal optional param") (:optional end param)
</pre>

**BASIC ROLL**
<pre>
/:roll           [amount]     
</pre>

**ATTACKS**  
<pre>
/:attack         [character] [ability]      ("adv"/"dis") (:weapon/spell name) ->   character makes attack roll    
/:monattack      [character] [attack bonus] ("adv"/"dis") (:enemy name)        ->   NPC attacks character
</pre>

**DAMAGE** 
<pre>
/:damage         [character] [amount] ("crit") (:damage type)                  ->   character makes damage roll    
/:hit            [character] [amount]          (:damage type)                  ->   character takes damage
/:monhit         [character] [amount] ("crit") (:enemy name)                   ->   NPC attacks character
/:heal           [character] [amount]                                          ->   character gains hp    
/:maxhp          [character]                                                   ->   restore character to max hp    
/:weapon         [character] [melee1/melee2/ranged1/ranged2] ("crit")          ->   character deals damage with weapon     
/:spell          [character] [spell1/spell2/spell3/spell4]   ("crit")          ->   character deals damage with spell    
</pre>

**CHECKS** 
<pre>
/:ability        [character] [ability] ("adv"/"dis")                           ->   character makes an ability check    
/:skill          [character] [skill]   ("adv"/"dis")                           ->   character makes skill check    
/:save           [character] [ability] ("adv"/"dis")                           ->   character makes saving throw    
/:initiative     [character]           ("adv"/"dis")                           ->   character rolls for initiative    
</pre>

**HIT DIE** 
<pre>
/:usehd          [character]                                                   ->   character uses a hit die      
/:longrest       [character]                                                   ->   character takes a long rest    
</pre>

**ENCUMBRANCE** 
<pre>
/:pickup         [character] [amount]                                          ->   character picks up weight    
/:drop           [character] [amount]                                          ->   character drops weight    
</pre>

**OPTIONAL POINTS** 
<pre>
/:addpoints      [character] [points]                                          ->   add points to character's optional stat pool    
/:usepoints      [character] [points]                                          ->   subtract points from character's optional stat pool    
/:maxpoints      [character]                                                   ->   restore character's optional stat pool to max   
</pre>

**INSPIRATION** 
<pre>
/:tipfedora      [character]                                                   ->   DM awards character an inspiration point    
/:useinspiration [character]                                                   ->   character uses an inspiration point    
</pre>

**STATUS**
<pre>
/:status         [character]                                                   ->   check character's status   
</pre>
                                                                                                                                                                   
Images of actual usage:

![alt text](https://i.ibb.co/2NNLV8W/image0-2.png)
![alt text](https://i.ibb.co/9G8rz40/image0-3.png)
![alt text](https://i.ibb.co/z27NhZ4/image1-2.png)

