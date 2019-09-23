# LTO Network Public Node Information Standard
**JSON Standard for Generator Information on the LTO public chain**

This is a proposed standard for LTO Network Generators to reference in a LTO_GENERATOR_INFO environment variable.

- generator_adress: LTO Public adress
- node: [Object]
  - node_name: Node/organization name
  - node_description
  - website: LTO Node website
  - ownership_disclosure: Full link to where it is,
  - email: Contact email
  - location: Node location
    - name: Node location in human readable format [City, State]
    - country: Country code [XX] in accordance to [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
  - node_type: Type of service `public/anchor/full`
  - api_endpoint: LTO REST API `http://host:port`
  - branding: {Object} - Logo images
      - logo_256: Entire url to image 256x256px
      - logo_1024: Entire url to image 1024x1024px
      - logo_svg: Entire url to image svg
    },
  - social: {Object} - NOT THE ENTIRE URL, only usernames on social networks,
    - lto_community: Username  
    - twitter: Username
    - youtube: Channel address
    - facebook: Page/group address
    - github: Username
    - reddit: Username
    - keybase: Username
    - telegram: Username
    - wechat: Username

### How to use it if you are running an LTO Public Node 
Create a file named generator.json and reference it in the LTO_GENERATOR_INFO environment variable. Example: LTO_GENERATOR_INFO=https://www.yourwebsite.com/generator.json