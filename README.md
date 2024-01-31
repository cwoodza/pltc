# PolicyLab Trade Classifications (pltc)

## Overview

pltc are a set of useful classification systems for trade data, which aim to enable policy analysis and interoperability with other economic data. 

There are three core parts to pltc. (1) The Narrative Classification System, or NCS, is a simplified classification system for translating HS6 level products into more manageable groups of Sectors, Sub-sectors, Product types and Products. (2) The Narrative Value Chain, or NVC, classification provides a mapping of products into inputs and end uses, with the aim of enabling the analysis of value chains. (3) Finally, a range of correspondence tables are available that use the NCS as an intermediary to, for example, connect trade data to the industry structure of domestic employment and production data.

There have been four iterations of the pltc:

- **Version 1:** Development of basic product classifications
- **Version 2:** Addition of partial Sector and Sub-sector classifications
- **Version 3:** Addition of Product-cluster level classifications, closing of gaps
- **Version 4:** Revision to pre-existing categories, and the addition of NVC classifications

The current stable version of pltc is **Revision 3**. The currently in-development version is **Revision 4**.

pltc implements its classification against six-digit Harmonised System codes, and thereafter makes available ten core elements, five in the Narrative Classification System (NCS) and five in the Narrative Value Chain (NVC) system.

## Narrative Classification System (NCS)

The five levels of the Narrative Classification System (NCS) are:

- **NCS1:** Sector
- **NCS2:** Sub-sector
- **NCS3:** Product group
- **NCS4:** Product
- **NCS5:** Original HS-code description

Given the complexity of trade data, there is a notable simplification that happens in converting data to the NCS, with some products overlapping across sectors and product groups. While the classifications aim to have a high degree of reliability, the pltc prioritises understandability over technical precision. As a result, the NCS places products into categories based on a consideration of how they would typically be viewed by a reasonably informed observer or policy practitioner. 

This results in some differences with other classifications systems. For example, refined sugar is often regarded as a manufactured product, but is considered an agricultural product in some versions of the pltc. This is because a typically informed observer would generally consider sugar to be an agricultural product, even if technically a manufacturing process is involved in its production. Similarly, iron ore is considered a mined good, even if there is substantial cleaning and processing of ore prior to its export, because most observers would think of it as belonging to the mining sector.

NCS classifications connect to a range of data in the PolicyLab database, with this connection usually taking place at NCS2 level. This means that, for example, the sub-sector classifications used in the employment, production and capacity utilisation data in the pldb will exactly match the sub-sector (NCS2) classification in data that makes use of pltc. Correspondence/concordance tables for these connections will be added at a later date.

## Narrative Value Chain (NVC)

The five levels of the narrative Value Chain (NVC) system are:

- **NVC1:** Value-chain product
- **NVC2:** Product origin
- **NVC3:** Industry use
- **NVC4:** Household use
- **NVC5:** Input product

In order to use the NVC system, you would typically first merge your existing trade data, which should be arrange at HS6 level, with revision 4 of the NCS. This would add NVC1 to your data, which gives you product a unique name in the value chain; and would add the additional classifications of NVC 2-4, which provide some detail on the role that product plays in value chains. For each individual product, you could then identify its inputs by referencing the NVC file, which contains a list of inputs (NVC5) for every individual product (NVC1).

Details on the classifications and linkages, and limitations in the NVC systems, are described below.

### Value chain classifications

*Product origin* classifies products by their positioning in the value chain, and is comprised of four categories: Raw material, Intermediate input, Final product and Other. 

Raw material refers to a product that is not comprised of components found elsewhere in the classification system, but may have as an input certain machinery or capital goods (like mining or agricultural equipment) included in the classification. Intermediate inputs are products that are comprised of inputs found elsewhere in the classification, but are themselves primarily used as an input into the production of another product. Final product refers to products that are comprised of inputs found elsewhere in the classification, but are not typically used as a component in further production. Other generally refers to waste, energy, art and personal effects. Notably, energy is not explicitly linked to most value chains, given its ubiquity across production networks.

*Industry use* classifies products by the way in which they are used by companies, and is comprised of six categories: Industrial input, Service equipment, Construction material, Extractive equipment, Capital equipment, Fuel & energy, and None. 

