# guidelines

**WORK IN PROGRESS**
**THIS WILL BE SPLIT INTO DIFFERENT FOLDERS WHEN THERE'S ENOUGH CONTENT**

## Branching
Branches should use the following structure and naming scheme:
```
master
|
+-- qa
|   |
|   +-- develop
|   |   |
|   |   +-->project/{project-name}
|   |   |   |
|   |   |   +-->{project-name}/{task-name}
|   |   |   |   |
|   |   |   |   * // commits for task
|   |   |   |   |
|   |   |   |<--+ // merge request for peer review (small)
|   |   |   |
|   |   |   ...
|   |   |   |
|   |   |<--+ // merge request for team review (big)
|   |   |
|   |   ...
|   |   |
|   |<--+ // developer snapshot release for qa testing
|   |   |
|   |   ...
|   |
|<--+ // release passed testing. good for production.
|   |
|   ...
|
...
```
Project and task branches should be created in order to help track work, although this process could be replaced with an external application (eg. JIRA) in the future.

## Commit Messages
A commit message should be comprehensible at a glance. This can be achieved by composing
the message in the following order.

**NOTE:** The first two parts **must** be in the commit message

#### 1. Emoji
The emoji indicates the general purpose of the commit.
Use all that apply and separate them with a space.

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
`[Poll]`. Sometimes the context can be a little ambiguous, so use your best judgment.


#### 3. Detail (Optional)
Specifying the first two parts should be sufficient for anyone to understand what
your changes affect. One may optionally add details to the commit message.

Details **must**:
- Use first-person singular present tense i.e `Fix`, not `Fixes` or `Fixed`
- Begin with an imperative i.e. `Add details to instructions`, not `More details in instructions`
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

## Documentation

#### Function Documentation
Use the [Docblockr](https://atom.io/packages/docblockr) plugin to
make documentation easier.

```JavaScript
/**
 * Start with a capital letter and end with a period.
 * Put a space in between the function description and the params
 * if it spans 2 or more lines.
 *
 * @param  {Object} options           The lines below indicate what options contain
 *         {String} [options.thing]   Square brackets mean optional
 *         {Number} [options.blah=2]  Indicates a default argument
 * @param  {Boolean} isSwag           
 * @return {[type]}         [description]
 */
function myFunction(options, isSwag) {...}
```
