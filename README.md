# Monopoly Kata

* Put Code Complete checklists into practice
* TDD

## Requirements

Implement the rules based on the wikipedia page:

* https://en.wikipedia.org/wiki/Monopoly_(game)
* https://monopoly.fandom.com/wiki/Main_Page

### Rules ###

* Players take turns in order with the initial player determined by chance before the game. 
* A typical turn begins with the rolling of the dice and advancing a piece clockwise around the board the corresponding number of squares.
* If a player rolls doubles, they roll again after completing that portion of their turn. 
* A player who rolls three consecutive sets of doubles on one turn has been "caught speeding" and is immediately sent to jail instead of moving the amount shown on the dice for the third roll.
* A player who lands on or passes the Go space collects $200 from the bank.
* Players who land on either Income Tax or Luxury Tax pay the indicated amount to the bank.
  * Income Tax: $200
  * Luxury Tax: $100 
* No reward or penalty is given for landing on Free Parking.
* Properties can only be developed once a player owns all the properties in that color group.
  * They then must be developed equally.
  * A house must be built on each property of that color before a second can be built.
  
### Board ###

https://monopoly.fandom.com/wiki/Monopoly_Board

<table>
    <tr>
        <td align="center">Free Parking</td>
        <td align="center"><a href="#kentucky_ave">(red)<br/>Kentucky Avenue<br/>$220</a></td>
        <td align="center">Chance</td>
        <td align="center">(red)<br/>Indiana Avenue<br/>$220</td>
        <td align="center">(red)<br/>Illinois Avenue<br/>$240</td>
        <td align="center">B. & O. Railroad<br/>$200</td>
        <td align="center">(yellow)<br/>Atlantic Avenue<br/>$260</td>
        <td align="center">(yellow)<br/>Ventnor Avenue<br/>$260</td>
        <td align="center">Water Works<br/>$150</td>
        <td align="center">(yellow)<br/>Marvin Gardens<br/>$280</td>
        <td align="center">Go To Jail</td>
    </tr>
    <tr>
        <td align="center">(orange)<br/>New York Avenue<br/>$200</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">(green)<br/>Pacific Avenue<br/>$300</td>
    </tr>
    <tr>
        <td align="center">(orange)<br/>Tennessee Avenue<br/>$180</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">(green)<br/>North Carolina Avenue<br/>$300</td>
    </tr>
    <tr>
        <td align="center">Community Chest</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">Community Chest</td>
    </tr>
    <tr>
        <td align="center">(orange)<br/>St. James Place<br/>$180</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">(green)<br/>Pennsylvania Avenue<br/>$320</td>
    </tr>
    <tr>
        <td align="center">Pennsylvania Railroad<br/>$200</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">Short Line<br/>$200</td>
    </tr>
    <tr>
        <td align="center">(pink)<br/>Virginia Avenue<br/>$160</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">Chance</td>
    </tr>
    <tr>
        <td align="center">(pink)<br/>States Avenue<br/>$140</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">(blue)<br/>Park Place<br/>$350</td>
    </tr>
    <tr>
        <td align="center">Electric Company<br/>$150</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">Luxury Tax<br/>Pay $100</td>
    </tr>
    <tr>
        <td align="center">(pink)<br/>St. Charles Place<br/>$140</td>
        <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
        <td align="center">(blue)<br/>Boardwalk<br/>$400</td>
    </tr>
    <tr>
        <td align="center">In Jail / Just Visiting</td>
        <td align="center">(lt blue)<br/>Connecticut Avenue<br/>$120</td>
        <td align="center">(lt blue)<br/>Vermont Avenue<br/>$100</td>
        <td align="center">Chance</td>
        <td align="center">(lt blue)<br/>Oriental Avenue<br/>$100</td>
        <td align="center">Reading Railroad<br/>$200</td>
        <td align="center">Income Tax<br/>Pay $200</td>
        <td align="center">(brown)<br/>Baltic Avenue<br/>$60</td>
        <td align="center">Community Chest</td>
        <td align="center">(brown)<br/>Mediterranean Avenue<br/>$60</td>
        <td align="center">Go / Collect $200 salary</td>
    </tr>
