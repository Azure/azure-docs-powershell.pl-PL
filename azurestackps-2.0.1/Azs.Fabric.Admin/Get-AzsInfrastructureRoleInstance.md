---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054193"
---
# Get-AzsInfrastructureRoleInstance

## STRESZCZENIe
Zwracanie żądanej instancji roli infrastruktury.

## POLECENIA

### Lista (domyślna)
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Pobierz
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Opis
Zwracanie żądanej instancji roli infrastruktury.

## Przykłady

### Przykład 1:
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

Zwraca listę wszystkich wystąpień ról infrastruktury.

### Przykład 2:
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

Zwracanie pojedynczego wystąpienia roli infrastruktury na podstawie nazwy.

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

### -Filter
Parametr filtru OData.

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
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

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
Lokalizacja zasobu.

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
Nazwa wystąpienia roli infrastruktury.

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
Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.

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
Nazwa grupy zasobów.

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
Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

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

### Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IInfraRoleInstance



## INFORMACYJN

ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.

INPUTobject <IFabricAdminIdentity> : parametr Identity
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
  - `[StoragePool <String>]`: Nazwa puli magazynu.
  - `[StorageSubSystem <String>]`: Nazwa systemu przechowywania.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.
  - `[Volume <String>]`: Nazwa woluminu magazynu.

## LINKI POKREWNE

