tags:: Linux

- This command combines stderr and stdout then uses grep with the inversion `-v` flag to find everything except Permission denied responses.
- `find / -name filename 2>$1 | grep -v "Permission denied"`