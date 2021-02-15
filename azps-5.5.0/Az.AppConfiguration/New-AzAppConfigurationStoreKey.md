---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182299"
---
# New-AzAppConfigurationStoreKey

## SYNOPSIS
Ponownie generuje klucz dostępu dla określonego magazynu konfiguracji.

## SKŁADNIA

### Generuj ponownieRozwiń (domyślne)
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Generuj generujViaIdentityExpanded
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Ponownie generuje klucz dostępu dla określonego magazynu konfiguracji.

## PRZYKŁADY

### Przykład 1. Klucz ponownego generowania magazynu konfiguracji aplikacji
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

To polecenie umożliwia ponowne wygenerowanie klucza magazynu konfiguracji aplikacji.

### Przykład 2. Ponowne generowanie klucza magazynu konfiguracji aplikacji według obiektu
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

To polecenie umożliwia ponowne wygenerowanie klucza magazynu konfiguracji aplikacji według obiektów.

## PARAMETERS

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

### — Identyfikator
Identyfikator klucza do ponownego wygenerowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa magazynu konfiguracji.

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, do której należy rejestr kontenera.

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji platformy Microsoft Azure.

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.IAppConfigurationIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IApiKey

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppConfigurationIdentity> Parametr tożsamości
  - `[ConfigStoreName <String>]`: nazwa magazynu konfiguracji.
  - `[GroupName <String>]`: nazwa grupy zasobów linku prywatnego.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy rejestr kontenerów.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.

## LINKI POKREWNE

