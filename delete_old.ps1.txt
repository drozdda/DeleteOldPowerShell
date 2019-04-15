$directory = "C:\Users\David\Downloads"
$aged = (Get-Date) - (New-TimeSpan - Days 10)
$listing = Get-ChildItem $directory | Where-Object {$_.LastWriteTime -lt $aged} | `
Remove-Item -Force -ErrorAction SilentlyContinue