</table>
  
### Chance or Community Chest ###

If a player lands on a Chance or Community Chest space, they draw the top card from the respective deck and follow its instructions. This may include collecting or paying money to the bank or another player or moving to a different space on the board.

#### Chance Cards ####

https://monopoly.fandom.com/wiki/Chance

1. Advance to "Go". (Collect $200)
1. Advance to Illinois Ave. If you pass Go, collect $200
1. Advance to St. Charles Place. If you pass Go, collect $200.
1. Advance token to nearest Utility. If unowned, you may buy it from the Bank. If owned, throw dice and pay owner a total 10 times the amount thrown.
1. Advance token to the nearest Railroad and pay owner twice the rental to which he/she {he} is otherwise entitled. If Railroad is unowned, you may buy it from the Bank.
1. Bank pays you dividend of $50.
1. Get out of Jail Free (This card may be kept until needed, or traded/sold.)
1. Go Back Three Spaces.
1. Go to Jail. (Go directly to Jail. Do not pass GO, do not collect $200.)
1. Make general repairs on all your property: For each house pay $25, For each hotel pay $100.
1. Pay poor tax of $15.
1. Take a trip to Reading Railroad. If you pass Go, collect $200.
1. Take a walk on the Boardwalk.
1. You have been elected Chairman of the Board. Pay each player $50.
1. Your building loan matures. Receive $150.
1. You have won a crossword competition. Collect $100.

#### Community Chest ####
 
https://monopoly.fandom.com/wiki/Community_Chest
 
1. Advance to "Go". (Collect $200)
1. Bank error in your favor. Collect $200
1. Doctor's fees. Pay $50.
1. From sale of stock you get $50.
1. Get out of Jail Free (This card may be kept until needed, or traded/sold.)
1. Go to Jail. (Go directly to Jail. Do not pass GO, do not collect $200.)
1. Grand Opera Night. Collect $50 from every player for opening night seats.
1. Holiday Fund matures. Receive $100.
1. Income tax refund. Collect $20.
1. It is your birthday. Collect $10 from every player.
1. Life insurance matures - Collect $100
1. Hospital Fees. Pay $50.
1. School fees. Pay $50.
1. Receive $25 consultancy fee.
1. You are assessed for street repairs: Pay $40 per house and $115 per hotel you own.
1. You have won second prize in a beauty contest. Collect $10.
1. You inherit $100.

### Jail ###

A player is sent to jail for doing any of the following:

* Landing directly on the "Go to Jail" space
* Throwing three consecutive doubles in one turn
* Drawing a "Go to Jail" card from Chance or Community Chest

When a player is sent to jail, they move directly to the Jail space and their turn ends ("Do not pass Go. Do not collect $200."). 

If an ordinary dice roll (not one of the above events) ends with the player's token on the Jail corner, they are "Just Visiting" and can move ahead on their next turn without incurring any penalty.

If a player is in jail, they do not take a normal turn and must either pay a fine of $50 to be released, use a Chance or Community Chest Get Out of Jail Free card, or attempt to roll doubles on the dice. 

If a player fails to roll doubles, they lose their turn. 
 
Failing to roll doubles for three consecutive turns requires the player to either pay the $50 fine or use a Get Out of Jail Free card, after which they move ahead according to the total rolled.

Players in jail may not buy properties directly from the bank since they are unable to move.

They can engage all other transactions, such as mortgaging properties, selling/trading properties to other players, buying/selling houses and hotels, collecting rent, and bidding on property auctions.

A player who rolls doubles to leave jail does not roll again.

If the player pays the fine or uses a card to get out and then rolls doubles, they do take another turn. 

### Properties ###

