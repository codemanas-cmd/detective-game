# detective-game
An interactive python based game

### Setup
`pip install -r requirements.txt`

### Play a story
run `python detective.py`

Starts an interactive session for a story. Play the detective searching and reading story entries. Prompts and menus are navigated with arrow keys + Return key⏎

### Write a story
Create a story of your own by writing the segmented entries a detective player can search through. A story is basically just a set of timestamped entries that are strategically linked by search terms. A story can also associated with some configuration like the max number of entries to make returnable on searches.

#### Story data
Stories are defined by yaml files. see example `stories/story_2.yaml`

* `intro_text`: string. if set, text to display at start of session (optional)
* `intro_stats`: bool. if set, display some stats about the story at start of session (optional)
* `match_count_limit`: int. if set, maximum number of entries that can be returned by a search (optional)
* `initial_search`: string. if set, start the session with an already executed search for this term (optional)
* `entries`: sequence of mappings w/ keys. this is the meat of the data
    * `id`: string. if not set, id will be set to entry's position index in list of entries (optional)
    * `date`: date|datetime. date for the entry. matches will be returned in order of date ascending
    * `text`: string. the content of the entry to be displayed