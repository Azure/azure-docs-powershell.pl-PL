---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350926"
---
# Test-AzKustoClusterNameAvailability

## STRESZCZENIe
Sprawdza, czy nazwa klastra jest prawidłowa i nie jest jeszcze używana.

## POLECENIA

### CheckExpanded (domyślny)
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentityExpanded
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Sprawdza, czy nazwa klastra jest prawidłowa i nie jest jeszcze używana.

## Przykłady

### Przykład 1: Sprawdzanie dostępności nazwy klastra usługi Kusto, która jest w użyciu
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "testnewkustocluster" istnieje w regionie "Wschodnie USA".

### Przykład 2: Sprawdzanie dostępności nazwy klastra Kusto, która nie jest używana
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "availablekustocluster" istnieje w regionie "Wschodnie USA".

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja na platformie Azure.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa klastra.

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

### -Subskrypcji
Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Typ zasobu, Microsoft. Kusto/klastrów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IKustoIdentity> : parametr Identity
  - `[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.
  - `[ClusterName <String>]`: Nazwa klastra usługi Kusto.
  - `[DataConnectionName <String>]`: Nazwa połączenia danych.
  - `[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[Location <String>]`: Lokalizacja platformy Azure.
  - `[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.
  - `[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

## LINKI POKREWNE

