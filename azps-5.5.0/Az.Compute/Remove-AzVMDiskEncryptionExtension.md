---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177547"
---
# Remove-AzVMDiskEncryptionExtension

## SYNOPSIS
Usuwa rozszerzenie szyfrowania dysku z maszyny wirtualnej.

## SKŁADNIA

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzVMCryptionExtension** usuwa rozszerzenie szyfrowania dysku i skojarzoną konfigurację rozszerzenia z maszyny wirtualnej. Jeśli nie zostanie określona nazwa rozszerzenia, to polecenie cmdlet usunie rozszerzenie o nazwie domyślnej Azure JakSzyfrowanieNaszycji dla maszyn wirtualnych, na których działa system operacyjny Windows, lub polecenie AzureCryptionForLinux dla maszyn wirtualnych opartych na systemie Linux. 

To polecenie cmdlet nie powiedzie się, jeśli szyfrowanie na maszyny wirtualnej nie zostało najpierw wyłączone.  Aby wyłączyć szyfrowanie na komputerze wirtualnym, [użyj szyfrowania Disable-AzVMCryption.](./Disable-AzVMDiskEncryption.md) 

## PRZYKŁADY

### Przykład 1. Usunięcie rozszerzenia szyfrowania dysku z maszyny wirtualnej.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

To polecenie usuwa rozszerzenie o nazwie domyślnej Azure Chromecryption dla maszyny wirtualnej z systemem operacyjnym Windows lub z maszyną wirtualną o nazwie MyTestVM opartą na systemie Linux.

### Przykład 2. Usunięcie z maszyny wirtualnej konkretnego rozszerzenia szyfrowania dysku.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

To polecenie usuwa rozszerzenie szyfrowania o nazwie MyCryptEncryptionExtension z maszyny wirtualnej o nazwie MyTestVM.

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

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.

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

### — Nazwa
Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.
Polecenie cmdlet Set-AzVMDiskEncryptionExtension ustawia tę nazwę na AzureDriveEncryption dla maszyn wirtualnych, na których działa system operacyjny Windows, oraz polecenie AzureUxEncryptionForLinux dla maszyn wirtualnych systemu Linux.
Określ ten parametr tylko w przypadku zmiany domyślnej nazwy w cmdlet **Set-AzVMCryptionExtension** lub użycia innej nazwy zasobu w szablonie Menedżer zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem. Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.

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

### -ResourceGroupName
Określa nazwę grupy zasobów dla maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTATKI

## LINKI POKREWNE

[Get-AzVM GdyszytEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Set-AzVM GdyszytEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


