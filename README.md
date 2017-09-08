# React Native Event Calendar
A React Native iOS style calendar implemented using VirtualizedList.
This package is forked of https://github.com/joshyhargreaves/react-native-event-calendar
allow run without expo and improve somethings

## Demo
<a href="https://raw.githubusercontent.com/duyluonglc/react-native-event-calendar/master/demo/demo.mp4"><img src="https://raw.githubusercontent.com/duyluonglc/react-native-event-calendar/master/demo/demo.gif" width="360"></a>

## Current API
Property | Type | Description
------------ | ------------- | -------------
events | PropTypes.array | Array of event
width | PropTypes.number | Container width
format24h | PropTypes.boolean | Use format 24hour or 12hour
formatHeader | PropTypes.string | Header date format
headerStyle | PropTypes.object | Header style
renderEvent | PropTypes.function | Function return a component to render event
eventTapped | PropTypes.function | Function on event press
virtualizedListProps | PropTypes.object | prop pass to virtualizedList

`EventCalendar` can be configured through a `style` prop whereby any of the components in the calendar can be styled. 
```
    {
        container: {
            backgroundColor: 'white'
        }, 
        event: {
            opacity: 0.5
        }
    }
```

## Examples
See Examples dir. 

```js
let { width } = Dimensions.get('window')

const events = [
    { start: '2017-09-07 00:30:00', end: '2017-09-07 01:30:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-07 01:30:00', end: '2017-09-07 02:20:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-07 04:10:00', end: '2017-09-07 04:40:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-07 01:05:00', end: '2017-09-07 01:45:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-07 14:30:00', end: '2017-09-07 16:30:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-08 01:20:00', end: '2017-09-08 02:20:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-08 04:10:00', end: '2017-09-08 04:40:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-08 00:45:00', end: '2017-09-08 01:45:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-08 11:30:00', end: '2017-09-08 12:30:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-09 01:30:00', end: '2017-09-09 02:00:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-09 03:10:00', end: '2017-09-09 03:40:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' },
    { start: '2017-09-09 00:10:00', end: '2017-09-09 01:45:00', title: 'Dr. Mariana Joseph', summary: '3412 Piedmont Rd NE, GA 3032' }
]


render () {
  return (
    <EventCalendar
      eventTapped={this._eventTapped.bind(this)}
      events={this.state.events}
      width={width}
    />
  )
}

```
