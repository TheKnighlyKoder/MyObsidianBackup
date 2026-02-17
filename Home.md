---
created_on: 2026-02-12T05:03
last_updated: 2026-02-16T18:04
tags: untagged
---
I ran [5km|mi] today
I had a temp of [98.3F|C]
I need to take [15ml|tsp]
I need to take [3tsp|ml]

[1013hPa|psi]
[[Untitled Kanban]]

[[Feb 11th 2026]]


```dataviewjs
{
    const d = dv.date('today');
    const day = d.day;
    let suffix = (day % 10 === 1 && day !== 11) ? "st" : (day % 10 === 2 && day !== 12) ? "nd" : (day % 10 === 3 && day !== 13) ? "rd" : "th";

    const yearDir = d.toFormat("yyyy"); 
    const monthDir = d.toFormat("(MM) MMMM"); 
    const fileName = d.toFormat("LLL ") + day + suffix + d.toFormat(" yyyy");
    const fullPath = `Bunker Reports/Weekly Reports/${yearDir}/${monthDir}/${fileName}`;

    // Create a styled "Action Button" for the Daily Report
    dv.header(3, "⚡ Mission Control");
    
    // This creates a link that looks like a button
    dv.el("div", `[[${fullPath}|📂 Open Today's Report in Live Preview]]`, { 
        attr: { 
            style: "background: var(--interactive-accent); color: white; padding: 10px; border-radius: 5px; text-align: center; font-weight: bold; cursor: pointer; display: block; width: fit-content; margin: 10px 0;" 
        } 
    });
}
```


```dataviewjs
{
    const d = dv.date('today');
    const day = d.day;
    let suffix = (day % 10 === 1 && day !== 11) ? "st" : (day % 10 === 2 && day !== 12) ? "nd" : (day % 10 === 3 && day !== 13) ? "rd" : "th";

    const yearDir = d.toFormat("yyyy"); 
    const monthDir = d.toFormat("(MM) MMMM"); 
    const fileName = d.toFormat("LLL ") + day + suffix + d.toFormat(" yyyy");
    const fullPath = `Bunker Reports/Weekly Reports/${yearDir}/${monthDir}/${fileName}.md`;

    // 1. Check if the file exists
    const fileExists = await app.vault.adapter.exists(fullPath);

    dv.header(3, "⚡ Mission Control");

    if (fileExists) {
        // IF FILE EXISTS: Show the blue "Open" button for Hover Editor
        dv.el("div", `[[${fileName}|📂 Open Today's Report (Live Preview)]]`, { 
            attr: { 
                style: "background: var(--interactive-accent); color: white; padding: 12px 20px; border-radius: 6px; text-align: center; font-weight: bold; cursor: pointer; display: block; width: fit-content;" 
            } 
        });
    } else {
        // IF FILE MISSING: Show a "Create" button that triggers Periodic Notes
        const btn = dv.el("button", "🛠️ Start Today's Bunker Log", {
            attr: { 
                style: "background: var(--background-modifier-border); color: var(--text-muted); padding: 12px 20px; border-radius: 6px; font-weight: bold; cursor: pointer;" 
            }
        });

        btn.onclick = () => {
            // This triggers the specific Periodic Notes command
            app.commands.executeCommandById('periodic-notes:open-daily-note');
            new Notice("Creating Today's Report...");
        };
    }
}
```

hello how arre  