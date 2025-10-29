# Four444 PWA Update - Version 5

## Changes in This Version

### ✅ 1. Five Day Cycle RESTORED
- Added back `FIFTH_DAY_START = '2025-10-26'`
- Restored full `isFifthDay()` function
- Restored full `getCycleDay()` function
- Calendar will again show orange indicators on every 5th work day
- Work days exclude Saturdays

### ✅ 2. Custom Icon Support
**Old:** Generic checkmark icon (SVG)
**New:** References your painting photo

The app now uses PNG icon files instead of inline SVG. You need to:
1. Create 5 PNG files from your painting (see ICON_SETUP.md)
2. Upload them with these exact names:
   - icon-152.png
   - icon-167.png
   - icon-180.png (main iPhone icon)
   - icon-192.png
   - icon-512.png

### Previous Updates Still Active:
- ✅ Goals: P1PN, £2MN, S3HM, 1Q84
- ✅ Daily tasks: 10, Objective-led deep work, 60, IKSS
- ✅ LTR list: 171 books

## Files to Upload

### Required Files (3):
1. **index.html** - Five day cycle restored
2. **manifest.json** - Icon references updated
3. **service-worker.js** - Cache v5

### Icon Files (5):
You must create and upload these PNG files from your painting:
1. **icon-152.png** (152×152)
2. **icon-167.png** (167×167)
3. **icon-180.png** (180×180) ⭐ Main icon
4. **icon-192.png** (192×192)
5. **icon-512.png** (512×512)

See **ICON_SETUP.md** for detailed instructions on creating these files.

## Upload Order

1. **First:** Create the 5 icon PNG files from your painting
2. **Then:** Upload all 8 files to GitHub:
   - 3 updated files (index.html, manifest.json, service-worker.js)
   - 5 icon files (.png)
3. **Commit changes**
4. **Wait 1-2 minutes** for GitHub Pages to deploy

## What Users Will See

- Five day cycle indicators return (orange highlights)
- Your painting as the app icon on their home screen (once they re-add it)
- All previous updates remain (goals, tasks, book list)

## Technical Notes

- Service worker cache: **v5**
- Five day cycle start: 2025-10-26
- Icons: PNG format (better quality than SVG for photos)
- Icon sizes optimized for all iOS devices

## Important

Users who already have the app installed will need to:
1. Delete the old app from their home screen
2. Visit the updated site
3. Re-add to home screen to get the new icon

The icon won't update automatically - it's only applied when adding to home screen.
