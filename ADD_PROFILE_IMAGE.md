How to add your profile photo to the site

The site already expects the profile photo at `assets/images/profile.jpg` and the styles in `style.css` will display it correctly.

Steps

1. Save the image (the one you uploaded here) as `profile.jpg`.
   - Place it in the folder: `assets/images/` (create the folder if it doesn't exist).

2. Verify the HTML reference

   - `index.html` already references `assets/images/profile.jpg` inside the `.profile-media` element.

3. If you prefer to paste the image from the Windows clipboard, run this PowerShell command from the project root (works if an image is in your clipboard):

```powershell
Add-Type -AssemblyName System.Windows.Forms
$img = [System.Windows.Forms.Clipboard]::GetImage()
if ($img -ne $null) { $img.Save("assets/images/profile.jpg", [System.Drawing.Imaging.ImageFormat]::Jpeg) } else { Write-Host "No image found in clipboard." }
```

4. After adding the file, open the site locally or push to GitHub Pages to see the new profile photo.

If you want, attach the image file here (upload it) and I can add it to the project for you, or paste its base64 and I will embed it directly into `index.html`.
