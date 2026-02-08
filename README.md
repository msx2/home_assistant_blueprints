# Home Assistant Blueprints

Set of my personal home assistant blueprints.

## Moonraker Print State Notifications

This blueprint allows you to receive notifications when your 3D printer pauses or completed the print. Additionally, you can attach a snapshot from printer's camera upon completion, and turn off the light inside your printer. It creates a temporary snapshot file in the `/www/snapshots/` directory, so make sure to have it created and accessible by Home Assistant. To keep things clean, the snapshot file is deleted 15 seconds after notification is sent, in order to achieve this, you need the following added into your `configuration.yaml`:

```yaml
shell_command:
  delete_file: 'rm {{ filename }}'
```

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmsx2%2Fhome_assistant_blueprints%2Fblob%2Fmain%2Fmoonraker_print_state_notifications.yaml)


### Notification examples
<img src="https://raw.githubusercontent.com/msx2/home_assistant_blueprints/refs/heads/main/assets/moonraker_print_state_notifications/notifications.jpg" width="500">
<img src="https://raw.githubusercontent.com/msx2/home_assistant_blueprints/refs/heads/main/assets/moonraker_print_state_notifications/completed.jpg" width="500">


## ZHA Zigbee Button

This blueprint allows you to use a Zigbee button configured with `Zigbee Home Automation` integration to control various actions in Home Assistant. You can configure single press, double press, and long press actions.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmsx2%2Fhome_assistant_blueprints%2Fblob%2Fmain%2Fzha_zigbee_button.yaml)
