---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: ec07964f62a22385d98c8cd9b8c98ea0b088ec8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969530"
---
# Add-AzVmssSecret

## SYNOPSIS
Dodaje klucz tajny do maszyny wirtualnej.

## SKŁADNIA

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet AzVmssSecret add-AzVmssSecret** dodaje klucz tajny do zestawu skal maszyny wirtualnej (VIRTUAL MACHINE Scale Set, MACHINESS).
Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.
Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [Co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Aby uzyskać więcej informacji o poleceniach cmdlet, zobacz polecenia [cmdlet](/powershell/module/az.keyvault) magazynu kluczy platformy Azure lub polecenie cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## PRZYKŁADY

### Przykład 1. Dodawanie tajemnicy do maszyn wirtualnych
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

W tym przykładzie dodano klucz tajny do usługi maszyny wirtualnej.
Pierwsze polecenie używa Get-AzKeyVault cmdlet w celu uzyskania tajnego magazynu z magazynu o nazwie ContosoVault i przechowuje wynik w zmiennej o nazwie $Vault.
Drugie polecenie używa polecenia cmdlet **New-AzVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu adresu URL określonego certyfikatu z magazynu certyfikatów o nazwie Certyfikaty i przechowuje wyniki w zmiennej o nazwie $CertConfig.
Trzecie polecenie używa polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji maszyny WIRTUALNEJ i przechowuje wynik w zmiennej o nazwie $VMSS.
Czwarte polecenie dodaje klucz tajny do maszyn wirtualnych wirtualnych przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu klucza i certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.

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

### -SourceVaultId
Określa identyfikator zasobu magazynu kluczy zawierający certyfikaty, które można dodać do maszyny wirtualnej.
Ta wartość działa również jako klucz do dodawania wielu certyfikatów.
Oznacza to, że można użyć tej samej wartości parametru *SourceVaultId* podczas dodawania wielu certyfikatów z tego samego magazynu kluczy.

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

### -VaultCertificate
Określa obiekt **certyfikat magazynu** zawierający adres URL certyfikatu i nazwę certyfikatu.
Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssVaultCertificateConfig.](./New-AzVmssVaultCertificateConfig.md)

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.
Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig.](./New-AzVmssConfig.md)

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

### Microsoft.Azure.Management.Compute.Models.VaultCertificate[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)
