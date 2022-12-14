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
This analysis only concerns the "agriculture" part of food, other data (industrialization, packaging, transportation etc.) being hard to distinguish between animal and plant-based food. (data hard to get)

Once we have the distinction between animal and plant products, we will be suming all the values to make the comparaison easier between these two categories.

This way, we can calculate the evolution if we reduce our animal-sourced products and replace them with plant-sourced products.

In this exercise, we will be calculating the remplacement on a constant production value. (meaning that 100KG of animal-sourced products is replaced by 100KG of plant-sourced products)

Moreover, we simulate the effect of less manure on the production of plant-based products.
What I decided to take as hypothesis was that if animal-sourced food decreased, manure would become harder and harder to get until there would be none at all, if replaced 100% of animal products.

So, we need to calculate how many more resources are needed to compensate this deficit and reach the same production as before, with manure.

This is the logic : The more we decrease, the more resources we need to compensate.
13% of total fertilizers come from manure.
According to Stewart & al (2005), 40% on average of total crop yield is attributable to commercial fertilizers input.
So, if we take this 40%, we get an increase of 66% due to fertilizers. (for example in 100 crop total production, 40 is due to fertilizers and 60 is not. 100/60 = 1.66, which is the 66% increase of getting to 100 vs starting with 60)

This means that by adding fertilizers to agriculture, crop yields can increase up to 66%.
Therefore, if we take 66% of the 13% of fertilizers from manure, it gives us the reference of 8,27%.
The efficiency of manure is therefore 8,27% at 100% animal product reduction, if we reduce animal products by 50%, I assume that manure effect will only be 4,135%, at 0% it'll be 0% and production will not be affected by resource increase to compensate.

This way, we can take this 8,27% value (or less if we increase animal product reduction), add 1 and multiply it on the resources (land, emissions, water) to compensate production for the loss in fertilizer. 

Once we increase the resources by this manure coeficient, the way to calculate the replacement from animal-based products to plant-based products is the following :

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

If we replaced 100% of animal-sourced products with plant-sourced products, we could save up to 65% in land use, 53% in greenhouse gas emissions, 18% in water use and still be above the NHS calorie intake recommendation to stay healthy.

## Quotations

Mekonnen, M.M. and Hoekstra, A.Y. (2010) The green, blue and grey water footprint of farm animals and animal products, Value of Water Research Report Series No. 48, UNESCO-IHE, Delft, the Netherlands.

Mekonnen, M.M. and Hoekstra, A.Y. (2010) The green, blue and grey water footprint of crops and derived crop products, Value of Water Research Report Series No. 47, UNESCO-IHE, Delft, the Netherlands.

Food and Agriculture Organization of the United Nations - FAOSTAT

Poore, J., & Nemecek, T. (2018). Reducing food???s environmental impacts through producers and consumers. Science, 360(6392), 987-992. ==> https://www.science.org/doi/10.1126/science.aaq0216

https://www.climatewatchdata.org/data-explorer/historical-emissions?historical-emissions-data-sources=cait&historical-emissions-gases=all-ghg&historical-emissions-regions=All%20Selected&historical-emissions-sectors=total-including-lucf&page=1

Citation,"Climate Watch Historical GHG Emissions. 2022. Washington, DC: World Resources Institute. Available online at: https://www.climatewatchdata.org/ghg-emissions"

https://www.nhs.uk/common-health-questions/food-and-diet/what-should-my-daily-intake-of-calories-be/

Stewart & al (2005) The Contribution of Commercial Fertilizer Nutrients to Food Production - Agronomy Journal
https://acsess.onlinelibrary.wiley.com/doi/abs/10.2134/agronj2005.0001

UN World Water Development Report 2022
https://www.unesco.org/reports/wwdr/2022/en/agriculture#:~:text=Summary&text=Currently%2070%25%20of%20global%20groundwater,is%20serviced%20by%20this%20resource.

Land Use - Hannah Ritchie and Max Roser - Our World in Data
https://ourworldindata.org/land-use
