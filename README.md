# Tools Presentation Demo Repository

This is a repository for the live demo in Tools Presentation.

You do **NOT** need to install any `npm` dependencies. There are no dependencies.

## How to Showcase the Merge Conflict

1. (Optional) Make a new branch based on `start-here` branch and switch to that branch. This is just to make it easier to restore to the original state. If you choose not to make a new branch, then just switch to `start-here` branch.
1. There are 2 branches, `merge-a` and `merge-b`. For simplicity, let's merge `merge-a` branch first to your current branch. The merge is applied without any problems.
1. GitKraken might already show a warning icon somewhere near `merge-b` branch because of a predicted merge conflict.
1. Try merging `merge-b` branch to your current branch. You will be greeted with a special kind of editor that shows you the comparison of what was in the current branch and what are the incoming changes that cause the conflict.
1. Maybe take a note of a button that will abort the merge. You can abort the merge and safely return to the previous state (right after you merged `merge-a` branch).
1. At this state, maybe try to see what the actual content of the file looks like. If you see some weird lines added to the file like the code block below, that's what I'm talking about. If you don't see any changes, then GitKraken is handling everything in its memory without writing any changes to the actual file system.
1. In the merge conflict editor, you have a lot of options. You can choose to keep what you had or to overwrite with the incoming change from `merge-b` branch. You should be also able to write a totally new thing since GitKraken is a very developed and polished program.
1. After applying the changes you want, mark the file as resolved. Since all files with merge conflicts are now marked as resolved, the GUI might or might not automatically proceed with the rest of the process to complete the merge.
1. Complete the merge.

### Some Random Thoughts

- You can either have a text editor like vscode open to show the content of the file, or you can also run `npm start` to show that the code is changed.

### Raw File with Merge Conflicts

```js
<<<<<<< HEAD
const message = "Hello! I'm from merge A.";
=======
const message = "Hello! I'm from merge B!";
>>>>>>> merge-b

console.log(message);
```
