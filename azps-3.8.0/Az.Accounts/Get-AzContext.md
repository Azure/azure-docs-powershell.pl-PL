---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051988"
---
# Get-AzContext

## STRESZCZENIe
Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.

## POLECENIA

### GetSingleContext (domyślny)
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### ListAllContexts
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzContext pobiera bieżące metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.
To polecenie cmdlet umożliwia pobieranie konta usługi Active Directory, dzierżawy usługi Active Directory, subskrypcji platformy Azure i ukierunkowanego środowiska platformy Azure.
Polecenia cmdlet usługi Azure Resource Manager domyślnie wykorzystują te ustawienia podczas przeprowadzania żądań Menedżera zasobów platformy Azure.

## Przykłady

### Przykład 1. Uzyskiwanie bieżącego kontekstu
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

W tym przykładzie rejestrujemy się na naszym koncie za pomocą abonamentu na platformie Azure za pomocą funkcji Connect-AzAccount, a następnie uzyskujemy kontekst bieżącej sesji przez nawiązanie połączenia Get-AzContext.

### Przykład 2: wyświetlanie wszystkich dostępnych kontekstów
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

W tym przykładzie są wyświetlane wszystkie obecnie dostępne konteksty.  Użytkownik może wybrać jedno z tych kontekstów przy użyciu polecenia SELECT-AzContext.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure

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

### -ListAvailable
Wyświetlanie wszystkich dostępnych kontekstów w bieżącej sesji.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa kontekstu

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. profile. Core. PSAzureContext

## INFORMACYJN

## LINKI POKREWNE

[Set-AzContext](./Set-AzContext.md)

