---
template: note
tags: HowTo, Article
source: https://benenewton.medium.com/adding-the-current-weather-to-my-obsidian-daily-note-793591026a0a
author: "Ben Newton"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1501446393885-828292b7670a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4NjY1OTQ0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-24) | (time:: 18:02) | (weather:: Vadodara: 🌦   +26°C ↑18km/h)

# Obsidian - Add weather details to your Notes

## Highlights
(highlightsURL:: [Glasp Highlight](https://share.glasp.co/ManadayM/?p=ehHSYkQqioE2ePbG40VW))
- All you need is the Templater plugin.
- In your Templater options, go to User Functions and add the following.
- getWeather
- // With City Name (Plantation) curl wttr.in/Plantation\?format=”%l:+%c+%t+feels+like+%f\nSunrise:+%S\nSunset:++%s\nMoon:++++%m\n”
- Then in your daily note template, add this line where you want the weather:
- Weather: <% tp.user.getWeather() %>
- This text will render the result of the user function getWeather.

## Notes
```bash
curl wttr.in/Vadodara?format="%l:+%c+%t+%w\n"
```