---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899126"
---
# Start-AzureRmVmss

## STRESZCZENIe
Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureRmVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.
W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .

## Przykłady

### Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.

### Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.
Na przykład: `-InstanceId "0", "3"`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

###  
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Nowe — AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Zatrzymaj — AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


