# GoCDtest: GoCD Pipeline + Ansible Playbook
This if for quick testing GoCD pipeline which is calling Ansible to install Apache server on CI

```
[go] Job Started: 2020-07-03 15:17:54 CEST

[go] Start to prepare TestingAnsibleWithGoCD/23/stageOne/1/ansible-playbook on ls-tmp-000-021 [/var/lib/go-agent]
    [go] Start to update materials.

    [go] Start updating files at revision 88d030caa15037b83635c85caca37b1507770e2d from https://github.com/lgs/GoCDtest
    [GIT] Fetching changes
    STDERR: From https://github.com/lgs/GoCDtest
    STDERR:    5d9ecb6..b045e39  master     -> origin/master
    [GIT] Performing git gc
    [GIT] Reset working directory pipelines/TestingAnsibleWithGoCD
    [GIT] Cleaning all unversioned files in working copy
    [GIT] Cleaning submodule configurations in .git/config
    [GIT] Updating working copy to revision 88d030caa15037b83635c85caca37b1507770e2d
    HEAD is now at 88d030c drop hosts
    [GIT] Removing modified files in submodules
    [GIT] Cleaning all unversioned files in working copy
    [go] Done.

    [go] setting environment variable 'GO_SERVER_URL' to value 'https://localhost:8154/go'
    [go] setting environment variable 'GO_PIPELINE_GROUP_NAME' to value 'defaultGroup'
    [go] setting environment variable 'GO_TRIGGER_USER' to value 'changes'
    [go] setting environment variable 'GO_PIPELINE_NAME' to value 'TestingAnsibleWithGoCD'
    [go] setting environment variable 'GO_PIPELINE_COUNTER' to value '23'
    [go] setting environment variable 'GO_PIPELINE_LABEL' to value '23'
    [go] setting environment variable 'GO_STAGE_NAME' to value 'stageOne'
    [go] setting environment variable 'GO_STAGE_COUNTER' to value '1'
    [go] setting environment variable 'GO_JOB_NAME' to value 'ansible-playbook'
    [go] setting environment variable 'GO_REVISION' to value '88d030caa15037b83635c85caca37b1507770e2d'
    [go] setting environment variable 'GO_TO_REVISION' to value '88d030caa15037b83635c85caca37b1507770e2d'
    [go] setting environment variable 'GO_FROM_REVISION' to value '88d030caa15037b83635c85caca37b1507770e2d'
    [go] setting environment variable 'GO_MATERIAL_URL' to value 'https://github.com/lgs/GoCDtest'
    [go] setting environment variable 'GO_MATERIAL_BRANCH' to value 'master'
    [go] setting environment variable 'GO_MATERIAL_HAS_CHANGED' to value 'true'

[go] Start to build TestingAnsibleWithGoCD/23/stageOne/1/ansible-playbook on ls-tmp-000-021 [/var/lib/go-agent]

[go] Task: /bin/ansible-playbook httpd.ymltook: 8.309s
    [WARNING]: provided hosts list is empty, only localhost is available. Note that
    the implicit localhost does not match 'all'

    PLAY [This sets up an httpd webserver] *****************************************

    TASK [Install apache packages] *************************************************
    changed: [127.0.0.1]

    TASK [ensure httpd is running] *************************************************
    [WARNING]: Consider using 'become', 'become_method', and 'become_user' rather
    than running sudo
    ok: [127.0.0.1]

    PLAY RECAP *********************************************************************
    127.0.0.1                  : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

    [go] Task status: passed, took: 8.309s

[go] Current job status: passed

[go] Start to create properties TestingAnsibleWithGoCD/23/stageOne/1/ansible-playbook on ls-tmp-000-021 [/var/lib/go-agent]

[go] Start to upload TestingAnsibleWithGoCD/23/stageOne/1/ansible-playbook on ls-tmp-000-021 [/var/lib/go-agent]

[go] Job completed TestingAnsibleWithGoCD/23/stageOne/1/ansible-playbook on ls-tmp-000-021 [/var/lib/go-agent]


```
