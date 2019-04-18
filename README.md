# AzureAiHackerearth2019
*This is my MVP for the Azure AI challenge on Hacker Earth. Ecommerce on what's app using Azure AI infrastrcture.*

The basic Idea is to build an automated system so you could sell stuff directly on what's app. It would be like a shop where you buy whatever you need from the brand or person you like. In this hackathon I would like to at least make a prototype/MVP that could accomplish phase 2.

**Objectives / Phases** 
1. **Text recognition so we know what the customer want to buy.**
2. **Adding better understanding of what the user want, so we know if there's customisation to the order.**
3. Finding items to buy from a picture or a random descriptions. 
4. Accept other languages than english 
5. Adding speech recognition so people don't need to write what they want. 
6. Maybe start accepting payement by crypto

# Back-end
1. Server that scrappe the message from the main what's app account.
2. Define new messages as (Request, Follow up, Closing or mistake)
3. Preprocess the message with basic manipulation to know if we can reply without Azure first.
4. Format to a JSON request to be send to Azure.
5. Azure Magic.
6. Look up on the database the item wanted
7. Craft a reply message
8  Send to customer and wait for Follow-up or closing message.
9. Define if the *Flow* was succesfull or not and save it to the training database.

# Azure AI
We connect the extracted text with this API from Azure AI and our own DB. This will give us a good starting point to better understand the request of our client.
* Key phrase extraction using the text Analytics REST Api [Doc](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-keyword-extraction)
* Identify entity in the text [Doc](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-entity-linking)



# Front-end

# Admin panel


# Software used in this MVP
**This MVP is not meant to be used as a commercial product, but only as a crude prototype**
* Admin panel [Django Suit](https://djangosuit.com/pricing/)
* Whatsapp [Analyzer](https://github.com/PetengDedet/WhatsApp-Analyzer)
* Whatsapp [Assistant bot](https://github.com/jctissier/whatsapp-assistant-bot)
