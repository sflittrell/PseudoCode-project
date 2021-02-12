# Pseudo Code Project
## Make the Perfect Cup of Tea

#### Functionality (use case): 
This program is made to create the perfect cup of tea for a user, based on their personal preferences.

#### Define Objects:
 	- electricTeaKettle: Used to heat water to specific temperatures
	- water: base liquid used to brew tea (among other things)
	- teaCup: Used to hold a specific amount of water (8 fluid oz) and insulate from high temperatures
	- teaBag: a small porous sachet containing an assortment of ground tea, suitable for making a single cup at 8 fluid oz.
	- spoon: used for stirring condiments into tea after brewing
	- timer: used to measure a specific amount of time
	condiments: items to modify/enhance the flavor of the tea that the user can choose from


#### Variables:
	- cupSize: user defined selection of a small 8 oz cup or a large 16 oz cup
		[smallCup, largeCup]
 	- teaType: a selection of available teas the user can pick from
		[greenTea, earlGray (Black tea), peppermintTea (Herbal tea), irishBreakfastTea (Black tea), oolongTea]
	- condimentSelection: a selection of available condiments that can be added to tea
  		[sugar, milk, lemon]

### Start Program
	INIT userCreation
		CREATE user //Creates the user who will be requesting the tea along with all of their personal tea preferences

	INIT teaPreference
		GET teaSelection from user //User can choose one type of tea from teaType.
		GET cupSize from user //User selects what size cup they want, small or large

	INIT objectCreation
		CREATE electricTeaKettle
		CREATE water
		CREATE teaCup === cupSize.userDefined //Creates whichever size cup based on the users selection
		CREATE teaBag === teaType.userDefined //Creates the tea bag containing tea based on the selection made by the user
		IF cupSize === largeCup repeat CREATE teaBag // creates a second tea bag for the 16 oz cup
		CREATE spoon
		CREATE timer

	GET water, filling electricTeaKettle

	INIT heatWater
		IF teaType  === geenTea set temperature to 160 degrees Fahrenheit
		ELSE IF teaType === oolongTea set temperature to 190 degrees Fahrenheit
		ELSE set temperature to 212 degrees Fahrenheit
		WAIT for water to reach desired temperature

	INIT brewTea
		GET teaCup
		PLACE teaBag(s) in teaCup //number of tea bags is determined by 
		POUR heated water into teaCup
		IF teaType  === geenTea let steep for 2 minutes using timer
		ELSE IF teaType === oolongTea let steep for 3 minutes using timer
		ELSE IF teaType === earlGray let steep for 4 minutes using timer
		ELSE let steep for 5 minutes using timer
		REMOVE teaBag and squeeze out excess liquid over cup
		REPEAT last step if there is a second teaBag
		DISCARD teaBag(s)


	INIT condimentPreference
		CREATE [condiments] === condimentSelection.userDefined // creates the condiments that the user selects from the list of available options
		IF teaType === greenTea and [condiments] contain sugar
		add sugar to tea
		IF teaType === greenTea and [condiments] contain lemon
		add lemon to tea
		IF teaType === oolongTea and [condiments] contain sugar
		add sugar to tea
		IF teaType === oolongTea and [condiments] contain lemon
		add lemon to tea
		IF teaType === oolongTea and [condiments] contain milk
		add milk to tea
		IF teaType === earlGrey and [condiments] contain sugar
		add sugar to tea
		IF teaType === earlGrey and [condiments] contain lemon
		add lemon to tea
		IF teaType === peppermintTea and [condiments] contain sugar
		add sugar to tea
		IF teaType === irishBreakfastTea and [condiments] contain sugar
		add sugar to tea
		IF teaType === irishBreakfastTea and [condiments] contain milk
		add milk to tea

	Stir tea with spoon until combined

	Let tea cool until it reaches reasonable temperature to drink (approximately 140 degrees Fahrenheit)

	DRINK tea

END Program