If the player lands on an unowned property, whether street, railroad, or utility, they can buy the property for its listed purchase price.

If they decline this purchase, the property is auctioned off by the bank to the highest bidder, including the player who declined to buy.
 
If the property landed on is already owned and unmortgaged, they must pay the owner a given rent; the amount depends on whether the property is part of a set or its level of development.

When a player owns all the properties in a color group and none of them are mortgaged, they may develop them during their turn or in between other player's turns.

Development involves buying miniature houses or hotels from the bank and placing them on the property spaces.

This must be done uniformly across the group. A second house cannot be built on any property within a group until all of them have one house.

Once the player owns an entire group, they can collect double rent for any undeveloped properties within it.

Although houses and hotels cannot be built on railroads or utilities, the given rent increases if a player owns more than one of either type.

### Mortgaging ###

Properties can also be mortgaged, although all developments on a monopoly must be sold before any property of that color can be mortgaged or traded.

The player receives half the purchase price from the bank for each mortgaged property. 

This must be repaid with 10% interest to clear the mortgage.

Houses and hotels can be sold back to the bank for half their purchase price.

Players cannot collect rent on mortgaged properties.

Trading mortgaged properties is allowed. The player receiving the mortgaged property must:
* immediately pay the bank the mortgage price plus 10% or 
* pay just the 10% amount and keep the property mortgaged. they must pay the 10% again when they pay off the mortgage.

### Bankruptcy ###

A player who cannot pay what they owe is bankrupt and eliminated from the game.

If the bankrupt player owes the bank, they must turn all their assets over to the bank, who then auctions off their properties (if they have any), except buildings.

If the debt is owed to another player instead, all assets are given to that opponent, except buildings which must be returned to the bank.

The new owner must either pay off any mortgages held by the bank on such properties received or pay a fee of 10% of the mortgaged value to the bank if they choose to leave the properties mortgaged.

The winner is the remaining player left after all of the others have gone bankrupt.

If a player runs out of money but still has assets that can be converted to cash, they can do so by selling buildings, mortgaging properties, or trading with other players. To avoid bankruptcy the player must be able to raise enough cash to pay the full amount owed.

A player cannot choose to go bankrupt; if there is any way to pay what they owe, even by returning all their buildings at a loss, mortgaging all their real estate and giving up all their cash, even knowing they are likely going bankrupt the next time, they must do so.

#### Deeds ####

A title deed for each property is given to a player to signify ownership, and specifies purchase price, mortgage value, the cost of building houses and hotels on that property, and the various rents depending on how developed the property is. Properties include:

##### Brown Group #####

<table>
    <tr><td align="center">Mediterranean Avenue</td></tr>
    <tr><td align="center">Rent $2</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$10</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$30</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$90</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$100</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $250</td></tr>
    <tr><td align="center">Mortgage Value $30</td></tr>
    <tr><td align="center">Houses cost $50 each</td></tr>
    <tr><td align="center">Hotels $50, plus 4 houses</td></tr>
</table>
            
<table>
    <tr><td align="center">Baltic Avenue</td></tr>
    <tr><td align="center">Rent $4</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$20</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$60</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$180</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$320</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $450</td></tr>
    <tr><td align="center">Mortgage Value $30</td></tr>
    <tr><td align="center">Houses cost $50 each</td></tr>
    <tr><td align="center">Hotels $50, plus 4 houses</td></tr>
</table>

##### Light Blue Group #####

