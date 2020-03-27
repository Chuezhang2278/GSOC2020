# Title 
Repository size reduction

## Abstract 
Matplotlib has an issue where its repository size increases too much everytime a new baseline image is added or modified. Rather than storing it in the repository, why not just store it inside the sdist/wheel so that baseline images are generated whenever sdist generates a new release of mpl.

## Technical Details 
- Transfer all baseline images from repo to sdist/wheel
- Unit tests are strictly done with the latest release of mpl
- To cache using CI cache so that CI time doesn't double
- commit messages require special string when modifications or additional baseline images are made
- Hopefully fix the issue with FreeStyle increasing baseline image sizes everytime there is an update 

## Schedules of Deliverables

### June 1st - June 15th
- Undertanding sdists/wheels, Caching and how Baseline images are used for unit tests.

### June 16th - July 7th
- To conduct tests on sdists and transfering baseline images over to sdist and have them be generated on new release

### June 7th - July 14th 
- Setup CI cache for when test suite is run on new environment 

### July 15th - July 29th
- By now, sdists should now generate baseline images and should not be within the repository
- caching should only be performed once for when the test suite is run for the first time

### July 30th - August 12th
- Hopefully fix the FreeStyle issue where everytime FreeStyle updates, baseline image size increases
- Bug fixes 

### August 13th - August 24th
- More bug fixes
- Changing up the documentation on test suites

## Development Experience
- I have no experience in developing or contributing to open source projects

## Other Experiences
- I have experience working as project leads for proejcts surrounding software development 

# Why this project
- I have found myself working closely with people that revolve around matplotlib and i would like to get into matplotlib myself. I was referred to this GSOC to gain experience and im looking forward to learning the backend of matplotlib in hopes of becoming a contributer for mpl
