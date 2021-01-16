---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334222"
---
# Set-AzVMSourceImage

## STRESZCZENIe
Umożliwia określenie obrazu maszyny wirtualnej.

## POLECENIA

### ImageReferenceSkuParameterSet (domyślny)
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImageReferenceIdParameterSet
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVMSourceImage** określa obraz platformy, który ma być używany dla maszyny wirtualnej.

## Przykłady

### Przykład 1. Ustawianie wartości dla obrazu
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.
Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Ostatnie polecenie ustawia wartości dla nazwy, oferty, jednostki SKU i wersji programu Publisher.
Polecenia cmdlet **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku** i **Get-AzVMImage** mogą odnajdować te ustawienia.

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

### -ID
Określa identyfikator.

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Offer
Określa typ oferty VMImage.
Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Określa nazwę wydawcy VMImage.
Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Określa VMImage SKU.
Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Określa wersję VMImage.
Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt lokalnego maszyny wirtualnej do skonfigurowania.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Nowe — AzVMConfig](./New-AzVMConfig.md)


