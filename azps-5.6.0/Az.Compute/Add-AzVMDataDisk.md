---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 685a1768dac652b3981bd081a2f8b29997c08639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981162"
---
# Add-AzVMDataDisk

## SYNOPSIS
Dodaje dysk danych do maszyny wirtualnej.

## SKŁADNIA

### VmNormalMeterParameterSetName (domyślna)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedMeterParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVMDataData Umożliwia** dodanie dysku danych do maszyny wirtualnej.
Możesz dodać dysk danych podczas tworzenia maszyny wirtualnej lub dodać dysk danych do istniejącej maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Dodawanie dysków danych do nowej maszyny wirtualnej
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Następne trzy polecenia przypiszą ścieżki trzech dysków danych do zmiennych $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.
Ta metoda ma na celu tylko czytelność następujących poleceń.
Ostatnie trzy polecenia każdego z nich dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.
URI każdego dysku jest przechowywany w $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.

### Przykład 2. Dodawanie dysku danych do istniejącej maszyny wirtualnej
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)
Polecenie przechowuje maszynę wirtualną w $VirtualMachine zmienną.
Drugie polecenie powoduje dodanie dysku danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
Ostatnie polecenie aktualizuje stan maszyny wirtualnej przechowywanej w u $VirtualMachine ResourceGroup11.

### Przykład 3. Dodawanie dysku danych do nowej maszyny wirtualnej z ogólnego obrazu użytkownika
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Następne dwa polecenia przypiszą ścieżki obrazu danych i dyskryminowania danych do $DataImageUri i $DataDiskUri zmiennych.
Ta metoda ma na celu poprawę czytelności następujących poleceń.
Końcowe polecenia dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.

### Przykład 4. Dodawanie dyskerów danych do nowej maszyny wirtualnej z specjalistycznego obrazu użytkownika
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Następne polecenia przypisze ścieżki dysku danych do zmiennej $DataDiskUri danych.
Ta metoda ma na celu poprawę czytelności następujących poleceń.
Ostatnie polecenie dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.

## PARAMETERS

### — buforowanie
Określa tryb buforowania dysku.
Dopuszczalne wartości dla tego parametru to:
- ReadOnly
- ReadWrite
- Brak Wartość domyślna to ReadWrite.
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

### — CreateOption
Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.
Dopuszczalne wartości dla tego parametru to:
- Dołączanie.
Określ tę opcję, aby utworzyć maszynę wirtualną na dysku specjalistycznym.
Po określeniu tej opcji nie należy określać *parametru SourceImageUri.*
*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD) w celu dołączenia go jako dysku danych do maszyny wirtualnej.
- Puste.
Określ tę wartość, aby utworzyć pusty dysk danych.
- FromImage.
Określ tę opcję, aby utworzyć maszynę wirtualną na dysku lub obrazie ogólnym.
Podczas określania tej opcji musisz określić parametr *SourceImageUri,* aby wskazać platformie Azure lokalizację pliku VHD do dołączenia jako dysku danych.
Parametr *VhdUri* jest używany jako lokalizacja identyfikująca miejsce przechowywania dysku danych VHD, gdy będzie używany przez maszynę wirtualną.

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

### -DiskEncryptionSetId
Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.  Tę wartość można określić tylko dla dysku zarządzanego.

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
Określa w gigabajtach rozmiar pustego dysku do dołączenia do maszyny wirtualnej.

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

### -Logicznej
Określa numer jednostki logicznej (OWĄ) dla dysku danych.

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

### -Managed Jednakid
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

### — Nazwa
Określa nazwę dysku danych do dodania.

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
Określa źródłowy URI dysku, który jest dołączany przez to polecenie cmdlet.

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
Określa typ konta magazynu zarządzanego dysku.

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

### - VhdUri
Określa identyfikator URI dla pliku wirtualnego dysku twardego (VHD) do utworzenia w przypadku użycia obrazu platformy lub obrazu użytkownika.
To polecenie cmdlet kopiuje do tej lokalizacji duży obiekt (blob) obrazu.
Jest to lokalizacja, z której należy uruchomić maszynę wirtualną.

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

### — MASZYNY WIRTUALNEJ
Określa lokalny obiekt maszyny wirtualnej, do którego ma być dodać dysk danych.
Aby uzyskać obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet **Get-AzVM.**
Aby utworzyć obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet **New-AzVMConfig.**

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

### - WriteAccelerator
Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na zarządzanym dysku danych.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTATKI

## LINKI POKREWNE

[Remove-AzVMDataData](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
