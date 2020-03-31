# Title 
Repository size reduction

## Abstract 
Matplotlib has an issue where its repository size increases too much everytime a new baseline image is added or modified. Rather than storing it in the repository, why not just store it inside the sdist/wheel so that baseline images are generated whenever sdist generates a new release of mpl.

## Technical Details 
- Transfer all baseline images from repo to sdist/wheel
- Unit tests are strictly done with the latest release of mpl
- To cache using CI cache so that CI time doesn't double
- Commit messages require special string when modifications or additional baseline images are made
- Fix the issue with FreeType increasing baseline image sizes everytime there is an update ( due to rasterization )

## Schedules of Deliverables

### June 1st - June 8th
- To understand 
  - Caching - Specifically on caching memory into specific areas 
  - Sdists - Modifying source distributions code and how we generate MPL
  - Baseline imaging and how we use FreeType to generate these images
  
### June 9th - June 22nd
-  Will start by modifying our Sdist so that on every new release, we will generate the latest version of our baseline imaging. (This means that everyone will have to be updated with the latest version of MPL in order to use the test suite)

### June 23rd - June 30th
- By now, sdists should now generate baseline images and should not be within the repository
- I will now start using gitlab CI for caching 

### July 1st - July 14th
- To deal with FreeType increasing the size of baseline images perhaps a solution would be delete all baseline images and have them regenerated as we use a new version of freetype (this may be highly unefficient so maintaining an older version of freetype may be better)

### July 15th - July 22nd 
- We will publish mpl-test-data as a wheel seperately
- If a baseline image needs to be changed, set up a special commit message that is required to modify the images

### July 23rd - August 24th
- Bug fixing
- Update documentation regarding using our test suites

## Development Experience
- I have no experience in development or experience in contributing to open source projects

## Other Experiences
- I have developed software for class proejects while acting as the project lead. A notable project developed was my stock market prediction software where matplotlib was actively used to display highs and lows of stocks. Matplotlib has also been used for displaying contents of trained data sets for my Machine Learning Course. 

# Why this project
- I was a student of Hannah Aizenman in the past and currently work with her in the GLASSLAB at The City College of New York. Due to this connection, i was recommended to try out this project so that i could build more experience working with matplotlib and open source projects in general.
