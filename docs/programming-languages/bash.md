# Bash

## Snippets

### Print without newline
```bash
echo -n "Enter:"
```

### Change directory to scripts directory
```bash
cd $( dirname -- "$0"; )
```

### Prompt for user input
```bash
echo -n Enter:
read host_to_deploy
echo "You entered '$host_to_deploy'"
```

### If value is not in list
```bash
if [[ " $hosts_to_select_from " =~ .*\ $host_to_deploy\ .* ]]; then
    ...
fi
```

### Print values in list with newlines
```bash
current_files=$(ls)
for file in ${current_files[@]}
do
   echo "  - ${file}"
done
```


