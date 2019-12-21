# anisbile-playbooks Elasticsearch

## Commands

```
ansible-playbook -i elasticsearch/host.ini elasticsearch/site.yml -K
```

## Sample Output
```
PLAY [elk_vm] ****************************************************************************************************

TASK [Gathering Facts] *******************************************************************************************
ok: [x.x.x.x]

TASK [install default-jre] ***************************************************************************************
ok: [x.x.x.x]

TASK [install default-jre] ***************************************************************************************
ok: [x.x.x.x]

TASK [add es apt-key] ********************************************************************************************
ok: [x.x.x.x]

TASK [install apt-transport-https] *******************************************************************************
ok: [x.x.x.x]

TASK [add artifacts details in sorces.list.d] ********************************************************************
ok: [x.x.x.x]

TASK [install elasticsearch service] *****************************************************************************
ok: [x.x.x.x]

TASK [copy elasticsearch configuration file] *********************************************************************
ok: [x.x.x.x]

TASK [create es data dir and chown to elasticsearch user] ********************************************************
changed: [x.x.x.x] => (item=/data/elasticsearch/data)
changed: [x.x.x.x] => (item=/data/elasticsearch/log)

TASK [enable and start elasticsearch service] ********************************************************************
changed: [x.x.x.x]

PLAY RECAP *******************************************************************************************************
x.x.x.x               : ok=10   changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0  
```