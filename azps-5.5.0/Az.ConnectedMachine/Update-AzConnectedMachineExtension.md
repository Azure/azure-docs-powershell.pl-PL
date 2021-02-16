---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177387"
---
# Update-AzConnectedMachineExtension

## SYNOPSIS
Operacja tworzenia lub aktualizowania rozszerzenia.

## SKŁADNIA

### UpdateExpanded (Domyślna)
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Aktualizacja
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentity
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## OPIS
Operacja tworzenia lub aktualizowania rozszerzenia.

## PRZYKŁADY

### Przykład 1. Aktualizowanie rozszerzenia
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualizuje rozszerzenie na określonym komputerze.

### Przykład 2. Aktualizowanie rozszerzenia przy użyciu lokalizacji określonej za pośrednictwem potoku
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.
W tym miejscu używamy rozszerzenia przekazywanego za pośrednictwem potoku, aby pomóc nam w określeniu, na którym rozszerzeniu chcemy pracować, i określamy, co chcemy zmienić za pośrednictwem normalnych parametrów `-Settings` (np.)

### Przykład 3. Aktualizowanie rozszerzenia przy użyciu parametrów rozszerzenia określonych za pośrednictwem potoku
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.
Tutaj używamy rozszerzenia przekazywanego za pośrednictwem potoku, aby udostępnić zmiany, które chcemy wprowadzić w ramach rozszerzenia.
Lokalizacja rozszerzenia nie jest pobierana za pośrednictwem potoku, lecz za pośrednictwem parametrów określonych normalnie (przez parametr splat).

### Przykład 4. Używanie obiektu rozszerzenia jako lokalizacji i parametrów aktualizacji
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.
W tym miejscu używamy rozszerzenia przekazanego za pośrednictwem potoku, aby pomóc nam w identyfikować, nad którym rozszerzeniem chcemy pracować.
Oprócz tego do określenia, co należy zaktualizować, używamy parametrów obiektu rozszerzenia.

## PARAMETERS

### — AsJob
Uruchamianie polecenia jako zadania

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

### -AutoUpgradeMinorVersion
Wskazuje, czy rozszerzenie powinno używać nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.
Jednak po wdrożeniu rozszerzenia nie zostanie uaktualnione wersje pomocnicze, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionParameters
W tym artykule opisano aktualizację rozszerzenia komputera.
Aby skonstruować, zobacz sekcję UWAGI, aby uzyskać informacje o właściwościach właściwości EXTENSIONPARAMETERS i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ForceRerun
Jak należy wymusić aktualizację programu obsługi rozszerzenia, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.

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
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa_komputera
Nazwa komputera, na którym należy utworzyć lub zaktualizować rozszerzenie.

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

### — Nazwa
Nazwa rozszerzenia komputera.

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

### -NoWait
Uruchamianie polecenia asynchronicznie

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

### -ProtectedSetting
Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault albo nie ma żadnych ustawień chronionych.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Publisher
Nazwa wydawcy programu obsługi rozszerzenia.

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

### -ResourceGroupName
Nazwa grupy zasobów.

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

### — Ustawienie
Formatowane ustawienia publiczne rozszerzenia.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi zasobów

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

### — Wpisz
Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".

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

### -TypeHandlerVersion
Określa wersję programu obsługi skryptów.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate

### Microsoft.Azure.PowerShell.Cmdlet.ConnectedMachine.Models.IConnectedMachineIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


EXTENSIONPARAMETERS: <IMachineExtensionUpdate> W tym artykule opisano aktualizację rozszerzenia komputera.
  - `[Tag <IUpdateResourceTags>]`: tagi zasobów
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[AutoUpgradeMinorVersion <Boolean?>]`: wskazuje, czy rozszerzenie powinno korzystać z nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrażania. Jednak po wdrożeniu rozszerzenia nie zostanie uaktualnione wersje pomocnicze, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.
  - `[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację programu obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.
  - `[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault lub nie może mieć żadnych ustawień chronionych.
  - `[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.
  - `[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json sformatował ustawienia publiczne dla rozszerzenia.
  - `[Type <String>]`: określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".
  - `[TypeHandlerVersion <String>]`: określa wersję programu obsługi skryptów.

INPUTOBJECT: <IConnectedMachineIdentity> Parametr tożsamości
  - `[ExtensionName <String>]`: nazwa rozszerzenia komputera.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Name <String>]`: nazwa komputera hybrydowego.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

## LINKI POKREWNE

