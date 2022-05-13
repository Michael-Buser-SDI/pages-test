# Accommodation Booking Cancelled

###

## Javascript Code

```js
window.appEventData = window.appEventData || [];
appEventData.push({
	event: 'Accommodation Booking Cancelled',
	booking: {
		roomList: [
			{
				location: {
					locationId: '<locationId>'
				}
			}
		]
	}
});
```

## Variable Definitions

| Path                                    | Type   | Description                      | Example               | Pattern | Min Length | Max Length | Minimum | Maximum | Multiple Of |
| --------------------------------------- | ------ | -------------------------------- | --------------------- | ------- | ---------- | ---------- | ------- | ------- | ----------- |
| booking.roomList[n].location.locationId | string | Unique Identifier of a Location. | 155, 65588, 987764448 |         |            |            |         |         |             |
