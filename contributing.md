# Content Guidelines

## About
[Wonderium.dev](https://wonderium.dev) uses content for cards based on JSON files in this repository.\
Each main folder, such as `html`, `css`, or `js`, represents a different learning level on the [platform](https://wonderium.dev). Inside each of these folders, there are separate unit folders containing JSON files that serve as the ultimate source of data for the cards.
```txt
level/unit/data.json
```

## Content Manifest
We adhere to clear principles for content selection to ensure the relevance and practical value of the information provided. To achieve this, we follow three rules:

1. **If not deprecated, then allowed**: We only include technologies, concepts, or tools that are not deprecated.
2. **Relevance of technologies**: We focus on technologies and concepts that have demonstrated long-term value and are expected to remain useful in the near future.
3. **Exclusion of experimental technologies**: We avoid including experimental or unstable technologies in our content.

Just like the platform's content, this manifest is open for contributions and suggestions.

## How to Contribute

1. **Fork this [content repository](https://github.com/wonderium/content) and clone it to your local machine.**

2. **Decide whether you will work on a new card or an existing one, as the process differs:**
   - **Creating a New Card**
     1. Determine the level you will be working on.
     2. Check that no one else has already created a card with the same content in actual commit.
     3. Decide on the title of the card.
     4. Open the appropriate level folder and create a new folder named in kebab-case for your card. This folder name will serve as the ID for the card and will be visible in the URL.
     5. Inside this folder, create a `data.json` file and fill it out with the following format:
        ```json
        {
          "title": "Card Title",
          "description": "Meta description of the card.",
          "categories": [],
          "content": "The content of the card here. Limit to 310 characters. All technical terms should be enclosed in backticks (``), and all property values should be in single quotes ('').",
          "extensions": {}
        }
        ```
     6. For the categories, check if similar cards have been added before and use the same categories if applicable. You can include up to three categories.
     7. Open `config.json` in the chosen level and add the ID to the list of `units` in the relevant topic. If the topic does not exist, propose a new topic following the structure for its creation.
   - **Editing an Existing card**
     1. Locate the card by opening the folder with its ID in the appropriate level.
     2. Open the `data.json` file and make the necessary edits.
     3. If you think that the card is in the wrong topic, open `config.json` in the level you working on and move the card ID to the appropriate topic.

3. **That's it! Create a pull request. After a review, your contribution will appear on the Wonderium.dev website!**
