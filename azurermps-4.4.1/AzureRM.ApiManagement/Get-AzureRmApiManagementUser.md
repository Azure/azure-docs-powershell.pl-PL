---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525797"
---
# Get-AzureRmApiManagementUser

## STRESZCZENIe
Pobiera użytkownika lub użytkowników.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Pobierz wszystkich użytkowników (domyślnie)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Uzyskaj użytkownika według identyfikatora
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Znajdowanie użytkowników
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.

## Przykłady

### Przykład 1: Pobierz wszystkich użytkowników
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

To polecenie pobiera wszystkich użytkowników.

### Przykład 2: Uzyskaj użytkownika według identyfikatora
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

To polecenie pobiera użytkownika według identyfikatora.

### Przykład: pobieranie użytkowników według nazwisk
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

To polecenie umożliwia użytkownikom, których imiona i nazwiska są określone przez użytkownika.

### Przykład 4: Uzyskaj użytkownikowi na podstawie adresu e-mail
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

To polecenie uzyskuje użytkownika o określonym adresie e-mail.

### Przykład 5: uzyskiwanie wszystkich użytkowników w grupie
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

To polecenie pobiera wszystkich użytkowników w określonej grupie.

## PARAMETRÓW

### -Context
Określa wystąpienie **PsApiManagementContext**.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Mail
Określa adres e-mail użytkownika.
Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika pocztą e-mail.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirstName
Określa Imię użytkownika.
Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika według imienia i nazwiska.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupId
Określa identyfikator grupy.
Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie wszystkich użytkowników w określonej grupie.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Określa nazwisko użytkownika.
Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje użytkowników według nazwiska.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Określa stan użytkownika.
Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie użytkowników w tym stanie.
Ten parametr jest opcjonalny.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Określa identyfikator użytkownika.
Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie użytkownika przy użyciu tego identyfikatora.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
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

### IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementUser>

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmApiManagementUser](./New-AzureRmApiManagementUser.md)

[Remove-AzureRmApiManagementUser](./Remove-AzureRmApiManagementUser.md)

[Set-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)


