# inotify_fun
Runnable notes on how to use inotify

# A simple example for monitoring the current directory for changes:

`inotifywait -m -r --format '%:e %f' .`

Where `-m` aka `--monitor` means keep running instead of quitting after the first event.
And `-r` is `--recursive`.

Taken from the [manpage](https://linux.die.net/man/1/inotifywait): Example 3.

Add a `-e`/`--event` to only listen for actual modifications:

`inotifywait -m -r --format '%:e %f' -e modify .`
