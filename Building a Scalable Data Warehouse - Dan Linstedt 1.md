---
Work Week: 25ww07
Date: Fri, Feb 14th  2025.
tags:
  - learning-development
  - Dan-Linstedt
  - data-vault
  - concepts
---
> [!question] #Questions
> - How do you automate the creation of links?
> - I see Data Vault is highly focused on the `loadDate` attribute and that makes me think that it is a modeling technique focused on the migration to cloud. Will the data vault model persist in time after the migration? if the migration to cloud is successful, Will the data be modeled using a different technique? 
> 

The model is based on three basic entity types, which are derived from the natural model:
- **[[Hub definition]]**. Separates the business keys from the rest of the model. Also, it stores metadata.
- **[[Link definition]]**. Stores relationships between business keys (and/or hubs). Links often represent transactions. Therefore, it often provides the basis for creating the facts of the dimensional model.
- **[[Satellite definition]]**. Store the context (the attributes of a business key or relationship).

![[Screenshot 2025-02-14 at 3.20.10 PM.png]]
Due to its design, querying a final Data Vault model requires many more joins than in a traditional data warehouse.