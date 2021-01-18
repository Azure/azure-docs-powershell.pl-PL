---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501913"
---
# Get-AzVMDscExtension

## STRESZCZENIe
Pobiera ustawienia rozszerzenia DSC na określonej maszynie wirtualnej.

## POLECENIA

### GetDscExtension (domyślny)
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VMParameterSet
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzVMDscExtension** pobiera ustawienia żądanego rozszerzenia konfiguracji stanu (DSC) na konkretnej maszynie wirtualnej.

## Przykłady

### Przykład 1: uzyskiwanie ustawień rozszerzenia DSC
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

To polecenie uzyskuje ustawienia dotyczące rozszerzenia o nazwie DSC na maszynie wirtualnej o nazwie VM07.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.
Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtension**.
Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia DSC.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej, na którym znajduje się rozszerzenie.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera rozszerzenie DSC.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


