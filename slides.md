```dataviewjs
let folder = "4Es Discipleship Journey/slides";
let files = app.vault.getFiles().filter(f => f.path.startsWith(folder) && f.extension === "png");

// Sort slides by name numerically/alphabetically
files.sort((a, b) => a.name.localeCompare(b.name, undefined, {numeric: true}));

for (let file of files) {
    dv.paragraph(`![[${file.path}]]`);
}
```
