---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197059"
---
# New-AzBatchCertificate

## SYNOPSIS
Dodaje certyfikat do określonego konta usługi Batch.

## SKŁADNIA

### Plik (domyślny)
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RawData
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzBatchCertificate** dodaje certyfikat do określonego konta usługi Azure Batch.

## PRZYKŁADY

### Przykład 1. Dodawanie certyfikatu z pliku
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

To polecenie dodaje certyfikat do określonego konta usługi Batch, używając pliku E:\Certificates\MyCert.cer.

### Przykład 2. Dodawanie certyfikatu z nieprzetworzonych danych
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

Pierwsze polecenie odczytuje dane z pliku o nazwie MyCert.pfx do zmiennej $RawData danych.
Drugie polecenie powoduje dodanie certyfikatu do określonego konta usługi Batch przy użyciu nieprzetworzonych danych przechowywanych w $RawData.

## PARAMETERS

### - BatchContext
Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.
Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory. Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu. Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany. Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### - FilePath
Określa ścieżkę pliku certyfikatu.
Plik certyfikatu musi mieć format cer lub pfx.

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Rodzaj
Rodzaj certyfikatu do utworzenia. Jeśli nie zostanie to określone, przyjmuje się, że wszystkie certyfikaty bez hasła są certyfikatem CER, a wszystkie certyfikaty z hasłem są pfx.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Hasło
Określa hasło dostępu do klucza prywatnego certyfikatu.
Ten parametr należy określić, jeśli zostanie określony certyfikat w formacie pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - RawData
Określa nieprzetworzone dane certyfikatu w formacie cer lub pfx.

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.Byte[]

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchCertificate](./Get-AzBatchCertificate.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Remove-AzBatchCertificate](./Remove-AzBatchCertificate.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
