---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054287"
---
# Get-AzsEdgeGatewayPool

## STRESZCZENIe


## POLECENIA

### Lista (domyślna)
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Pobierz
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Opis


## Przykłady

### Przykład 1. Aby uzyskać listę wszystkich pul granicznych bram.
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

Wyświetlanie listy wszystkich pul z systemem Edge.

### Przykład 2: uzyskiwanie określonej puli bram brzegowych.
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

Pobierz określoną pulę bram brzegowych.

## PARAMETRÓW

### -DefaultProfile


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

### -Filter


```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Inputobject
Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### — Lokalizacja


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (nazwa)


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

### -PassThru


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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -Subskrypcji


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

### Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IEdgeGatewayPool



## INFORMACYJN

ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.

INPUTobject <IFabricAdminIdentity> : 
  - `[Drive <String>]`: Nazwa dysku magazynu.
  - `[EdgeGateway <String>]`: Nazwa bramy granicznej.
  - `[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.
  - `[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.
  - `[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.
  - `[IPPool <String>]`: Nazwa puli adresów IP.
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[InfraRole <String>]`: Nazwa roli infrastruktury.
  - `[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.
  - `[Location <String>]`: Lokalizacja zasobu.
  - `[LogicalNetwork <String>]`: Nazwa sieci logicznej.
  - `[LogicalSubnet <String>]`: Nazwa podsieci logicznej.
  - `[MacAddressPool <String>]`: Nazwa puli adresów MAC.
  - `[Operation <String>]`: Identyfikator operacji.
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów.
  - `[ScaleUnit <String>]`: Nazwa jednostki skali.
  - `[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.
  - `[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.
  - `[StorageSubSystem <String>]`: Nazwa systemu przechowywania.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.
  - `[Volume <String>]`: Nazwa woluminu magazynu.

## LINKI POKREWNE

