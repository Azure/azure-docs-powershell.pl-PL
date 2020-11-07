---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893469"
---
# Save-AzVMImage

## STRESZCZENIe
Umożliwia zapisanie maszyny wirtualnej jako VMImage.

## POLECENIA

### ResourceGroupNameParameterSetName (domyślny)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Save-AzVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.
Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzVM.

Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.
Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.

## Przykłady

### Przykład 1: Przechwytywanie maszyny wirtualnej
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.

Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.
Właściwość **Output** zwraca szablon JSON.

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

### -DestinationContainerName
Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.

Jeśli kontener nie istnieje, zostanie on utworzony.
Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.
Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.
Adres URL zapisanego obrazu jest podobny do: 

https:// \< storageAccountName \> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Określa identyfikator zasobu maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wskazuje, że to polecenie cmdlet zastępuje wszystkie dyski VHD, które mają ten sam prefiks w kontenerze docelowym.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Określa ścieżkę dysku VHD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
Określa prefiks w nazwie obiektów blob, które tworzą profil przechowywania VMImage.

Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \< GUID \> . VHD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
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

### Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


