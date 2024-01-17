# PolicyLab Trade Classifications (pltc)

## Overview

pltc are a set of useful classification systems for trade data, aimed to enable understanding and unique technical analysis. While the classifications aim to have a high degree of reliability, the pltc prioritise understandability over technical precision. This means, for example, translating complex customs code desciprtions into more undesrstandable product clusters.

There are three core parts to pltc. (1) The Narrative Classification System, or NCS, is a simplified classification system for translating HS6 level products into more manageable groups of Sectors, Sub-sectors, Product types and Products. (2) The Narrative Valus Chain, or NVC, classification provides a mapping of products into inputs and end uses, with the aim of enabling the targetting of value chains that countries could potentially move up or consolidate. (3) Finally, range of correspondance tables are available that use the NCS as an intermediary to, for example, connect trade data to the industry structure of domestic employment and production data.

- **Version 1:** Development of basic sector and sub-sector classifications
- **Version 2:** Addition of Product-level classifications
- **Version 3:** Addition of Product-cluster level classifications
- **Version 4:** Revision to pre-existing categories, and the addition of NVC classifications

pltc implements its classifciation against six-digit Harmonised System codes, and thereafter makes available nine core elements, five in the Narrative Classification System (NCS) and five in the Narrative Value Chain (NVC) system.

## Narrative Classification System (NCS)

The five levels of the Narrative Classification System (NCS) are:

- **NCS1:** Sector
- **NCS2:** Sub-sector
- **NCS3:** Product group
- **NCS4:** Product
- **NCS5:** Original HS-code description

Describe

## Narrative Value Chain (NVC)

The five levels of the narrative Value Chain (NVC) system are:

- **NVC1:** Value-chain product
- **NVC2:** Product origin
- **NVC3:** Industry use
- **NVC4:** Household use
- **NVC5:** Input product

Value-chain product and Input product are identical identifiers of product groups, and are similar to NCS4 level classifications, albeit at a more granular level of detail. 

Product origin classified products by their positioning in the value chain, and is comprised of four categories: Raw material, Intermediate input, Final product and Other. Raw material refers to a product that is not comprised of components found elsewhere in the classification system, but may have as an input certain machinery or capital goods (like mining or agricultural equipment). Intermediate inputs are products that are comprised of inputs found elsewhere in the classification, but are themselves primarily used as an input into the production of another product. Final product refers to products that are comprised of inputs found elsewhere in the classification, but are not typically used as a component in further production. Other generally refers to waste, energy, art and personal effects. 

Industry use classifies products by the way in which they are used by companies, and is comprised of sixth categories: Industrial input, Service equipment, Construction material, Extractive equipment, Capital equipment, Fuel & energy, and None. 

Industrial input refers to a product that is mainly used as a component in the production of a more complex good. Service equipment refers to a product that utilised in the delivery of a service, rather than in the production of another good (examples could include vending machines, airplanes or desktop computers). Construction materials refer to products used in construction, such as cement or bricks. Capital equipment refers to machinery used in the production of final products and intermediate inputs. Extractive equipment refers to machinery used in the production of raw materials. Fuel & energy refer to electricity, petrol and gas; and None means that the product is typically purchased by consumers, and not by companies.

Household use classified products by the way in which they are used by households, and is comprised of three categories: Primary, Secondary and None. Primary means that households are the most important purchasers of the product; while secondary means that, while households may purchase a product, they are not the most important user of said product. An example of the latter category could be medical gloves, which are purchased by households but which are primarily used in the medical industry. None means that households are not notable purchases of the product. 

## Value chain analysis

Words
