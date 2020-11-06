---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552987"
---
# Save-AzureRmVMImage

## STRESZCZENIe
Umożliwia zapisanie maszyny wirtualnej jako VMImage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ResourceGroupNameParameterSetName (domyślny)
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Save-AzureRmVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.
Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzureRmVM.

Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.
Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.

## Przykłady

### Przykład 1: Przechwytywanie maszyny wirtualnej
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.

Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.
Właściwość **Output** zwraca szablon JSON.

## PARAMETRÓW

### -DestinationContainerName
Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.

Jeśli kontener nie istnieje, zostanie on utworzony.
Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.
Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.
Adres URL zapisanego obrazu jest podobny do: 

https:// \<storageAccountName\> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.

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

Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \<guid\> . dysków.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Set-AzureRmVM](./Set-AzureRmVM.md)


