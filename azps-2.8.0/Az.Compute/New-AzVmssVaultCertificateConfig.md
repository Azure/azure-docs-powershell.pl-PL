---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0afd599bd1af9b3f597e9753d1be1e8ae710e5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706308"
---
# New-AzVmssVaultCertificateConfig

## STRESZCZENIe
Umożliwia utworzenie konfiguracji certyfikatu magazynu kluczy.

## POLECENIA

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzVmssVaultCertificateConfig** określa klucz tajny, który należy umieścić na maszynach wirtualnych zestawu skali maszyny wirtualnej (VMSS).
Dane wyjściowe tego polecenia cmdlet są przeznaczone do użycia z poleceniem cmdlet Add-AzVmssSecret.

## Przykłady

### Przykład 1: Tworzenie konfiguracji certyfikatu magazynu kluczy
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

To polecenie powoduje utworzenie konfiguracji certyfikatu magazynu kluczy, w której jest używany magazyn certyfikatów o nazwie Moje certyfikaty znajdujący się pod określonym adresem URL certyfikatu.

## PARAMETRÓW

### -CertificateStore
Określa magazyn certyfikatów na maszynach wirtualnych w zestawie skali, w którym jest dodawany certyfikat.
Jest to prawidłowe tylko w przypadku zestawów skali maszyny wirtualnej systemu Windows.

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

### -CertificateUrl
Określa identyfikator URI certyfikatu przechowywanego w magazynie kluczy.
Jest to kodowanie Base64 następującego obiektu JSON, który jest zakodowany w formacie UTF-8: {"dane": " \< Unbased-Encoded-Certificate \> ", "DataType": "PFX", "Password": "PFX \< -File-Password \> "}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Management. COMPUTE. MODELES. VaultCertificate

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzVmssSecret](./Add-AzVmssSecret.md)
