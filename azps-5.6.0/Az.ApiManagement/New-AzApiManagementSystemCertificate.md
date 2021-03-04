---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: cc3cc5d0e7ae617fc745c2f119f7da9df88417a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959194"
---
# New-AzApiManagementSystemCertificate

## SYNOPSIS
Tworzy `PsApiManagementSystemCertificate` wystąpienie. Certyfikat może zostać wystawiony przez prywatny urząd certyfikacji i zainstalowany w usłudze zarządzania interfejsami API do `CertificateAuthority` magazynu lub do `Root` magazynu.

## SKŁADNIA

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **New-AzApiManagementSystemCertificate** to polecenie pomocnika, które tworzy wystąpienie **polecenia PsApiManagementSystemCertificate.**
To polecenie jest używane z poleceniem cmdlet New-AzApiManagement i Set-AzApiManagement cmdlet.

## PRZYKŁADY

### Przykład 1. Tworzenie i inicjowanie wystąpienia pliku PsApiManagementSystemCertificate przy użyciu certyfikatu SSL z pliku
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

To polecenie tworzy i inicjuje wystąpienie narzędzia **PsApiManagementSystemCertificate** z certyfikatem głównego urzędu certyfikacji. Następnie tworzy usługę zarządzania interfejsami API, która instaluje certyfikat certyfikacji w sklepie głównym.

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

### -PfxPassword
Hasło do pliku certyfikatu pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - PfxPath
Ścieżka do pliku certyfikatu pfx.

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

### -StoreName
Nazwa magazynu certyfikatów

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Security.SecureString

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate

## NOTATKI

## LINKI POKREWNE

[New-AzApiManagement](./New-AzApiManagement.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)