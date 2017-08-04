**WARN: this repo is under development.**

## Draft Utils

draft-js is awesome, and it provide some method to use.


### What's problem?

if we want to get text in ContentBlock, we need to do something like

```javascript
editorState
    .getCurrentContent()
    .getBlockForKey(selection.getStartKey())
    .getText();
```

so this utils provide convienient way to use draftJS.

For example,

```javascript
  getContentBlockText(editorState) // do the some thing above.
```

All you need to do is passing editorState, which is more reasonable.
