# Field descriptions

## projects.json

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
- `mainURL`
  - This is the main URL of your project
  - A big button on the project page will open this URL
- `img`
  - This is the file name of the SVG of your project
  - Read the [logo requirements](#logo-requirements) for more information
- `inTheMarketYouTubeVideoId`
  - Here you can add the YouTube video ID of the interview with the InTheMarket podcast
  - The video will be embedded on the project page
  - You can contact us via our [Telegram group](https://t.me/DMC_Universe), if you'd like to be interviewed
- `links`
  - This is an array of links to your project
  - Each link is an object, which is described in the [link field](#link-field) section
- `team`
  - This is an array of team members
  - Each team member is an object with three properties
    - `name`
      - The name of the team member
      - E.g. first name, nickname, etc.
      - Max 20 characters
    - `role`
      - The role of the team member
      - E.g. developer, community manager, etc.
      - Max 20 characters
    - `img`
      - This is the file name of the jpg of the team member
      - The jpg needs to be 1:1 ratio
      - It needs to be placed in the `/teams` folder
    - `links`
      - This is an array of links to your project
      - Each link is an object, which is described in the [link field](#link-field) section

### Link object

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
    - If none of the above values match, use "Website"
    - If you want to add a new type, please contact us via our [Telegram group](https://t.me/DMC_Universe)
  - `label`
    - Only required if the `type` is "Website"
    - This is the text that will be displayed for the link
    - Max 20 characters
