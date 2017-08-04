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

### API

#### getSelectedEntity(editorState)

get selected entity instance (not entity key!)
 @param  {EditorState} editorState
 @return {Entity}

### createEntity(type, mutable, data)

return a function(editorState) and create an entity.

### setContentState(contentState, editorState)

set contentState in provided editorState. useful when you use some method only return contentState.


### applyEntity(contentState, selectionState, entityKey)

return a function(editorState). apply an entity and set ContentState to provided EditorState.

### setBlockType(contentState, selectionState, blockType)

return a function(editorState). apply an blockType and set ContentState to provided EditorState.

### getCurrentBlockType(editorState)

return currentBlock type.

### getSelectedText(editorState)

get selected text with editorState.


### toHTML(editorState)

convert editorState into HTML.

### getPlainText(editorState)

get plain text with editorState.


### LICENSE

MIT
