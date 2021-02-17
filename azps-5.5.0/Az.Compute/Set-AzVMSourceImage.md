---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238629"
---
# Set-AzVMSourceImage

## SYNOPSIS
Określa obraz dla maszyny wirtualnej.

## SKŁADNIA

### ImageReferenceSkuParameterSet (domyślne)
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImageReferenceIdParameterSet
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVMSourceImage** określa obraz platformy do użycia dla maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Ustawianie wartości obrazu
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.
Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Ostatnie polecenie ustawia wartości dla nazwy wydawcy, oferty, wersji i wersji.
Polecenia cmdlet **Get-AzVMImagePublisher,** **Get-AzVMImageOffer,** **Get-AzVMImageSku** i **Get-AzVMImage** mogą wykryć te ustawienia.

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

### — Id
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

### — Oferta
Określa typ oferty MASZYNY WIRTUALNEJ.
Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.

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
Określa nazwę wydawcy maszyny wirtualnej.
Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.

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

### — jednostki SKU
Określa sKU MASZYNY.WIRTUALNEJ.
Aby uzyskać jednostki SKU, użyj Get-AzVMImageSku cmdlet.

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

### — Wersja
Określa wersję maszyny WIRTUALNEJ.
Aby używać najnowszej wersji, określ wartość najnowszej zamiast określonej wersji.

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

### - MASZYNY WIRTUALNEJ
Określa lokalny obiekt maszyny wirtualnej do skonfigurowania.

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

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[New-AzVMConfig](./New-AzVMConfig.md)


