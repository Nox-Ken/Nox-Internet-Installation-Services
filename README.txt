NOX INTERNET INSTALLATION SERVICES

Files to publish
- index.html: complete website, with the logo, styles, and scripts embedded.
- nox-data.json: business records read by the website.
- .nojekyll: static file publishing marker.
Keep index.html and nox-data.json in the same folder. Upload the extracted files, rather than the ZIP itself.

First setup on GitHub
1. Extract this package and upload index.html, nox-data.json, and .nojekyll to your repository's publishing folder.
2. If Pages is not configured yet, open repository Settings > Pages. Select Deploy from a branch, your branch, and the folder containing index.html, then Save.
3. Wait for the Pages deployment to complete, then open your published link.
4. Sign in with your NOX account. New browsers start with NOX1107 / admin (administrator) and NOX / viewer (read only).

Your normal update routine
1. Make changes in the website.
2. Click BACKUP in the upper right. It downloads nox-data.json.
3. Open the downloaded JSON in a text editor and copy all its contents.
4. In your GitHub repository, open nox-data.json, click the pencil to edit, replace all contents with the downloaded contents, and commit the change. You can also upload the downloaded file to replace it.
5. Wait until GitHub Pages finishes publishing that commit.
6. Click RESTORE beside the reload button on the website. It immediately fetches and applies the published JSON, while keeping your current account signed in. Press RESTORE on your other devices too.

RESTORE loads the whole published business snapshot. Before replacement, an administrator's previous browser records are downloaded as a recovery copy. A recovery copy is also retained in browser storage. Missing or invalid repository JSON leaves your current records intact.

The file name must stay nox-data.json. If your browser adds a number to a download name, rename the file before uploading it. You can edit valid record values directly in GitHub; keep the JSON structure and use unique record IDs. No checksum needs to be recalculated for this repository format.

Business data is plain JSON and publicly readable through GitHub Pages. The upper-right BACKUP export excludes local accounts, password verifiers, and login tokens. Accounts and theme preferences stay on each browser. RESTORE also accepts earlier NOX JSON backup formats and imports their business records while preserving current local accounts. Use the upper-right BACKUP export for future repository updates.

Included records
The included nox-data.json preserves the saved NOX business snapshot available on 23 October 2026. If you have a more recent backup, replace nox-data.json with its contents before using RESTORE. Keep your own latest backup separately.

Included features
- Current Philippine month calendar, with a brief pending due list for that month.
- Smooth revenue and expense line graph.
- Personal subscribers: monthly obligation, billing start month, due day, monthly balances, partial payments, overdue month count, and total overdue balance.
- Payments can be assigned to the oldest unpaid months first, or to a selected month.
- Existing subscribers need their monthly obligation and billing start configured before overdue balances can be calculated. Rates are not guessed. Editing the rate recalculates bills from the selected billing start month.
- After each dated Vendo harvest, its site/area is due for harvest one calendar month later. The latest active collection replaces the earlier schedule. Shorter months use their final day.
- Light/dark button, with the selected theme remembered on the device.
- Financial reports include the number of Vendo entries harvested. Monthly cash flow statements can be printed.
- Manpower duty calendars, reminders, scanned receipts link, receipt printing, entry deletion, Trash recovery, and local accounts.

Scanned physical receipts
https://drive.google.com/drive/folders/1iajGykO95aG4uSmGfZ-qXPqKTmPhojVy

Recovery and source files
backup/nox-data.json is a second copy of the initial business snapshot. To return to it, copy it over the root nox-data.json, commit, wait for publishing, and press RESTORE.
source/ contains editable application source and build instructions. It is not needed to use the published website. The complete runtime is already in index.html.