<table>
    <tr><td align="center">Oriental Avenue</td></tr>
    <tr><td align="center">Rent $6</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$30</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$90</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$270</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$400</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $550</td></tr>
    <tr><td align="center">Mortgage Value $50</td></tr>
    <tr><td align="center">Houses cost $50 each</td></tr>
    <tr><td align="center">Hotels $50, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Vermont Avenue</td></tr>
    <tr><td align="center">Rent $6</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$30</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$90</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$270</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$400</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $550</td></tr>
    <tr><td align="center">Mortgage Value $50</td></tr>
    <tr><td align="center">Houses cost $50 each</td></tr>
    <tr><td align="center">Hotels $50, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Connecticut Avenue</td></tr>
    <tr><td align="center">Rent $8</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$40</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$300</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$450</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $600</td></tr>
    <tr><td align="center">Mortgage Value $60</td></tr>
    <tr><td align="center">Houses cost $50 each</td></tr>
    <tr><td align="center">Hotels $50, plus 4 houses</td></tr>
</table>

##### Pink Group #####

<table>
    <tr><td align="center">St. Charles Place</td></tr>
    <tr><td align="center">Rent $10</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$150</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$450</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$625</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $750</td></tr>
    <tr><td align="center">Mortgage Value $70</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">States Avenue</td></tr>
    <tr><td align="center">Rent $10</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$150</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$450</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$625</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $750</td></tr>
    <tr><td align="center">Mortgage Value $70</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Virginia Avenue</td></tr>
    <tr><td align="center">Rent $12</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$60</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$180</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$500</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$700</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $900</td></tr>
    <tr><td align="center">Mortgage Value $70</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

##### Orange Group #####

<table>
    <tr><td align="center">St. James Place</td></tr>
    <tr><td align="center">Rent $14</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$70</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$280</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$550</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$750</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $950</td></tr>
    <tr><td align="center">Mortgage Value $90</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Tennessee Avenue</td></tr>
    <tr><td align="center">Rent $14</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$70</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$280</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$550</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$750</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $950</td></tr>
    <tr><td align="center">Mortgage Value $90</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">New York Avenue</td></tr>
    <tr><td align="center">Rent $16</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$80</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$220</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$600</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$800</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1000</td></tr>
    <tr><td align="center">Mortgage Value $100</td></tr>
    <tr><td align="center">Houses cost $100 each</td></tr>
    <tr><td align="center">Hotels $100, plus 4 houses</td></tr>
</table>

##### Red Group #####

<a name="kentucky_ave"></a>
<table>
    <tr><td align="center">Kentucky Avenue</td></tr>
    <tr><td align="center">Rent $18</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$90</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$250</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$700</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$875</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1050</td></tr>
    <tr><td align="center">Mortgage Value $110</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Indiana Avenue</td></tr>
    <tr><td align="center">Rent $18</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$90</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$250</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$700</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$875</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1050</td></tr>
    <tr><td align="center">Mortgage Value $110</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Illinois Avenue</td></tr>
    <tr><td align="center">Rent $20</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$300</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$750</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$925</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1100</td></tr>
    <tr><td align="center">Mortgage Value $120</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

##### Yellow Group #####

<table>
    <tr><td align="center">Atlantic Avenue</td></tr>
    <tr><td align="center">Rent $22</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$110</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$330</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$800</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$975</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1150</td></tr>
    <tr><td align="center">Mortgage Value $130</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Ventnor Avenue</td></tr>
    <tr><td align="center">Rent $22</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$110</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$330</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$800</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$975</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1150</td></tr>
    <tr><td align="center">Mortgage Value $130</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Marvin Gardens</td></tr>
    <tr><td align="center">Rent $24</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$120</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$360</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$850</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1025</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1200</td></tr>
    <tr><td align="center">Mortgage Value $140</td></tr>
    <tr><td align="center">Houses cost $150 each</td></tr>
    <tr><td align="center">Hotels $150, plus 4 houses</td></tr>
</table>

##### Green Group #####

