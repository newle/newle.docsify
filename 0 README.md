# newle.github.io

```dataviewjs
dv.span("**daily note size**") /* optional βΉοΈπ€β‘β π§©βββ³ππΎπππππβ¨οΈπΈοΈππβ¨ */
const calendarData = {
    year: 2022,  // (optional) defaults to current year
    entries: []
}

//DataviewJS loop
for (let page of dv.pages('"daily"')) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name.substring(0,10),     // (required) Format YYYY-MM-DD
        intensity: page.file.size,
        content: await dv.span(`[](${page.file.name})`)
    })
}

renderHeatmapCalendar(this.container, calendarData)
```





