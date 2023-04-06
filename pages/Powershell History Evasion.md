tags:: Powershell, InfoSec

- Define your own code for determining if a command is written to history
	- `Set-PSReadLineOption -AddToHistoryHandler { return $false }`
- Prevent logging
	- `Set-PSReadlineOption -HistorySaveStyle SaveNothing`
- Delete History
	- `Remove-Item (Get-PSReadlineOption).HistorySavePath`
- Set alternate history file path
	- `Set-PSReadLineOption -HistorySavePath $env:TEMP\out.txt`
- Use ContrainedLanguage mode
	- `$ExecutionContext.SessionState.LanguageMode = “ConstrainedLanguage”`