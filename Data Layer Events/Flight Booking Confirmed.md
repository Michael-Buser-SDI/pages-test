# Flight Booking Confirmed

###

## Javascript Code

```js
window.appEventData = window.appEventData || [];
appEventData.push({
	event: 'Flight Booking Confirmed',
	airTravel: {
		companionFareIndicator: '<companionFareIndicator>',
		flightList: [
			{
				tripId: '<tripId>'
			}
		]
	},
	booking: {
		reservationId: '<reservationId>'
	},
	voucherDiscount: {
		discountCode: '<discountCode>',
		discountCodeStatus: '<discountCodeStatus>'
	}
});
```

## Variable Definitions

| Path                               | Type   | Description                                                                                                               | Example                                                             | Pattern                  | Min Length | Max Length | Minimum | Maximum | Multiple Of |
| ---------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------ | ---------- | ---------- | ------- | ------- | ----------- |
| airTravel.companionFareIndicator   | string | An indication of whether a companion fare is available \/ being requested \/ used for the trip.                           | available, unavailable, in use                                      |                          |            |            |         |         |             |
| airTravel.flightList[n].tripId     | string | A unique representation of the main departure and arrival points for all primary trip legs \(not including connections\). | SFO&gt;YYC:YYC&gt;SFO, SFO&gt;YYC, SFO&gt;YYC:YYC&gt;YXC:YKA&gt;SFO | ^([A-Z]{3}>[A-Z]{3}:?)+$ |            |            |         |         |             |
| booking.reservationId              | string | A unique identifier of a booking used for communication between customer and booking company                              | ADFIG986958, IUFO89699, XDF-875008767                               |                          |            |            |         |         |             |
| voucherDiscount.discountCode       | string | Discount code entered or applied                                                                                          | 5OFFSHOES, AKRONCANDLES2019                                         |                          |            |            |         |         |             |
| voucherDiscount.discountCodeStatus | string | Indicates whether a discount code is valid, expired, or invalid.                                                          | valid, invalid, expired                                             |                          |            |            |         |         |             |
