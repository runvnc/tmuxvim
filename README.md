#!/bin/bash
## vp (vim in pane)

Runs vim in designated expanded tmux pane (pane 0) to edit the file specified ($1).

This is useful for me because I want to be able to use cd and other commands to navigate 
around a file system, then open vim to edit or maybe inspect a file, 
but still be able to execute commands in the same directory that I was in if I choose.
Or I can leave it open, run a command to test it, and then go back to the top pane to edit
some more.

The idea is I keep a top pane running across tmux that is sort of 
minimized (height 2).

Then as I am changing directories and doing things in other panes and I want to edit a file,
I run `vp filename` and it resizes pane 0, calculates the absoluate path to the file,
opens vim on that file, then when I quit vim it resizes back to height two and switches back to the original
tmux pane.

I apologize in advance if you don't think this is helpful to you or you have a different workflow.
For me it seems convenient at the moment.  
