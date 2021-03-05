---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: e72729b1721fb31ca2ce3a52d33f0295c55bb537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001370"
---
# New-AzKeyVaultCertificateAdministratorDetail

## SYNOPSIS
Tworzy obiekt szczegółów administratora certyfikatu w pamięci.

## SKŁADNIA

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzKeyVaultCertificateAdministratorDetail** tworzy obiekt szczegółów administratora certyfikatu w pamięci.

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu szczegółów administratora certyfikatu
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

To polecenie tworzy obiekt szczegółów administratora certyfikatu w pamięci, a następnie zapisuje go w $AdminDetails danych.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -EmailAddress
Określa adres e-mail administratora certyfikatu.

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

### -FirstName
Określa pierwszą nazwę administratora certyfikatu.

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

### -LastName
Określa nazwisko administratora certyfikatu.

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

### -PhoneNumber
Określa numer telefonu administratora certyfikatu.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails

## NOTATKI

## LINKI POKREWNE

[New-AzKeyVaultCertificateOrganizationDetail](./New-AzKeyVaultCertificateOrganizationDetail.md)

