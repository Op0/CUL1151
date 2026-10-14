# CUL-1151 Baker's Math

A phone-friendly baker's percentage calculator and math checker for CUL 1151 Baking. It is a single HTML file with no build step and no server.

Live copy: https://op0.github.io/CUL1151/

## Using it

1. Pick a **Recipe** from the dropdown, or build your own by adding ingredients.
2. Enter the **Target dough weight** and, if you are scaling the batch, a **Conversion factor** (blank means 1).
3. Flours each get their own line and together count as 100%. Everything else is a percentage of the flour.
4. Tap **Check my math** to grade the weights you typed, or **Calculate** to have the app fill them in.

The bottom line always shows the running total percentage, the dough weight, the factor, and the score in check mode.

Weights can be in grams or ounces. The **g / oz** switch sits above the ingredient list and converts the target weight and any typed answers.

### Check mode

Type the weight you worked out for each ingredient. Each row is marked correct or incorrect against the expected weight, and the score appears in the bottom line. Answers within 1% of the expected weight count as correct, with a floor of 1 g (or 0.05 oz) so rounding on small amounts like salt and yeast still passes.

### Saving results

After a calculation or check, tap **Save** to keep a copy of the results on your device as a spreadsheet (.xlsx) or a plain text table (.txt). The filename can be edited before saving. Nothing is uploaded or stored anywhere else.

### My recipes

Tap **Save to My recipes** above the Recipe dropdown to keep the current recipe on this device, including its name, unit, target weight, factor, ingredients, and any answers typed so far. Saved recipes appear in a **My recipes** group at the top of the dropdown. Saving again under the same name updates it, and **Delete** removes it after a second tap to confirm. Recipes are stored in the browser on that device only and are never uploaded.

### Settings

Press and hold the title for about half a second to open settings. There you can switch between **Check** and **Calculate** mode and choose a **System**, **Light**, or **Dark** theme. Check mode is the default.

## Recipes

The recipe dropdown holds 27 flour-based formulas from the weekly handouts, with ingredients expressed as baker's percentages. Custards, fillings, frostings, and meringues have no flour base and are not included. `ingredients.md` lists every ingredient found in the handouts and how often each is used, which is how the dropdown's ingredient list was chosen.

Conversions used when a handout gave a volume: 50 g per egg, 3 g per teaspoon of kosher salt, 4 g per teaspoon of baking powder, and standard weights for spices and extracts. Pinches were dropped.

## Running it elsewhere

Open `index.html` in any browser, or host it on any static web server. The page loads two Google Fonts and, only when someone saves an .xlsx file, the SheetJS library from cdnjs. Everything else is inline. The recipe in progress, the unit, and the settings are kept in the browser's local storage on that device only.
