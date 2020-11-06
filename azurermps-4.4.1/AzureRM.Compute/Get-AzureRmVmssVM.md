---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: fcde9de2862590cbf05d680c130bbf7b7f3070d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525685"
---
# Get-AzureRmVmssVM

## STRESZCZENIe
Pobiera właściwości maszyny wirtualnej VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### DefaultParameter (domyślny)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVmssVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej zestawu skali maszyny wirtualnej (VMSS).
Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.
Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.
Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.

## Przykłady

### Przykład 1: uzyskiwanie właściwości maszyny wirtualnej VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.
Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.

### Przykład 2: uzyskiwanie właściwości widoku modelu maszyny wirtualnej VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.
Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok model.

### Przykład 3: uzyskiwanie właściwości widoku wystąpienia maszyny wirtualnej VMSS
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.
Ponieważ polecenie określa parametr Switch *InstanceView* , polecenie cmdlet umożliwia wyświetlenie widoku wystąpienia maszyny wirtualnej.
Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok wystąpienia.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


