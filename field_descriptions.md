# Field descriptions

## config.json

```json
{
  "featuredProjects": []
}
```

- `featuredProjects`
  - This is an array of project IDs
  - These projects will be featured on the home page
  - The order of the projects in the array will be the order of the projects on the home page
  - Only one project is visible at a time and the carousel will automatically switch to the next project after a few seconds

## projects.json

```json
{
  "id": "",
  "updatedAt": "",
  "name": "",
  "description": "",
  "longDescription": "",
  "mainURL": "",
  "inTheMarketYouTubeVideoId": "",
  "SpotlightXSpaceURL": "",
  "SpotlightBlogpostURL": "",
  "status": "",
  "customVideo": {
    "title": "",
    "description": "",
    "youTubeVideoId": ""
  },
  "links": [],
  "initiators": [
    {
      "name": "",
      "role": "",
      "img": "",
      "links": []
    }
  ],
  "positions": [
    {
      "title": "",
      "description": "",
      "location": "",
      "type": "",
      "requirements": [""],
      "benefits": [""],
      "applicationLink": ""
    }
  ],
  "projectTokenId": "",
  "tags": [""]
}
```

- `id`
  - This is the ID of your project
  - It must be unique and can only contain lowercase letters, numbers and dashes
  - Max 20 characters
  - This will be used in the URL of your project page and in the file names of your project's files
- `updatedAt`
  - This is the date when the project was last updated
  - Format: `YYYY-MM-DDTHH:mm:ss.SSSZ`
- `name`
  - Project name
  - Max 25 characters
- `description`
  - Project description
  - One sentence that describes your project
  - Max 65 characters
- `longDescription`
  - Project long description
  - A few sentences that describe your project
  - Max 1000 characters
  - You can use `\n\n` to add line breaks
- `mainURL`
  - This is the main URL of your project
  - A big button on the project page will open this URL
- `inTheMarketYouTubeVideoId`
  - Here you can add the YouTube video ID of the interview with the InTheMarket podcast
  - The video will be embedded on the project page
  - You can contact us via our [Telegram group](https://t.me/DMC_Universe), if you'd like to be interviewed
- `SpotlightXSpaceURL`
  - The direct URL to the X Space of your project's spotlight
- `SpotlightBlogpostURL`
  - The direct URL to the blog post of your project's spotlight
- `status`
  - This is the status of the project
  - Possible values are:
    - `NotLaunched`: The project is not launched yet
    - `Testnet`: The project is launched on the testnet
    - `Mainnet`: The project is launched on the mainnet
    - `LiveService`: The project is live but is not a blockchain project
- `customVideo`
  - You can add a custom video to your project
  - `title`
    - The title of the video
    - Max 25 characters
  - `description`
    - A short description of the video
    - Max 100 characters
  - `youTubeVideoId`
    - The YouTube video ID of the video
    - The video will be embedded on the project page
- `links`
  - This is an array of links to your project
  - Each link is an object, which is described in the [link field](#link-field) section
- `initiators`
  - This is an array of initiators
  - Each initiator is an object with three properties
    - `name`
      - The name of the initiator
      - E.g. first name, nickname, etc.
      - Max 20 characters
    - `role`
      - The role of the initiator
      - E.g. developer, community manager, etc.
      - Max 20 characters
    - `img`
      - This is the file name of the jpg of the initiator
      - The jpg needs to be 1:1 ratio
      - It needs to be placed in the `/initiators` folder
      - It should be labeled like `dmcuniverse_peddy.jpg`
    - `links`
      - This is an array of links to your project
      - Each link is an object, which is described in the [link field](#link-field) section
- `positions`
  - This is an array of positions
  - Here you can add open positions for your project
    - `title`
      - The title of the position
      - E.g. developer, community manager, etc.
      - Max 20 characters
    - `description`
      - The description of the position
      - Max 110 characters
    - `location`
      - The location of the position
      - E.g. Remote, Berlin, etc.
      - Max 15 characters
    - `type`
      - The type of the position
      - E.g. Full-time, Part-time, etc.
      - Max 15 characters
    - `requirements`
      - This is an array of requirements for the position
      - Each requirement is a string
      - Max 40 characters each
    - `benefits`
      - This is an array of benefits for the position
      - Each benefit is a string
      - Max 40 characters each
    - `applicationLink`
      - Link to a website or `mailto:`
- `projectTokenId`
  - This is the ID of the project token
  - The token must exist in the `/data/tokens.json` file
- `tags`
  - Array of tags/categories this project belongs to
  - See `/tags.json` for the list of available tags
  - Max 3 tags

### Link object

```json
{
  "url": "",
  "type": "",
  "label": "" // optional
}
```

- This is an array of links to your project
- Each link is an object with three properties
  - `url`
    - The URL of the link
  - `type`
    - The type of the link
    - This can be one of the following values
      - "X"
      - "Medium"
      - "YouTube"
      - "Reddit"
      - "Telegram"
      - "Discord"
      - "TikTok"
      - "GitHub"
      - "LinkedIn"
      - "CoinMarketCap"
      - "CoinGecko"
      - "Facebook"
      - "Documentation"
      - "Newsletter"
    - If none of the above values match, use "Website"
    - If you want to add a new type, please contact us via our [Telegram group](https://t.me/DMC_Universe)
  - `label`
    - Optional
    - This will override the default label for the link type
    - Recommended if you have multiple links of the same type like multiple Telegram groups
    - Max 20 characters

### Token object

```json
{
  "id": "",
  "symbol": "",
  "name": "",
  "contract": "",
  "decimals": 18,
  "description": "",
  "totalSupply": 1000000,
  "allocations": [
    {
      "category": "",
      "percentage": 100,
      "amount": 1000000
    }
  ]
}
```

- `id`
  - This is the ID of the token
  - It must be unique and can only contain lowercase letters, numbers and dashes
  - Max 20 characters
- `symbol`
  - Token symbol
  - Max 10 characters
- `name`
  - Token name
  - Max 20 characters
- `contract`
  - Token contract address
  - This is the address of the token contract on the MetaChain blockchain
  - It must be a valid MetaChain address
- `description`
  - Token description
  - One sentence that describes your token
  - Max 500 characters
- `decimals`
  - Token decimals
  - This is the number of decimals of your token
  - E.g. 18
- `totalSupply`
  - Token total supply
  - This is the total supply of your token
  - E.g. 1000000000
- `allocations`
  - This is an array of allocations
  - Each allocation is an object with three properties
    - `category`
      - The category of the allocation
      - E.g. Advisors / Team, Marketing, etc.
      - Max 40 characters
    - `percentage`
      - The percentage of the allocation
      - E.g. 24
    - `amount`
      - The amount of the allocation
      - E.g. 240000000

### Spotlight Space audio file

The mp3 audio file should be placed in the `/data/spaces` folder and must have the same name as the project ID.

For example, if your project ID is `my-project`, the logo should be named `my-project.mp3`
