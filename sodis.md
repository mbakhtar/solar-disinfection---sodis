# SODIS

## @showhint
Create a Variable ``||Variables:reading||`` and
nest it under the ``||basic:forever||`` loop
```blocks
basic.forever(function () {
reading = 0    
})
```
## @showhint
Go to the ``||led:led drawer||`` drag and nest the block ``||led:plot bar graph of 0 up to 0||``
under the ``||Variables:set reading to 0||`` block
```blocks
basic.forever(function () {
    reading = 0
    led.plotBarGraph(
    0,
    0
    )
})
```
## @showhint
Next go to the ``||Variables:Variables||`` drawer and drag the ``||Variables:reading||``
insert it place of 0 of the ``||led:plot bar graph of 0||`` . Also change the other 0 
to 255
```blocks
basic.forever(function () {
    reading = 0
    led.plotBarGraph(
    reading,
    255
    )
})
```
## @showhint
In this step we need to use the ``||input:light level||`` block from the ``||input:input||`` drawer
Drag the ``||input:light level||`` block and replace the 0 in ``||Variables:set reading to 0||`` with it
```blocks
basic.forever(function () {
    reading = input.lightLevel()
    led.plotBarGraph(
    reading,
    255
    )
})
```
## @showhint
This is the final code
```blocks
let reading = 0
basic.forever(function () {
    reading = input.lightLevel()
    led.plotBarGraph(
    reading,
    255
    )
})
```