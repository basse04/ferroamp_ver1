# ferroamp_ver1
Create Thing as:
Required parameters
Hostname = 'IP' to energyhub
Username = 'username for energyhub'
Password = 'password for energyhub'

Optional parameter, to be used with several SSO's connected

Channels:
Configure Charge Power, value ex. 5000
Configure Discharge Power, value ex. 12000
Configure Auto Power, value ex. ON

Rules:
configuration: {}
triggers:
  - id: "1"
    configuration:
      cronExpression: 0/15 0 8 * * ? *
    type: timer.GenericCronTrigger
conditions: []
actions:
  - inputs: {}
    id: "2"
    configuration:
      command: "5000"
      itemName: ferroamp_Energy_Hub_Configure_Charge_Power
    type: core.ItemCommandAction


    configuration: {}
triggers:
  - id: "1"
    configuration:
      cronExpression: 0/20 0 8 * * ? *
    type: timer.GenericCronTrigger
conditions: []
actions:
  - inputs: {}
    id: "2"
    configuration:
      command: "12000"
      itemName: ferroamp_Energy_Hub_Configure_Discharge_Power
    type: core.ItemCommandAction
    
    
    configuration: {}
triggers:
  - id: "1"
    configuration:
      cronExpression: 0/25 0 8 * * ? *
    type: timer.GenericCronTrigger
conditions: []
actions:
  - inputs: {}
    id: "2"
    configuration:
      command: ON
      itemName: ferroamp_Energy_Hub_Configure_Auto_Power
    type: core.ItemCommandAction
    
    
    
    
