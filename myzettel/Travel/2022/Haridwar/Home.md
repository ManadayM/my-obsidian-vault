---
template: travel
starts: "2022-10-21T05:30:00"
ends: "2022-10-27T10:50:00"
aliases: [Haridwar]
---
# Haridwar
![tp.web.random_picture](https://images.unsplash.com/photo-1511754863001-18d44abd0a93?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMTQ2ODIx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

## Checklist
- [ ] 

## Places to visit
- [ ] 

## Tickets 🎫
```dataview
TABLE WITHOUT ID
	link(file.link, train_no) AS Train,
	elink(pnr_status, pnr) AS PNR,
	boarding_from AS From,
	boarding_to AS To,
	dateformat(date(reporting_time), "dd-MM HH:mm") AS Reporting,
	dateformat(date(departure_time), "dd-MM HH:mm") AS Departure,
	dateformat(date(arrival_time), "dd-MM HH:mm") AS Arrival
FROM "Travel/2022/Haridwar" 
WHERE contains(template, "ticket")
SORT date(departure_time) ASC
```

---
#### Internal Links
[[2022]], [[Travel]]