---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: 6f10af70b5f45a4ff1441ea43837753163a0d6ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502423"
---
# New-AzApiManagementCertificate

## STRESZCZENIe
Tworzy certyfikat zarządzania interfejsem API do użycia podczas uwierzytelniania z zapleczem wewnętrznym.

## POLECENIA

### LoadFromFile (domyślny)
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Nowego
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzApiManagementCertificate** tworzy certyfikat zarządzania interfejsem Azure API.

## Przykłady

### Przykład 1. Tworzenie i przekazywanie certyfikatu
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

To polecenie przekazuje certyfikat do zarządzania interfejsem API. Tego certyfikatu można używać do wzajemnego uwierzytelniania z zapleczem przy użyciu zasad.

### Przykład 2

Tworzy certyfikat zarządzania interfejsem API do użycia podczas uwierzytelniania z zapleczem wewnętrznym. (autogenerowana)

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementCertificate -CertificateId '0123456789' -Context <PsApiManagementContext> -PfxFilePath 'C:\contoso\certificates\apimanagement.pfx' -PfxPassword '1111'
```

## PARAMETRÓW

### -CertificateId
Określa identyfikator certyfikatu, który ma zostać utworzony.
Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.

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

### -Context
Określa obiekt **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -PfxBytes
Określa tablicę bajtów pliku certyfikatu w formacie PFX.
Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxFilePath
Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.
Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPassword
Określa hasło dla certyfikatu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext

### System. String

### System. Byte []

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate

## INFORMACYJN

## LINKI POKREWNE

[Get-AzApiManagementCertificate](./Get-AzApiManagementCertificate.md)

[Remove-AzApiManagementCertificate](./Remove-AzApiManagementCertificate.md)

[Set-AzApiManagementCertificate](./Set-AzApiManagementCertificate.md)


