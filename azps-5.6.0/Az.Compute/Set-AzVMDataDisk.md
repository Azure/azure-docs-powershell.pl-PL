---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: da4455e7d2630ddb263c56aae96be79fe3cc7a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964986"
---
# Set-AzVMDataDisk

## SYNOPSIS
Modyfikuje właściwości dysku danych maszyny wirtualnej.

## SKŁADNIA

### ChangeWithName
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWith Jednak
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzVMDataData** zmodyfikuje właściwości dysku danych maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Modyfikowanie trybu buforowania dysku danych
```powershell
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzVM.**
Polecenie przechowuje je w $VM zmienną.
Drugie polecenie modyfikuje tryb buforowania dysku danych o nazwie Data Jednak01 na komputerze wirtualnym w $VM.
Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM, które implementuje zmiany.
Zmiana trybu cashingu powoduje ponowne uruchomienie maszyny wirtualnej.

### Przykład 2

Modyfikuje właściwości dysku danych maszyny wirtualnej. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMDataDisk -Caching None -Lun 1 -VM <PSVirtualMachine>
```

## PARAMETERS

### — buforowanie
Określa tryb buforowania dysku.
Dopuszczalne wartości dla tego parametru to:
- ReadOnly
- ReadWrite Wartość domyślna to ReadWrite.
Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.
To ustawienie wpływa na spójność i wydajność dysku.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
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
Określa w gigabajtach rozmiar dysku danych.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Logicznej
Określa numer jednostki logicznej (ZER) dysku danych, który jest zmieniany przez to polecenie cmdlet.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę dysku danych, który ma być zmieniany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Typ konta zarządzanego przez maszynę wirtualną.

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

### — MASZYNY WIRTUALNEJ
Określa maszynę wirtualną, dla której to polecenie cmdlet modyfikuje dysk danych.
Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.

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
Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku danych.

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

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Update-AzVM](./Update-AzVM.md)