Industrial input refers to a product that is mainly used as a component in the production of a more complex good. Service equipment refers to a product that utilised in the delivery of a service, rather than in the production of another good (examples could include vending machines, airplanes or computer servers). Construction materials refer to products used in construction, such as cement or bricks. Capital equipment refers to machinery used in the production of final products and intermediate inputs. Extractive equipment refers to machinery used in the production of raw materials. Fuel & energy refer to electricity, petrol and gas; and None means that the product is not typically purchased by companies.

*Household use* classifies products by the way in which they are used by households, and is comprised of three categories: Primary, Secondary and None. Primary means that households are the most important purchasers of the product; while secondary means that, while households may purchase a product, they are not the most important user of said product. An example of the latter category could be medical masks, which are purchased by households but which are primarily used in the medical industry. None means that households are not notable purchases of the product. 

### Value chain linkages

While these classifications offer some supplementary information, the core of the NVC system are the linkages between products. Linkages are developed by identifying each product’s primary inputs. This has required individual research on each product category, and given the scale of the classification, the depth of this exercise was obviously limited. As a result, linkages only connect products to their core components, and exclude important but secondary inputs. 

To illustrate this, take the example of stainless steel. The NVC system identifies six core inputs for primary stainless steel – including ferrochrome, iron ore, coke, foundry and metalworking machinery, and basic equipment like furnaces. Each individual input has a detailed set of its own inputs, with ferrochrome drawing on chrome ore and a range of other products; and with chrome ore drawing on the likes of mining equipment – all of which allows stainless steel to be traced back all the way along its supply chain.

At the same time, primary stainless steel is an input into a range of more complex stainless-steel products, including structural fixtures and shaped pieces. These are themselves an input into a very wide range of industrial products, ultimately meaning that stainless steel directly connects into 127 products within the NVC classification. Each of which, in turn, connect into many more complex products.

![An example of NVC linkages in stainless steel](/example.png)

However, excluded from this picture are the wooden pallets that hold finished products, the trucks that transport those products, and some of the chemicals used to finish products. These non-core products are a part of the stainless steel value chain, but are beyond the level of detail available in the NVC.

A further limitation is that the categorisation system used to classify products in the NVC inherently requires some simplification. For example, while each individual polymer is included in the classification, most of these typically connect to a more generic category of "Plastic panels and sheets". This means that an industry that specifically uses one type of plastic is nevertheless linked to this broader bucket of different types of polymers. This analysis is necessary to avoid the exponential complexity of connecting individual HS codes, but does not involve a major loss of analytical potential, given that the grouping of similar products aims to demonstrate capability in a product space, rather than ability in a precise product line. 

In addition to these broad limitations, a number of products have warning messages within their inputs. These come in 4 forms:
- **Inputs not yet classified**: The most common warning, this simply means that there are known inputs which are not currently included. This message is effectively a placeholder to indicate where further work is needed.
- **Complex electronics not yet added**: Used for very complex electronics devices, this message typically indicates that the precise inputs used by the product may not be easily identifiable in either the HS codes or the NVC system. 
- **Machinery components not yet added**: Similarly, in the case of certain machinery components, both the complexity of the product, and the relatively more limited role played by these products in the classification (since they feed into equipment and not other products) means they have been excluded for now, primarily in order to meet deadline commitments. 
- **Inputs excluded from classification**: Refers to inputs explicitly not included, because they are used to produce dangerous products. Most types of weapons and explosives fall into this category.

A range of sectoral weaknesses are also notable. For example, in the case of chemicals, many chemical inputs are either at a level of detail that isn’t fully captured by the HS codes or NVC classification, and/or are able to be produced by such a diversity of processes and reactions that it proved difficult to assign a narrow set of inputs. 

Finally, it should be noted that many value chains are infinitely cyclical. That is, the product being examined is often an input somewhere down its own value chain. Stainless steel, for example, relies on chrome that is extracted by mining equipment, which itself often uses stainless steel in its construction. For this reason, analysis generally requires the use of 'step-limits' which determine how many stages down/up the value chain the analysis runs. In most cases, steps should be limited to two-forward and two-backward. 