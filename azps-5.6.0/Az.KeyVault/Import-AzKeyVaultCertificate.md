---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 507bcce6607566c733ee4cd52f72f7e7910ac90f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001409"
---
# Import-AzKeyVaultCertificate

## SYNOPSIS
Importuje certyfikat do magazynu kluczy.

## SKŁADNIA

### ImportCertificateFromFile (domyślne)
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ImportWithPrivateKeyFromString
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ImportWithPrivateKeyFromCollection
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Import-AzKeyVaultCertificate** importuje certyfikat do magazynu kluczy.
Certyfikat można utworzyć do zaimportowania przy użyciu jednej z następujących metod:
- Umożliwia `Add-AzKeyVaultCertificate` utworzenie żądania podpisania certyfikatu i przesłanie go do urzędu certyfikacji. Zobacz https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request
- Użyj istniejącego pliku pakietu certyfikatu, takiego jak pfx lub p12, który zawiera zarówno certyfikat, jak i klucz prywatny.

## PRZYKŁADY

### Przykład 1. Importowanie certyfikatu magazynu kluczy
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

Pierwsze polecenie tworzy bezpieczne ConvertTo-SecureString cmdlet, a następnie zapisuje je w $Password danych.
Drugie polecenie importuje certyfikat o nazwie ImportCert01 do magazynu kluczy cosotosoKV01.

## PARAMETERS

### -CertificateCollection
Określa kolekcję certyfikatów do dodania do magazynu kluczy.

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificateString
Określa ciąg certyfikatu.

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### - FilePath
Określa ścieżkę pliku certyfikatu, który zostanie importowany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę certyfikatu. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu z nazwy magazynu kluczy, obecnie wybranego środowiska i nazwy certyfikatu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Hasło
Określa hasło dla pliku certyfikatu.

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Określa nazwę magazynu klucza, do którego to polecenie cmdlet importuje certyfikaty.
To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.

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

### System.Security.Cryptography.X509Certificates.X509Certificate2Collection

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate

## NOTATKI

## LINKI POKREWNE

[Remove-AzKeyVaultCertificate](./Remove-AzKeyVaultCertificate.md)

[Tworzenie i scalanie obsługi klienta w magazynie kluczy](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request)