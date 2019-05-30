# Automated Raspberry Pi Setup and Updates

This is my collection of some pibakery xml, and ansible playbooks for setup and configuration of my assorted raspberry pi projects. Many common raspberry pi configuration options can be set using the raspi-config noint (non-interactive) mode and for anything else I have found the Ansible [lineinfile](http://docs.ansible.com/ansible/lineinfile_module.html) module is perfect for automating configuration that is done via text files.

 For playbooks that use vars_prompts I am passing the prompt variable into the playbook using the "Extra CLI Arguments" box on the semaphore task template. Using the -e (extra vars) CLI argument I am passing in the vars that would be prompted for when running the playbook in bash. I use PiBakery instead of the inital setup script now, but I have kept the new-default playbook up to date.

    ["-e","hostname='your_hostname' wifi_ssid='your_ssid' wifi_password='your_pass'"]
