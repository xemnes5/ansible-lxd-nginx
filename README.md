

## 

## Usage

1. Run vagrant:
```
	vagrant up
```

2. Run playbook
```
	ansible-playbook playbook.yml
```

## TEST

- Test root access:
```
	ssh root@192.168.58.100 -p2222 -i users/odmin
```


- Test web server:
```
	curl 192.168.58.100:8080
```

or just open in browser http://192.168.58.100:8080

