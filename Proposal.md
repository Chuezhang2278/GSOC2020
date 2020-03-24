# Title 

## Abstract 
Matplotlib has an issue where its repository size increases too much everytime a new baseline image is added or modified. Rather than storing it in the repository, why not just store it inside the sdist/wheel so that baseline images are generated whenever sdist generates a new release of mpl.

## Technical Details 
- Transfer all baseline images from repo to sdist/wheel
- Unit tests are strictly done with the latest release of mpl
- Can rely on CI cache for CI 
- commit messages require special string when modifications or additional baseline images are made
- Hopefully fix the issue with FreeStyle increasing baseline image sizes everytime there is an update 

## Schedules of Deliverables


