
# [View CHANGELOG](CHANGELOG.md)
## [View list of CHANGELOG entries](notes)
## How to Add Release Notes to the Change Log

- For each release, the notes should be put in their own markdown file and saved to the `notes` directory.
- The filename should be prefixed with the date in YYY-MM-DD format and include the release version number after.
  - This is important as it will define the order of the notes in the full CHANGELOG.md file.
  - example: `2015-05-01_R11-1.md`
  
- We should strive to keep the notes in [this](1900-01-01_R0-0.md) format (which is really just the format provided by the brilliant http://keepachangelog.com/).

- A special file `_header.md` is also in the `notes` directory. This will be the text that shows up at the top of `CHANGELOG.md`.

## Rebuilding CHANGELOG.md

The CHANGELOG.md file in this repository is automatically generated by a script and should never be edited directly.

To rebuild CHANGELOG.md, first, make sure you have [Node.js](https://nodejs.org) installed.

Then run these commands from the terminal:
```bash

# checkout the project
git clone https://github.com/BestBuyAPIs/api-release-notes.git

# install npm packages
npm install

# run the script
npm start

# once completed, commit the new changelog:
git commit -am "updated CHANGELOG"

# Finally, push the commit to github
git push origin master
```
