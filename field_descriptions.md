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
    - The description of the video
    - Max 100 characters
  - `youTubeVideoId`
    - The YouTube video ID of the video
    - The video will be embedded on the project page
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

### Spotlight Space audio file

The mp3 audio file should be placed in the `/data/spaces` folder and must have the same name as the project ID.

For example, if your project ID is `my-project`, the logo should be named `my-project.mp3`
