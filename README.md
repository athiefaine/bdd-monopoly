# Behaviour-Driven Development kata: Monopoly

[Monopoly rules](https://simple.wikipedia.org/wiki/Monopoly_(game))

![Classic edition Board](resources/classic_board.jpg)


### Some examples

#### Go pass

```gherkin
Scenario: Player Emma passes Go and gets rewarded
  Given player Emma owns 400M
  When player Emma passes Go
  Then player Emma receives 200M
  And player Emma owns 600M
```
<details><summary> Spoiler alert</summary>
Is this always true? What happens if the Bank has no money?

</details>

#### Property set

```gherkin
Scenario: Player Patrick buys a property set
  Given player Patrick owns 2 properties of the same colour
  When he buys a third property within the same colour
  Then the properties value is increased
  And he can buy buildings
```

Find some code smells

<details><summary> Spoiler alert</summary>
<p>

* isn't it a rule disguised as an example?
  * what specific colour?
  * what properties are owned? which property is missing?
* shouldn't we recall player Patrick for each step?
* properties value is increased: how much? what was the initial value of the property set? what is the final value?
* player Patrick can buy buildings: it is a possibility, not a fact
   * => provide an example where the player owns a property set as a pre-requisite and he buys a building
</p>
</details>
