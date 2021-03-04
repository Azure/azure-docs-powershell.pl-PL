---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969505"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Dodaje dysk danych do maszyny wirtualnej maszyny wirtualnej.

## SKŁADNIA

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet AzVmssVMDataData Add-AzVmssVMDataData Umożliwia** dodanie dysku danych do maszyny wirtualnej maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Dodawanie zarządzanego dysku danych do maszyny wirtualnej maszyny wirtualnej.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Pierwsze polecenie otrzymuje istniejący dysk zarządzany.
Następne polecenie pobiera istniejącą maszynę wirtualnej maszyny wirtualnej, która jest podana przez nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.
Następne polecenie dodaje dysk zarządzany do maszyny wirtualnej maszyny wirtualnej przechowywanej lokalnie w $VmssVM.
Końcowe polecenie aktualizuje maszynę wirtualnej maszyny wirtualnej o dodany dysk danych.

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
Position: Named
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
Position: 2
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
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Logicznej
Określa numer jednostki logicznej (OWĄ) dla dysku danych.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Managed Jednakid
Określa identyfikator dysku zarządzanego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Określa typ konta magazynu zarządzanego dysku.

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

### -VirtualMachineScaleSetVM
Określa lokalny obiekt skalowania maszyny wirtualnej, do którego ma być dodać dysk danych.
Możesz użyć polecenia cmdlet **Get-AzVmssVM,** aby uzyskać obiekt ZESTAWU SKALA MASZYNY WIRTUALNEJ.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - WriteAccelerator
Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na zarządzanym dysku danych.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTATKI

## LINKI POKREWNE
