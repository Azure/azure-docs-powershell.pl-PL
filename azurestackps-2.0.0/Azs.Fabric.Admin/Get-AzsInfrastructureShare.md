---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893950"
---
# Get-AzsInfrastructureShare

## STRESZCZENIe
Zwraca żądany udział pliku sieci szkieletowej.

## POLECENIA

### Lista (domyślna)
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### Pobierz
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Opis
Zwraca żądany udział pliku sieci szkieletowej.

## Przykłady

### Przykład 1:
```powershell
PS C:\> Get-AzsInfrastructureShare
```

Zwraca listę wszystkich udziałów plików.

### Przykład 2:
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

Zwraca udział pliku na podstawie nazwy.

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
Nazwa udziału plików w sieci szkieletowej.

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

### -Skip
Parametr pomijania OData.

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

### -Początek
Parametr najwyższy OData.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IFileShare



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
  - `[StorageSubSystem <String>]`: Nazwa systemu przechowywania.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.
  - `[Volume <String>]`: Nazwa woluminu magazynu.

## LINKI POKREWNE

