# RPiOS-Personalization

My personal OS preferences for Raspbian OS. This includes bash aliases, keyboard mappings for the terminal (like pressing the up arrow after starting to type a command to perform a reverse search through the command history) as well as installing OS and global python packages using Pipx.

## Requirements

This is only intended for systems running the headless Raspbian OS Lite. 

## Role Variables

`global_python_packages` - List of packages to be installed with pipx. 

## Dependencies

None.

## Example Playbook

For anyone else reading this I recommend forking my repository and making changes to suit your own preferences in your own fork. 

Use a requirements.yml file with the following contents modified to point to your own fork.

```yaml
---
roles:
- src: https://github.com/agarthetiger/rpios-personalization
```

Install the role using Ansible Galaxy. Either run this from the same folder as the requirements.yml is in, or provide the full path to the requirements.yml file. Run `ansible-galaxy install -h` for help about this command.

```bash
ansible-galaxy install -r requirements.yml
```

Now you can run your playbook using the installed role.

```yaml
- hosts: all
  roles:
      - rpios-personalization
```

## License

MIT

## Author Information

Andrew Garner (@agarthetiger)
