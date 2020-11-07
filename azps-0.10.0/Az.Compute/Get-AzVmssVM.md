---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 43c6f96556cb283ef21f24df00d6a6ddb9c5397a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893697"
---
# Get-AzVmssVM

## STRESZCZENIe
Pobiera właściwości maszyny wirtualnej VMSS.

## POLECENIA

### DefaultParameter (domyślny)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzVmssVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej zestawu skali maszyny wirtualnej (VMSS).
Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.
Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.
Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.

## Przykłady

### Przykład 1: uzyskiwanie właściwości maszyny wirtualnej VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.
Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.

### Przykład 2: uzyskiwanie właściwości widoku modelu maszyny wirtualnej VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.
Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok model.

### Przykład 3: uzyskiwanie właściwości widoku wystąpienia maszyny wirtualnej VMSS
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.
Ponieważ polecenie określa parametr Switch *InstanceView* , polecenie cmdlet umożliwia wyświetlenie widoku wystąpienia maszyny wirtualnej.
Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok wystąpienia.

## PARAMETRÓW

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
Określa identyfikator wystąpienia, dla którego ma zostać wyświetlony widok model.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Gatunek nazwy VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


