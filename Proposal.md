# Title 
Repository size reduction

## Abstract 
Matplotlib has an issue where its repository size increases too much everytime a new baseline image is added or modified. Rather than storing it in the repository, why not just store it inside the sdist/wheel so that baseline images are generated whenever sdist generates a new release of mpl.

## Technical Details 
- Transfer all baseline images from repo to sdist/wheel
- Unit tests are strictly done with the latest release of mpl
- To cache using CI cache so that CI time doesn't double
- commit messages require special string when modifications or additional baseline images are made
- Hopefully fix the issue with FreeType increasing baseline image sizes everytime there is an update 

## Schedules of Deliverables

### June 1st - June 8th
- Undertanding sdists/wheels and how Baseline images are used for unit tests.

### June 9th - 15th 
- Understand how Caching works and where we will be caching into

### June 16th - July 7th
- To conduct tests on
  - Cache
  - Sdists 
  - Baseline imaging 
  
### June 7th - July 14th 
- Setup CI cache for when test suite is run on new environment 

### July 15th - July 22nd
- By now, sdists should now generate baseline images and should not be within the repository
- caching should only be performed once for when the test suite is run for the first time

### July 23rd - June 30th
- Understanding FreeType image rendering

### August 1st - August 8th
- Hopefully by now, a fix for FreeType will be implemented 

### August 9th - August 24th
- More bug fixes
- Changing up the documentation on test suites

## Development Experience
- I have no experience in development or experience in contributing to open source projects

## Other Experiences
- I have developed software for class proejects while acting as the project lead. A notable project developed was my stock market prediction software where matplotlib was actively used to display highs and lows of stocks. Matplotlib has also been used for displaying contents of trained data sets for my Machine Learning Course. 

# Why this project
- I was a student of Hannah Aizenman in the past and currently work with her in the GLASSLAB at The City College of New York. Due to this connection, i was recommended to try out this project so that i could build more experience working with matplotlib and open source projects in general.
