# ansible-role-kafka-ui

<table style="border:0px; width:100%"><tr><td width=160px valign=top><img src="media/icon_kafkaui.png" alt="Kafka UI icon" width=128 height=128></td>
<td>
Ansible role for installation, configuration, usage and management of Kafka UI, a web-based UI for managing Apache Kafka clusters. The UI is accessible after installation via `https://<servername/ip>:8080`<br><br>Official website: `https://github.com/provectus/kafka-ui`<br><br>
</td>
</tr></table>

Ansible role Kafka UI : [Design](docs/DESIGN.md)  |  [Examples](examples)  |  [Test](molecule)  |  [Issues]()  |<br>
Latest version:

# Actions:

<table style="border:0px; width:100%">
<tr><th>Deployment</th><th>Administration</th></tr>
<tr>
  <td valign=top>install<br>uninstall<br>update</td>
  <td valign=top>configure<br>start<br>stop<br></td>
</tr></table>

## Deployment

action: **install**<br>
Installation of the latest Provectus Kafka UI version.<br>
variables:<br>
<kbd>uninstall</kbd> (optional) : Uninstall existing Kafka UI instance before installation.<br>

```
- name: Install Kafka UI
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : install
```


action: **uninstall**<br>
Uninstallation of Provectus Kafka UI.<br>
variables:<br>
<kbd>(none)</kbd> : No variables required.<br>

```
- name: Uninstall Kafka UI
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : uninstall
```

## Administration

action: **start**<br>
Start of Kafka UI service. `ROADMAP`.<br>
variables:<br>
<kbd>(none)</kbd> : No variables required.<br>

```
- name: Start Kafka UI service
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : start
```


action: **stop**<br>
Stop of Kafka UI service. `ROADMAP`.<br>
variables:<br>
<kbd>(none)</kbd> : No variables required.<br>

```
- name: Stop Kafka UI service
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : stop
```


action: **configure**<br>
Reconfiguration of Kafka UI. `ROADMAP`.<br>
variables:<br>
<kbd>(none)</kbd> : No variables required.<br>

```
- name: Configure Kafka UI service
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : configure
```


***

- **changelog**<br>
  Change log.
  See [changelog](CHANGELOG.md)

- **roadmap**<br>
  Vision and future developments.
  See [roadmap](ROADMAP.md)

***

## Preparations
(none).


## Dependencies
Dependencies are listed in the **requirements.yml** file.<br>
Use `ansible-galaxy install ./requirements.yml --force` for installation.<br>
If this role is used in other playbooks or Ansible projects, the URL of this role must be added to the `requirements.yml` file. Using the above command, the role will be placed in the correct folder structure.


## Installation and configuration
Installation via the action variable <kbd>install</kbd>. (Re-)configuration via the action variable <kbd>configure</kbd>.

When using this role in other playbooks or Ansible projects:
```
- name: Install and configure Kafka UI
  hosts: localhost
  roles:
   - role: kafka-ui
     vars:
       action : install
```


When used as a stand-alone Ansible project:
```
- name: Install and configure Kafka UI
  hosts: localhost
  tasks:

    - name: Install Kafka UI
      ansible.builtin.include_tasks:
        file: tasks/install.yml
```

## Additional information
The UI is accessible via `https://<servername/ip>:8080`. 

## License
MIT

## Author
Marcel Venema
