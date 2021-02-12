# Pseudo Code Project
## Make the Perfect Cup of Tea

### Functionality (use case): 
This program is made to create the perfect cup of tea for a user, based on their personal preferences.

### Define Objects:
   - **electricTeaKettle:** used to heat water to specific temperatures
   - **water:** base liquid used to brew tea
   - **teaCup:** used to hold a specific amount of water and insulate from high temperatures
   - **teaBag:** a small porous sachet containing an assortment of ground tea, suitable for making a single cup at 8 fluid oz.
   - **spoon:** used for stirring condiments into tea after brewing
   - **timer:** used to measure a specific amount of time
   - **condiments:**  items to modify/enhance the flavor of the tea


### Define Variables:
   - **cupSize:** user defined selection of a small 8 oz cup or a large 16 oz cup
        <span style="color: green">[smallCup, largeCup]</span>
   - **teaType:** a selection of available teas the user can pick from
        <span style="color: green">[greenTea, earlGray (Black tea), peppermintTea (Herbal tea), irishBreakfastTea (Black tea), oolongTea]</span>
   - **condimentSelection:** a selection of available condiments that can be added to tea
   <span style="color: green">[sugar, milk, lemon]</span>

#### Start Program
    INIT userCreation
        CREATE user // *Creates the user who will be requesting the tea along with all of their personal tea preferences*

    INIT teaPreference
        GET teaSelection from user // *User can choose one type of tea from teaType*
        GET cupSize from user // *User selects what size cup they want, small or large*

    INIT objectCreation
        CREATE electricTeaKettle
        CREATE water
        CREATE teaCup === cupSize.userDefined // *Creates whichever size cup based on the users selection*
        CREATE teaBag === teaType.userDefined // *Creates the tea bag containing tea based on the selection made by the user*
        IF cupSize === largeCup repeat CREATE teaBag // *Creates a second tea bag for the 16 oz cup*
        CREATE spoon
        CREATE timer

    GET water, filling electricTeaKettle

    INIT heatWater
        IF teaType === geenTea set temperature to 160 degrees Fahrenheit
        ELSE IF teaType === oolongTea set temperature to 190 degrees Fahrenheit
        ELSE set temperature to 212 degrees Fahrenheit
        PRESS start on electricTeaKettle
        WAIT for water to reach desired temperature

    INIT brewTea
        GET teaCup
        GET teaBag(s) and place in teaCup // *Number of tea bags is determined by cupSize*
        POUR heated water into teaCup
        IF teaType === geenTea let steep for 2 minutes, using timer to measure time
        ELSE IF teaType === oolongTea let steep for 3 minutes, using timer to measure time
        ELSE IF teaType === earlGray let steep for 4 minutes, using timer to measure time
        ELSE let steep for 5 minutes, using timer to measure time
        REMOVE teaBag and squeeze out excess liquid over cup
        REPEAT last step if there is a second teaBag
        DISCARD teaBag(s)

    INIT condimentPreference
        CREATE [condiments] === condimentSelection.userDefined // *Creates an array of the condiments that the user selects from the list of available options*
        // *If the user selected a condiment from the options given and that condiment is compatible with a given tea then the condiment will be added to the tea*
        IF [condiments] contain sugar AND teaType === greenTea OR oolongTea OR earlGrey OR peppermintTea OR irishBreakfastTea 
        add sugar to tea
        IF [condiments] contain lemon AND teaType === greenTea OR earlGrey
        add lemon to tea
        IF [condiments] contain milk AND teaType === irishBreakfastTea
        add milk to tea

    Stir tea with spoon until combined

    Let tea cool until it reaches reasonable temperature to drink (approximately 140 degrees Fahrenheit)

    DRINK tea

END Program
