---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238599"
---
# Set-AzVmssStorageProfile

## SYNOPSIS
Ustawia właściwości profilu magazynu dla maszyny wirtualnej.

## SKŁADNIA

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skal maszyny wirtualnej (VMSS).

## PRZYKŁADY

### Przykład 1. Ustawianie właściwości profilu magazynu dla usługi maszyny wirtualnej
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

To polecenie ustawia właściwości profilu magazynu dla maszyn wirtualnych o nazwie ContosoVMSS.

## PARAMETERS

### -DataDrive
Określa obiekt dysku danych.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Diff Diff DiffSetting
Określa różne ustawienia dysku systemu operacyjnego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionSetId
Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.  Tę wartość można określić tylko dla dysku zarządzanego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Obraz
Określa identyfikator URI obiektu blob dla obrazu użytkownika.
Narzędzie MASZYNY.WIRTUALNE tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceId
Określa identyfikator odwołania do obrazu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceOffer
Określa typ oferty obrazu maszyny wirtualnej (VIRTUALImage).
Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.

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

### -ImageReferencePublisher
Określa nazwę wydawcy maszyny wirtualnej.
Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.

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

### -ImageReferenceSku
Określa wartość SKU MASZYNY.WIRTUALNEJ.
Aby uzyskać jednostki SKU, użyj Get-AzVMImageSku cmdlet.

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

### -ImageReferenceVersion
Określa wersję programu VMImage.
Aby użyć najnowszej wersji, określ wartość najnowszej zamiast określonej wersji.

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

### -Managed Jednak
Określa dysk zarządzany.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDriveCaching
Określa tryb buforowania dysku systemu operacyjnego. Dopuszczalne wartości dla tego parametru to:
- ReadOnly
- ReadWrite Wartość domyślna to ReadWrite.
Jeśli zmienisz wartość buforowania, polecenie cmdlet uruchomi ponownie maszynę wirtualną.
To ustawienie wpływa na spójność i wydajność dysku.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsCreateOption
Określa sposób, w jaki to polecenie cmdlet tworzy maszyny wirtualne MASZYNY WIRTUALNE.
Dopuszczalne wartości dla tego parametru to:
- Dołączanie: ta wartość jest używana podczas tworzenia maszyny wirtualnej MASZYNY WIRTUALNEJ przy użyciu dysku specjalistycznego. 
- FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej MASZYNY WIRTUALNEJ za pomocą obrazu.
Jeśli używasz obrazu platformy, będziesz również używać *parametru imageReference.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Os Jednakowa_nazwa
Określa nazwę dysku systemu operacyjnego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDriveOsType
Określa typ systemu operacyjnego na dysku.
Jest ona potrzebna tylko w przypadku scenariuszy obrazów użytkowników, a nie dla obrazów platformy.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Os JednakowyAccelerator
Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - VhdContainer
Określa adresy URL kontenera używane do przechowywania dysków systemu operacyjnego dla maszyny wirtualnej.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.
Aby uzyskać obiekt, użyj New-AzVmssConfig obiektu.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.String[]

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDataDla]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


