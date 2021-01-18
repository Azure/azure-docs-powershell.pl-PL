---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499965"
---
# Get-AzResourceGraphQuery

## STRESZCZENIe
Tworzenie kwerendy o pojedynczej grafie przy użyciu jej ResourceName.

## POLECENIA

### Lista (domyślna)
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Pobierz
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Opis
Tworzenie kwerendy o pojedynczej grafie przy użyciu jej ResourceName.

## Przykłady

### Przykład 1: pobieranie wszystkich kwerend wykresu zasobów w grupie zasobów
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

To polecenie pobiera całą kwerendę dotyczącą wykresu zasobów w grupie zasobów.

### Przykład 2: pobieranie zapytania dotyczącego wykresu zasobów według nazwy
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

To polecenie pobiera zapytanie wykresu zasobu według nazwy.

### Przykład 2: pobieranie zapytania dotyczącego wykresu zasobów przez objecy
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

To polecenie pobiera zapytanie wykresu zasobu według obiektu.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa zasobu kwerendy wykresu.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Identyfikator subskrypcji platformy Azure.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. IResourceGraphIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. Api20180901Preview. IGraphQueryResource

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IResourceGraphIdentity> : parametr Identity
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów.
  - `[ResourceName <String>]`: Nazwa zasobu kwerendy wykresu.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.

## LINKI POKREWNE

