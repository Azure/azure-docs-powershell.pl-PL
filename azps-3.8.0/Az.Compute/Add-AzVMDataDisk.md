---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052420"
---
# Add-AzVMDataDisk

## STRESZCZENIe
Dodaje dysk danych do maszyny wirtualnej.

## POLECENIA

### VmNormalDiskParameterSetName (domyślny)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVMDataDisk** dodaje dysk danych do maszyny wirtualnej.
Dysk danych można dodać podczas tworzenia maszyny wirtualnej lub można dodać dysk z danymi do istniejącej maszyny wirtualnej.

## Przykłady

### Przykład 1: Dodawanie dysków z danymi do nowej maszyny wirtualnej
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Kolejne trzy polecenia przypisują ścieżki trzech dysków z danymi do $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03 zmiennych.
Taka metoda dotyczy tylko czytelności następujących poleceń.
Trzy ostatnie polecenia każdy z nich dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.
Identyfikator URI każdego dysku jest przechowywany w $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.

### Przykład 2: Dodawanie dysku danych do istniejącej maszyny wirtualnej
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .
Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.
Drugie polecenie dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.

### Przykład 3: Dodawanie dysku danych do nowej maszyny wirtualnej z ogólnego obrazu użytkownika
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Następne dwa polecenia umożliwiają przypisanie ścieżek do obrazów danych i dysków z danymi odpowiednio do $DataImageUri i $DataDiskUri zmiennych.
Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.
Ostatnie polecenia dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.

### Przykład 4: Dodawanie dysków z danymi do nowej maszyny wirtualnej z obrazu specjalistycznego użytkownika
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Następne polecenia przypisują ścieżki do $DataDiskUri zmiennej.
Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.
Polecenie ostatnie Dodaj dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.

## PARAMETRÓW

### -Buforowanie
Określa tryb buforowania dysku.
Dopuszczalne wartości tego parametru to:
- Odczytu
- ReadWrite
- Żadna wartość domyślna to ReadWrite.
Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.
To ustawienie wpływa na spójność i wydajność dysku.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Opcja
Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.
Dopuszczalne wartości tego parametru to:
- Ponowne.
Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.
Po określeniu tej opcji nie określaj parametru *SourceImageUri* .
*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD), który ma zostać dołączony jako dysk danych do maszyny wirtualnej.
- Wolnego.
Określ, czy chcesz utworzyć pusty dysk danych.
- FromImage.
Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie uogólnionego obrazu lub dysku.
Po określeniu tej opcji należy określić również parametr *SourceImageUri* , aby wskazać platformę Azure lokalizację dysku VHD, który ma zostać dołączony jako dysk danych.
Parametr *VhdUri* jest wykorzystywany jako lokalizacja identyfikująca lokalizację, w której dysk VHD z danymi będzie przechowywany, gdy jest on wykorzystywany przez maszynę wirtualną.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DiskEncryptionSetId
Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.  Ten parametr może być określony tylko dla dysków zarządzanych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Określa rozmiar, w gigabajtach, pustego dysku, który ma zostać dołączony do maszyny wirtualnej.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Określa logiczny numer jednostki (LUN) dla dysku danych.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Określa identyfikator dysku zarządzanego.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę dysku danych, który ma zostać dodany.

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

### -SourceImageUri
Określa źródłowy identyfikator URI dysku, który jest dołączony do tego polecenia cmdlet.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Określa typ konta magazynu zarządzanego.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Określa identyfikator URI (Uniform Resource Identifier) pliku wirtualnego dysku twardego (VHD), który ma zostać utworzony po użyciu obrazu platformy lub obrazu użytkownika.
To polecenie cmdlet umożliwia skopiowanie do tej lokalizacji dużego obiektu (BLOB) w formacie binarnym.
To jest lokalizacja, z której ma zostać uruchomiona maszyna wirtualna.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa lokalny obiekt maszyny wirtualnej, do którego ma zostać dodany dysk danych.
Aby uzyskać obiekt maszyny wirtualnej, można użyć polecenia cmdlet **Get-AzVM** .
Za pomocą polecenia cmdlet **New-AzVMConfig** można utworzyć obiekt maszyny wirtualnej.

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

### -WriteAccelerator
Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

### System. String

### Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes

### System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[Nowe — AzVMConfig](./New-AzVMConfig.md)
