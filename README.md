# Task 1
## Ansible Task

#### Setup

- Server VM Ubuntu
- Host VM CentOs with IP address `192.168.10.136`

#### Commands

1. Check connection to the host
```
ping 192.168.10.136
```

2. Generate key pair in server
```
ssh-keygen -t rsa
```

3. Add host to server's Known hosts file
```
ssh-keyscan -H 192.168.10.136 >> ~/.ssh/known_hosts
```

4. Send public key to host
```
ssh-copy-id root@192.168.10.136
```

5. Clone repository 
```
git clone https://github.com/M-Hossam-Zaazoue/Task1.git
```

6. Run playbook
```
cd ~/Task1
ansible-playbook -i hosts playbook.yaml
```