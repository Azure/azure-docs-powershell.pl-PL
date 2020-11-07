---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: caf6f142c9669ba3f1b5f343c4bbb1a4dc978a97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706401"
---
# Get-AzVMDscExtensionStatus

## STRESZCZENIe
Pobiera stan obsługi rozszerzeń DSC dla maszyny wirtualnej.

## POLECENIA

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzVMDscExtensionStatus** Pobiera stan programu obsługi rozszerzeń konfiguracji stanu (DSC) dla maszyny wirtualnej w grupie zasobów.
Po zastosowaniu konfiguracji to polecenie cmdlet zapewnia spójność danych wyjściowych za pomocą polecenia cmdlet Start-DscConfiguration.

## Przykłady

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
Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtensionStatus**.
Ten parametr należy określić tylko wtedy, gdy w szablonie Menedżera zasobów zmieniono nazwę domyślną w polu Set cmdlet lub użyto innej nazwy zasobu.

```yaml
Type: System.String
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera stan rozszerzenia DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView

## INFORMACYJN

## LINKI POKREWNE

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


