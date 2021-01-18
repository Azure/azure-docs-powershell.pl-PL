---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499145"
---
# Get-AzDigitalTwinsInstance

## STRESZCZENIe
Pobierz zasób DigitalTwinsInstances.

## POLECENIA

### Lista (domyślna)
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### List1
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Opis
Pobierz zasób DigitalTwinsInstances.

## Przykłady

### Przykład 1: lista (domyślnie)
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

Domyślnie Pobierz wszystkie DigitalTwinsInstance

### Przykład 2: Uzyskaj
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

Pobierz określoną AzDigitalTwinsInstance przez resourceName

### Przykład 3: GetViaIdentity
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

Pobieranie określonego AzDigitalTwinsInstance według obiektu

### Przykład 4: list1
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

Pobierz wszystkie DigitalTwinsInstance przez ResourceGroupName

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
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Nazwa DigitalTwinsInstance.

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

### -Subskrypcji
Identyfikator subskrypcji.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
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

### Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IDigitalTwinsIdentity> : parametr Identity
  - `[EndpointName <String>]`: Nazwa zasobu punktu końcowego.
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[Location <String>]`: Lokalizacja DigitalTwinsInstance.
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.
  - `[ResourceName <String>]`: Nazwa DigitalTwinsInstance.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji.

## LINKI POKREWNE

