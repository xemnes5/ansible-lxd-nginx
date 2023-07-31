

## First steps 
- clone repo:
```
	git clone https://github.com/xemnes5/ansible-lxd-nginx ./
```
- fix messed up permissions:
```
	chmod 0600 users/odmin
	chmod 0600 users/pupa
```

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

