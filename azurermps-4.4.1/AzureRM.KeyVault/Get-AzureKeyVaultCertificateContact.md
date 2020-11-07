---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718530"
---
# Get-AzureKeyVaultCertificateContact

## STRESZCZENIe
Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.

## Przykłady

### Przykład 1: pobieranie wszystkich kontaktów z certyfikatem
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.

## PARAMETRÓW

### -Magazynname
Określa nazwę magazynu kluczy.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Lista<Microsoft. Azure. Commands.. models. KeyVaultCertificateContact>

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureKeyVaultCertificateContact](./Add-AzureKeyVaultCertificateContact.md)

[Remove-AzureKeyVaultCertificateContact](./Remove-AzureKeyVaultCertificateContact.md)

