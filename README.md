# BackupFile Fuzzing on WebSite

A tool for fuzzing files on the website for find backup files


## Usage

```bash
git clone https://github.com/begininvoke/backupfinder.git
cd backupfinder
go build
./backupfinder -url https://site.com 
```
## Help
```bash
./backupfinder -h
Usage of ./backupfinder:

  -url string
        url address https://google.com
  -v    show success result  only
  -o string
        output file path (e.g., /path/to/output.json)
  -f string
        output format (json or csv) (default "json")
```

## Output Formats

### JSON Output
When using `-f json`, the tool will save results in JSON format:
```json
{
    "url": "https://example.com",
    "total_found": 3,
    "files": [
        "https://example.com/backup.zip",
        "https://example.com/db.sql",
        "https://example.com/archive.tar.gz"
    ]
}
```

### CSV Output
When using `-f csv`, the tool will save results in CSV format:
```csv
URL,File
https://example.com,https://example.com/backup.zip
https://example.com,https://example.com/db.sql
https://example.com,https://example.com/archive.tar.gz
```

## Examples
```bash
# Export as JSON
./backupfinder -url https://site.com -o ./results/output.json

# Export as CSV
./backupfinder -url https://site.com -o ./results/output.csv -f csv
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)