# What if we decided to replace our animal-sourced food with plant-sourced food ? : The environmental impact of agricultural changes

In this synthesis, I'll try to explain the methodology behind this project and how some changes in agricultural practices can positively impact the planet.

## Methodology

First of all, we are using the FAO Stat (https://www.fao.org/faostat/en/#data) and Water footprint Network Data (https://waterfootprint.org/en/resources/waterstat/product-water-footprint-statistics/) - more details can be found in the script - to assess this problem.

This analysis will concern 4 categories :

- Greenhouse Gas Emissions
- Land Use
- Water Use
- Calories

In order to get our results, we separate data between animal-sourced products and plant-sourced products.
Animal-sourced products do not contain production of fishery, only "in-land" animals.

Once we have the distinction between animal and plant products, we will be suming all the values to make the comparaison easier between these two categories.

This way, we can calculate the evolution if we reduce our animal-sourced products and replace them with plant-sourced products.

In this exercise, we will be calculating the remplacement on a constant production value. (meaning that 100KG of animal-sourced products is replaced by 100KG of plant-sourced products)

Moreover, we simulate the effect of less manure on the production of plant-based products.
What I decided to take as hypothesis was that if animal-sourced food decreased, manure would become harder and harder to get until there would be none at all, if replaced 100% of animal products.

So, we need to calculate how many more resources are needed to compensate this deficit and reach the same production as before, with manure.

This is the logic : The more we decrease, the more resources we need to compensate.

The way to calculate this replacement is the following :

- We caculate the ratios between the category concerned (emissions etc...) and the production (separated between animal and plant)
- We calculate the percentage of animal-sourced products that are replaced with plant-sourced products (75% for example)
- Then, we distribute this percentage between animal and plant products (25% animal and 75% plant with the example above)
- Next, we calculate the new production values with the ratios previously calculated. (example : 75% of plant production is converted to plant Greenhouse Gas Emissions - which is far less emissive per Ton than an animal sourced product)
- Finally, we calculate a new total and an actual total so that we can get a variation and draw a conclusion

We then plot it, and get the results bellow.

## Results

This graph is an example of the results if 100% of animal-sourced products were replaced with plant-sourced products.

And the graph bellow is the effect of this transition on calories. The discontinued line corresponds to the NHS calorie recommendation when we average men and woman recommendation. (2500kcal for men - 2000kcal for women, knowing that the world is more or less composed of half/half, 2250kcal per person on a daily baisis is a good reference)

It does not take into account fishery.
It takes into account manure that decreases.

![newplot (4)](https://user-images.githubusercontent.com/117353586/199954203-fa4443f9-16f2-48e5-883f-26e5073bd602.png)

![newplot (9)](https://user-images.githubusercontent.com/117353586/199956152-cae4ea1d-8a5a-47c7-98c7-e43b243d0078.png)

If we replaced 100% of animal-sourced products with plant-sourced products, we could save up to 65% in land use, 53% in greenhouse gas emissions, 18% in water use and still be above the NHS caloric recommendations to stay healthy.

## Quotations

