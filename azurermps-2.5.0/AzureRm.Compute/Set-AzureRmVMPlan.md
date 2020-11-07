---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899368"
---
# Set-AzureRmVMPlan

## STRESZCZENIe
Umożliwia ustawienie informacji dotyczących planu rynkowego na maszynie wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmVMPlan** ustawia informacje dotyczące planu Azure Marketplace dla maszyny wirtualnej.

Przed rozpoczęciem wdrażania obrazu witryny Marketplace za pośrednictwem wiersza polecenia program dostęp programistyczny musi być włączony lub wdrożenie maszyny wirtualnej za pomocą portalu Azure.

## Przykłady

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

### -Name (nazwa)
Określa nazwę obrazu na podstawie witryny Marketplace.
Jest to ta sama wartość, która jest zwracana przez polecenie cmdlet Get-AzureRmVMImageSku.
Aby uzyskać więcej informacji na temat znajdowania informacji o obrazach, zobacz Nawigowanie i wybieranie obrazów maszyny wirtualnej platformy Azure za pomocą programu PowerShell i usługi Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) w dokumentacji platformy Microsoft Azure).

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

### -Product
Określa iloczyn obrazu z witryny Marketplace.
Jest to ta sama informacja, co wartość **oferty** elementu **imageReference** .

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wydawca
Umożliwia określenie wydawcy obrazu.
Te informacje można znaleźć przy użyciu Get-AzureRmVMImagePublisher polecenia cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej, dla którego ma zostać ustawiony plan rynku.
Możesz użyć polecenia cmdlet Get-AzureRmVM, aby uzyskać obiekt maszyny wirtualnej.
Możesz użyć polecenia cmdlet New-AzureRmVMConfig, aby utworzyć obiekt maszyny wirtualnej.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSVirtualMachine
Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Nowe — AzureRmVMConfig](./New-AzureRmVMConfig.md)
