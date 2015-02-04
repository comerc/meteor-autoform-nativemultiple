# meteor-autoform-nativemultiple
Custom "nativemultiple" input type for AutoForm

```coffee
mySchema = new SimpleSchema
  myField:
    type: String
    optional: true
    autoform:
      type: "nativemultiple"
      min: 0
      max: 180
      step: 20
      nativeMultipleOptions:
        stylesheet: 'slider'
        onCreate: ->
          console.log(this)
        onChange: (first_value, second_value) ->
          console.log('onchange', [first_value, second_value])
        onSlide: (first_value, second_value) ->
          console.log('onslide', [first_value, second_value])

```
