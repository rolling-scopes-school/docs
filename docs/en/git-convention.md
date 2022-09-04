## Commit Requirements
- The names of the commits should be according to the guideline - https://www.conventionalcommits.org/en/v1.0.0-beta.2/
- The commit type MUST BE in lowercase only (`init`, `feat`, `fix`, `refactor`, `docs` etc.)
- Present tense ("add feature" not "added feature") should be used.
- Imperative mood ("move cursor to ..." not "moves cursor to ..." should be used).

### Examples of commit names
- `init:` - used to start the project / task. Example:
```
init: start youtube-task
init: start mentor-dashboard task
```
- `feat:` - this is the implemented new functionality from the technical specifications (added zoom support, added footer, added product card). Example:
```
feat: add basic page layout
feat: implement search box 
feat: implement request to youtube API
feat: implement swipe for horizontal list
feat: add additional navigation button
feat: add banner
feat: add social links
feat: add physical security section
feat: add real social icons
```
- `fix:` - fixed a bug in previously implemented functionality. Example:
```
fix: implement correct loading data from youtube
fix: change layout for video items to fix bugs
fix: relayout header for firefox
fix: adjust social links for mobile
```
- `refactor:`  - did not add new functionality / behavior did not change. Files in other places put, deleted, added. Changed the code formatting (white-space, formatting, missing semi-colons, etc). Improved the algorithm, without changing the functionality. Example:
```
refactor: change structure of the project
refactor: rename vars for better readability
refactor: apply eslint
refactor: apply prettier
```
- `docs:` - used when working with project documentation / readme. Example:
```
docs: update readme with additional information
docs: update description of run() method
``` 

## FAQ
### Is it possible to reverse a commit (pushed) to a repository without reducing the score?
Yes, you can.