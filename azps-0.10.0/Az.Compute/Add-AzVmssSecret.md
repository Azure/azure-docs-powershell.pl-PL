---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 908810f658cdd4083bd24356eaab4e52d4dd5158
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395122"
---
# Add-AzVmssSecret

## STRESZCZENIe
Dodaje klucz tajny do VMSS.

## POLECENIA

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVmssSecret** umożliwia dodanie klucza tajnego do zestawu skali maszyny wirtualnej (VMSS).
Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.
Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz [co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](/powershell/module/az.keyvault) lub polecenia cmdlet [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .

## Przykłady

### Przykład 1. Dodaj klucz tajny do VMSS
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

W tym przykładzie jest dodawany klucz tajny do VMSS.
W pierwszym poleceniu użyto polecenia cmdlet Get-AzKeyVault, aby uzyskać tajemnicę magazynu z magazynu o nazwie ContosoVault i przechowywać wynik w zmiennej o nazwie $Vault.
W drugim poleceniu użyto polecenia cmdlet **New-AzVmssVaultCertificateConfig** w celu utworzenia konfiguracji certyfikatu magazynu kluczy przy użyciu określonego adresu URL certyfikatu z magazynu certyfikatów o nazwie Certificates i zapisanie wyników w zmiennej o nazwie $CertConfig.
W trzecim poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.
Czwarte polecenie dodaje klucz tajny do VMSS przy użyciu klucza tajnego magazynu przy użyciu identyfikatora zasobu kluczy oraz certyfikatu magazynu przechowywanego w $Vault i $CertConfig zmiennych.

## PARAMETRÓW

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

### -SourceVaultId
Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.
Ta wartość działa także jako klucz do dodawania wielu certyfikatów.
Oznacza to, że w przypadku dodawania wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości parametru *SourceVaultId* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultCertificate
Określa obiekt **certyfikatu** magazynu zawierający adres URL i nazwę certyfikatu certyfikatu.
Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) .

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt VMSS.
Aby utworzyć ten obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### VirtualMachineScaleSet
Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu

## WYSYŁA

### Znaleziono
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[Nowe — AzVmssConfig](./New-AzVmssConfig.md)
