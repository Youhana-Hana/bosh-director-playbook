Run the playbook substituting the variable placeholders:

    `ansible-playbook -i ./inventory ./main.yml -e ansible_ssh_user=user -e ansible_ssh_pass=PASSWORD -e ansible_ssh_port=22 -e vsphere_user=VSPHERE_USER -e vsphere_password=VSPHERE-PASSWORD -e environment_name=ENVIRONMENT_NAME -e git_token=GIT_TOKEN -e git_url=GIT_URL -e director_ip=DIRECTOR_IP `

This will download files into the /tmp folder of your workstation and upload files to the ~/git-repos folder of your target VM (i.e. tools VM). Specifically, it will

1. (On your workstation) Download the required bosh releases (bosh, Concourse, Minio, Postgres)
2. (On your workstation) Download the required bosh stemcells
3. (On the target machine i.e. Tools VM) Clone from git the pcf-automation & pcf-automation-deployments repos
4. (From your workstation to the target machine i.e. Tools VM) Upload the bosh releases and stemcells
5. (On your workstation) Clone from GitHub the open source bosh-deployment repo
6. (From your workstation to the target machine i.e. Tools VM) Upload the bosh-deployment repo
7. (On the target VM i.e. Tools VM) Execute the pcf automation script (~/git-repos/pcf-automation/pcf-automation-setup)
