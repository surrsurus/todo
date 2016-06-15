# todo
*todo* is a simple tasklist manager in python with support for an openbox pipemenu to edit and view your tasklist at anytime. It is rather feature-sparse, only providing a way to simply track and manage items, without priorities or deadlines (which will perhaps be implemented in future versions)

## Openbox
Put an entry in ~/.config/openbox/menu.xml, making sure to adjust for the proper path to this script:
`<menu id="pipe-tasklist" label="Task List" execute="python /path/to/todo.py*8 menu" />`

Then put the following wherever you'd like it to be displayed in your menu:
`<menu id="pipe-tasklist" />`

## Conky
You can easily add this script to your conky configurations with the following line:
`${head /path/to/list 30 20}`

This will append all of the items in the todo file directly to your conky

## Usage
Here is a list of arguments that can be passed to the script
- No arguments: Run with no arguments to see your task list
- `new`: Be prompted to add a new task
- `del`: Delete a task based on it's position in the tasklist array
- `done`: Complete a task based on it's relative position (array location + 1). You can see which number a task is assigned by running `todo.py` with no arguments
- `menu`: Print the openbox pipemenu xml
- `add`: Add all arguments after add as a new task (ex: `todo add finish project` will add 'finish project' to the list)
- `test`: See what openbox commands are set. Useful for debugging

