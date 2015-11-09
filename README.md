# guidelines

## Commit Messages
A commit message should be comprehensible at a glance. This can be achieved by composing
the message in the following order. 

**NOTE:** The first two parts **must** be in the commit message

#### 1. Emoji
The emoji indicates the general purpose of the commit. 
Use all that apply and seperate them with a space.

|      Emoji       | Code               | Purpose                       |
|:----------------:|:-------------------|:------------------------------|
|   :sunflower:    | `:sunflower:`      | New feature                   |
|      :bear:      | `:bear:`           | Documentation changes         |
|      :bug:       | `:bug:`            | Bug fixes                     |
|      :ram:       | `:ram:`            | Cleanup or refactoring        |
|    :elephant:    | `:elephant:`       | Adding tests                  |
|   :racehorse:    | `:racehorse:`      | Performance improvements      |
| :cherry_blossom: | `:cherry_blossom:` | Style changes (aesthetically) |
|     :monkey:     | `:monkey:`         | Chore/Everything else?        |



#### 2. Context
The context should indicate the specific module that is being affected in the commit. It should be wrapped in
square brackets in the commit message and there **should only ever be one**. An example context could be,
`[Poll]`. Sometimes the context can be a little ambiguous, so use your best judgement.


#### 3. Detail (Optional)
Specifying the first two parts should be sufficient for anyone to understand what
your changes affect. One may optionally add detail to the commit message.

Details **must**:
- Be in present tense
- Begin with an imperative i.e `Fix`, not `Fixes` or `Fixed`
- Have the first letter capitalized


#### Examples

```
:bear: [Poll]
```

```
:bug: :bear: [Poll] Fix rendering and update documentation
```

```
:cherry_blossom: [Poll] Increase margin size
```