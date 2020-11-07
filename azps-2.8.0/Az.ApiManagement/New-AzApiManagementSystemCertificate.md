---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 834a713e5fb7cc6bfcf24244bbb376eb0f01a8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706986"
---
# New-AzApiManagementSystemCertificate

## STRESZCZENIe
Tworzy wystąpienie `PsApiManagementSystemCertificate` . Certyfikat może zostać wystawiony przez prywatny urząd certyfikacji i zostanie zainstalowany w usłudze zarządzania interfejsem API `CertificateAuthority` lub w `Root` sklepie.

## POLECENIA

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzApiManagementSystemCertificate** jest poleceniem pomagającym, które tworzy wystąpienie **PsApiManagementSystemCertificate**.
To polecenie jest używane w przypadku polecenia cmdlet New-AzApiManagement i Set-AzApiManagement.

## Przykłady

### Przykład 1: Tworzenie i Inicjowanie wystąpienia PsApiManagementSystemCertificate przy użyciu certyfikatu SSL z pliku
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementSystemCertificate** przy użyciu certyfikatu głównego urzędu certyfikacji. Następnie tworzy i usługa zarządzania interfejsem API, która instaluje certyfikat urzędu certyfikacji w magazynie głównym.

## PARAMETRÓW

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

### -PfxPassword
Hasło do pliku certyfikatu PFX.

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

### -PfxPath
Ścieżka do pliku certyfikatu PFX.

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

### -Pole NazwaSklepu
Certyfikat pole NazwaSklepu

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Security. SecureString

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzApiManagement](./New-AzApiManagement.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)