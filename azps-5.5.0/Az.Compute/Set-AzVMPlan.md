---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196970"
---
# Set-AzVMPlan

## SYNOPSIS
Ustawia informacje o planie usługi Marketplace na komputerze wirtualnym.

## SKŁADNIA

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVMPlan** ustawia informacje o planie usługi Azure Marketplace dla maszyny wirtualnej.
Aby można było wdrożyć obraz z witryny Marketplace za pośrednictwem wiersza polecenia, należy włączyć dostęp programowy lub wdrożyć maszynę wirtualną przy użyciu portalu Azure Portal.

## PRZYKŁADY

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Określa nazwę obrazu z witryny Marketplace.
Jest to ta sama wartość, która jest zwracana przez Get-AzVMImageSku cmdlet.
Aby uzyskać więcej informacji o tym, jak znaleźć informacje o obrazach, zobacz Nawigowanie po obrazach maszyn wirtualnych platformy Azure i wybieranie ich za pomocą programu PowerShell i interfejsu cli platformy Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (w https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) dokumentacji platformy Microsoft Azure).

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

### — Produkt
Określa igiełę obrazu z witryny Marketplace.
Są to te same informacje co wartość **Offer** elementu **imageReference.**

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

### -PromotionCode
Określa kod promocyjny.

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

### — Publisher
Określa wydawcę obrazu.
Możesz znaleźć te informacje za pomocą polecenia cmdlet Get-AzVMImagePublisher cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - MASZYNY WIRTUALNEJ
Określa obiekt maszyny wirtualnej, dla którego ma być ustawiany plan usługi Marketplace.
Aby uzyskać obiekt maszyny wirtualnej, Get-AzVM użyć polecenia cmdlet.
Możesz użyć polecenia cmdlet New-AzVMConfig, aby utworzyć obiekt maszyny wirtualnej.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[New-AzVMConfig](./New-AzVMConfig.md)
