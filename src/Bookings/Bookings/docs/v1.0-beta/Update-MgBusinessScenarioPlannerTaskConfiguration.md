---
external help file:
Module Name: Microsoft.Graph.Bookings
online version: https://docs.microsoft.com/en-us/powershell/module/microsoft.graph.bookings/update-mgbusinessscenarioplannertaskconfiguration
schema: 2.0.0
---

# Update-MgBusinessScenarioPlannerTaskConfiguration

## SYNOPSIS
Update the properties of a plannerTaskConfiguration object.

## SYNTAX

### UpdateExpanded (Default)
```
Update-MgBusinessScenarioPlannerTaskConfiguration -BusinessScenarioId <String>
 [-AdditionalProperties <Hashtable>] [-EditPolicy <IMicrosoftGraphPlannerTaskPolicy>] [-Id <String>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Update
```
Update-MgBusinessScenarioPlannerTaskConfiguration -BusinessScenarioId <String>
 -BodyParameter <IMicrosoftGraphPlannerTaskConfiguration> [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### UpdateViaIdentity
```
Update-MgBusinessScenarioPlannerTaskConfiguration -InputObject <IBookingsIdentity>
 -BodyParameter <IMicrosoftGraphPlannerTaskConfiguration> [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-MgBusinessScenarioPlannerTaskConfiguration -InputObject <IBookingsIdentity>
 [-AdditionalProperties <Hashtable>] [-EditPolicy <IMicrosoftGraphPlannerTaskPolicy>] [-Id <String>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Update the properties of a plannerTaskConfiguration object.

## EXAMPLES

## PARAMETERS

### -AdditionalProperties
Additional Parameters

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BodyParameter
plannerTaskConfiguration
To construct, please use Get-Help -Online and see NOTES section for BODYPARAMETER properties and create a hash table.

```yaml
Type: Microsoft.Graph.PowerShell.Models.IMicrosoftGraphPlannerTaskConfiguration
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BusinessScenarioId
key: id of businessScenario

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EditPolicy
plannerTaskPolicy
To construct, please use Get-Help -Online and see NOTES section for EDITPOLICY properties and create a hash table.

```yaml
Type: Microsoft.Graph.PowerShell.Models.IMicrosoftGraphPlannerTaskPolicy
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
The unique idenfier for an entity.
Read-only.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, please use Get-Help -Online and see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Graph.PowerShell.Models.IBookingsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns true when the command succeeds

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Graph.PowerShell.Models.IBookingsIdentity

### Microsoft.Graph.PowerShell.Models.IMicrosoftGraphPlannerTaskConfiguration

## OUTPUTS

### System.Boolean

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


BODYPARAMETER <IMicrosoftGraphPlannerTaskConfiguration>: plannerTaskConfiguration
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Id <String>]`: The unique idenfier for an entity. Read-only.
  - `[EditPolicy <IMicrosoftGraphPlannerTaskPolicy>]`: plannerTaskPolicy
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[Rules <IMicrosoftGraphPlannerTaskRoleBasedRule[]>]`: The rules that should be enforced on the tasks when they are being changed outside of the scenario, based on the role of the caller.
      - `[DefaultRule <String>]`: Default rule that applies when a property or action-specific rule is not provided. Possible values are: Allow, Block
      - `[PropertyRule <IMicrosoftGraphPlannerTaskPropertyRule>]`: plannerTaskPropertyRule
        - `[(Any) <Object>]`: This indicates any property can be added to this object.
        - `[RuleKind <String>]`: plannerRuleKind
        - `[AppliedCategories <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
          - `[(Any) <Object>]`: This indicates any property can be added to this object.
          - `[DefaultRules <String[]>]`: The default rules that apply if no override matches to the current data.
          - `[Overrides <IMicrosoftGraphPlannerRuleOverride[]>]`: Overrides that specify different rules for specific data associated with the field.
            - `[Name <String>]`: Name of the override. Allowed override values will be dependent on the property affected by the rule.
            - `[Rules <String[]>]`: Overridden rules. These are used as rules for the override instead of the default rules.
        - `[Assignments <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
        - `[CheckLists <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
        - `[Delete <String[]>]`: Rules and restrictions for deleting the task. Accepted values are allow and block.
        - `[DueDate <String[]>]`: Rules and restrictions for changing the due date of the task. Accepted values are allow and block.
        - `[Move <String[]>]`: Rules and restrictions for moving the task between buckets or plans. Accepted values are allow, moveBetweenPlans, moveBetweenBuckets, and block.
        - `[Notes <String[]>]`: Rules and restrictions for changing the notes of the task. Accepted values are allow and block.
        - `[Order <String[]>]`: Rules and restrictions for changing the order of the task. Accepted values are allow and block.
        - `[PercentComplete <String[]>]`: Rules and restrictions for changing the completion percentage of the task. Accepted values are allow, setToComplete, setToNotStarted, setToInProgress, and block.
        - `[PreviewType <String[]>]`: Rules and restrictions for changing the preview type of the task. Accepted values are allow and block.
        - `[Priority <String[]>]`: Rules and restrictions for changing the priority of the task. Accepted values are allow and block.
        - `[References <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
        - `[StartDate <String[]>]`: Rules and restrictions for changing the start date of the task. Accepted values are allow and block.
        - `[Title <String[]>]`: Rules and restrictions for changing the title of the task. Accepted values are allow and block.
      - `[Role <IMicrosoftGraphPlannerTaskConfigurationRoleBase>]`: plannerTaskConfigurationRoleBase
        - `[(Any) <Object>]`: This indicates any property can be added to this object.
        - `[RoleKind <String>]`: plannerUserRoleKind

EDITPOLICY <IMicrosoftGraphPlannerTaskPolicy>: plannerTaskPolicy
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Rules <IMicrosoftGraphPlannerTaskRoleBasedRule[]>]`: The rules that should be enforced on the tasks when they are being changed outside of the scenario, based on the role of the caller.
    - `[DefaultRule <String>]`: Default rule that applies when a property or action-specific rule is not provided. Possible values are: Allow, Block
    - `[PropertyRule <IMicrosoftGraphPlannerTaskPropertyRule>]`: plannerTaskPropertyRule
      - `[(Any) <Object>]`: This indicates any property can be added to this object.
      - `[RuleKind <String>]`: plannerRuleKind
      - `[AppliedCategories <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
        - `[(Any) <Object>]`: This indicates any property can be added to this object.
        - `[DefaultRules <String[]>]`: The default rules that apply if no override matches to the current data.
        - `[Overrides <IMicrosoftGraphPlannerRuleOverride[]>]`: Overrides that specify different rules for specific data associated with the field.
          - `[Name <String>]`: Name of the override. Allowed override values will be dependent on the property affected by the rule.
          - `[Rules <String[]>]`: Overridden rules. These are used as rules for the override instead of the default rules.
      - `[Assignments <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
      - `[CheckLists <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
      - `[Delete <String[]>]`: Rules and restrictions for deleting the task. Accepted values are allow and block.
      - `[DueDate <String[]>]`: Rules and restrictions for changing the due date of the task. Accepted values are allow and block.
      - `[Move <String[]>]`: Rules and restrictions for moving the task between buckets or plans. Accepted values are allow, moveBetweenPlans, moveBetweenBuckets, and block.
      - `[Notes <String[]>]`: Rules and restrictions for changing the notes of the task. Accepted values are allow and block.
      - `[Order <String[]>]`: Rules and restrictions for changing the order of the task. Accepted values are allow and block.
      - `[PercentComplete <String[]>]`: Rules and restrictions for changing the completion percentage of the task. Accepted values are allow, setToComplete, setToNotStarted, setToInProgress, and block.
      - `[PreviewType <String[]>]`: Rules and restrictions for changing the preview type of the task. Accepted values are allow and block.
      - `[Priority <String[]>]`: Rules and restrictions for changing the priority of the task. Accepted values are allow and block.
      - `[References <IMicrosoftGraphPlannerFieldRules>]`: plannerFieldRules
      - `[StartDate <String[]>]`: Rules and restrictions for changing the start date of the task. Accepted values are allow and block.
      - `[Title <String[]>]`: Rules and restrictions for changing the title of the task. Accepted values are allow and block.
    - `[Role <IMicrosoftGraphPlannerTaskConfigurationRoleBase>]`: plannerTaskConfigurationRoleBase
      - `[(Any) <Object>]`: This indicates any property can be added to this object.
      - `[RoleKind <String>]`: plannerUserRoleKind

INPUTOBJECT <IBookingsIdentity>: Identity Parameter
  - `[BookingAppointmentId <String>]`: key: id of bookingAppointment
  - `[BookingBusinessId <String>]`: key: id of bookingBusiness
  - `[BookingCurrencyId <String>]`: key: id of bookingCurrency
  - `[BookingCustomQuestionId <String>]`: key: id of bookingCustomQuestion
  - `[BookingCustomerBaseId <String>]`: key: id of bookingCustomerBase
  - `[BookingCustomerId <String>]`: key: id of bookingCustomer
  - `[BookingServiceId <String>]`: key: id of bookingService
  - `[BookingStaffMemberBaseId <String>]`: key: id of bookingStaffMemberBase
  - `[BookingStaffMemberId <String>]`: key: id of bookingStaffMember
  - `[BusinessScenarioId <String>]`: key: id of businessScenario
  - `[BusinessScenarioTaskId <String>]`: key: id of businessScenarioTask
  - `[PlannerPlanConfigurationLocalizationId <String>]`: key: id of plannerPlanConfigurationLocalization

## RELATED LINKS

