GitAsana
=========

Simple integration of git with [Asana](http://asana.com).

Usage
-----

To use GitAsana you have to set `ASANA_KEY` variable with value of your [API key](http://app.asana.com/-/account_api). You also have to create config file `.git-asana-config` in the main directory of your repository: 

```
{
    "project": "<Project name>",
    "workspace": "<Workspace name>"
}
```

To add comments automatically after every commit copy `hooks/post-commit` to `.git/hooks/post-commit` in the main directory of your repository.

Now, to use it call `git-asana` (without arguments). It will display list of your tasks in workspace and project. If you want to create a new task use `git-asana create "<task name>" <task description>`. In both cases you'll get a task id which you have to set with `. git-asana-set <task id>` (notice the dot in front of the command - it's very important).

Now just commit into git and it'll add comments to selected task on Asana automatically.

TODO
----

* Make comments format easier to change.