<table>
    <tr><td align="center">Pacific Avenue</td></tr>
    <tr><td align="center">Rent $26</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$130</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$390</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$900</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1100</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1275</td></tr>
    <tr><td align="center">Mortgage Value $150</td></tr>
    <tr><td align="center">Houses cost $200 each</td></tr>
    <tr><td align="center">Hotels $200, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">North Carolina Avenue</td></tr>
    <tr><td align="center">Rent $26</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$130</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$390</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$900</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1100</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1275</td></tr>
    <tr><td align="center">Mortgage Value $150</td></tr>
    <tr><td align="center">Houses cost $200 each</td></tr>
    <tr><td align="center">Hotels $200, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Pennsylvania Avenue</td></tr>
    <tr><td align="center">Rent $28</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$150</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$450</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$1000</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1200</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1400</td></tr>
    <tr><td align="center">Mortgage Value $160</td></tr>
    <tr><td align="center">Houses cost $200 each</td></tr>
    <tr><td align="center">Hotels $200, plus 4 houses</td></tr>
</table>

##### Blue Group #####

<table>
    <tr><td align="center">Park Place</td></tr>
    <tr><td align="center">Rent $35</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$175</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$500</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$1100</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1300</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $1500</td></tr>
    <tr><td align="center">Mortgage Value $175</td></tr>
    <tr><td align="center">Houses cost $200 each</td></tr>
    <tr><td align="center">Hotels $200, plus 4 houses</td></tr>
</table>

<table>
    <tr><td align="center">Boardwalk</td></tr>
    <tr><td align="center">Rent $50</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>With 1 House</td>
                    <td>$200</td>
                </tr>
                <tr>
                    <td>With 2 Houses</td>
                    <td>$600</td>
                </tr>
                <tr>
                    <td>With 3 Houses</td>
                    <td>$1400</td>
                </tr>
                <tr>
                    <td>With 4 Houses</td>
                    <td>$1700</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">With Hotel $2000</td></tr>
    <tr><td align="center">Mortgage Value $200</td></tr>
    <tr><td align="center">Houses cost $200 each</td></tr>
    <tr><td align="center">Hotels $200, plus 4 houses</td></tr>
</table>

#### Railroads ####

<table>
    <tr><td align="center">Reading Railroad</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>Rent</td>
                    <td>$25</td>
                </tr>
                <tr>
                    <td>If 2 RR's are owned</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>If 3 RR's are owned</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>If 4 RR's are owned</td>
                    <td>$200</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $100</td></tr>
</table>

<table>
    <tr><td align="center">Pennsylvania Railroad</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>Rent</td>
                    <td>$25</td>
                </tr>
                <tr>
                    <td>If 2 RR's are owned</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>If 3 RR's are owned</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>If 4 RR's are owned</td>
                    <td>$200</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $100</td></tr>
</table>

<table>
    <tr><td align="center">B. & O. Railroad</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>Rent</td>
                    <td>$25</td>
                </tr>
                <tr>
                    <td>If 2 RR's are owned</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>If 3 RR's are owned</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>If 4 RR's are owned</td>
                    <td>$200</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $100</td></tr>
</table>

<table>
    <tr><td align="center">Short Line</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>Rent</td>
                    <td>$25</td>
                </tr>
                <tr>
                    <td>If 2 RR's are owned</td>
                    <td>$50</td>
                </tr>
                <tr>
                    <td>If 3 RR's are owned</td>
                    <td>$100</td>
                </tr>
                <tr>
                    <td>If 4 RR's are owned</td>
                    <td>$200</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $100</td></tr>
</table>

#### Utilities ####

<table>
    <tr><td align="center">Electric Company</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>If one "Utility" is owned rent is 4 times amount shown on dice.</td>
                </tr>
                <tr>
                    <td>If both "Utilities" are owned rent is 10 times shown on dice.</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $75</td></tr>
</table>
 
<table>
    <tr><td align="center">Water Works</td></tr>
    <tr>
        <td>
            <table>
                <tr>
                    <td>If one "Utility" is owned rent is 4 times amount shown on dice.</td>
                </tr>
                <tr>
                    <td>If both "Utilities" are owned rent is 10 times shown on dice.</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr><td align="center">Mortgage Value $75</td></tr>
</table>
