
# "You've got 5 seconds... and 3 are up." - *Steven Seagall*
##[Check out the demo NOW](https://jforaker.github.io/react-accordion-with-header/demo/)

React accordion component with flexbox header 

![Steven](https://d17oy1vhnax1f7.cloudfront.net/items/2E3v430p1B2z351E3F0a/Screen%20Recording%202016-09-20%20at%2003.10%20PM.gif)

## Usage

Install via NPM:

```
npm install react-accordion-with-header
```

Then:

```javascript
import {
    AccordionWithHeader,
    AccordionNode,
    AccordionHeader,
    AccordionPanel
} from 'react-accordion-with-header';

…

  render() {
    return (
      <AccordionWithHeader>
        {[1, 2, 3, 4].map((item, i) => {
          return (
            <AccordionNode key={i} className="foobar-node">

              <AccordionHeader className="foobar-header"
                               title={null}
                               titleColor="#607D8B"
                               horizontalAlignment="centerSpaceAround"
                               verticalAlignment="center">
                {/* elements below will render in the header, aligned flexbox style */}
                <h5>Some title</h5>
                <div>Something else</div>
                <h5>A third item</h5>
              </AccordionHeader>

              <AccordionPanel>
                <div>
                  <h2>Important information!</h2>
                </div>
              </AccordionPanel>

            </AccordionNode>
          );
        })}
      </AccordionWithHeader>
    );
  }

…

```


## options / PropTypes

#### AccordionNode
| Property | Type | Description | Default |
|:---|:---|:---|:---|
| className | `String` | Custom classname applied to root item div | `accordion-node` |


#### AccordionHeader
| Property | Type | Description | Default |
|:---|:---|:---|:---|
| title | `String` | For simple headers, a title will render an `<h1>` and disallow child elements | `null` |
| titleColor | `String` | some valid CSS color or rgb or hex | `black` |
| horizontalAlignment | `String` | One of: 'centerSpaceBetween', 'centerSpaceAround', 'center', 'left', 'right'. Maps to corresponding flex-box CSS property | `left` |
| verticalAlignment | `String` | One of: 'top', 'center', 'bottom' | `center` |
| className | `String` | Custom classname applied to root div | `accordion-header` |
| style | `Object` | Inline styles applied to root div | `null` |


