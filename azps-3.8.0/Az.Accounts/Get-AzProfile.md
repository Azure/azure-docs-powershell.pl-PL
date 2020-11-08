---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051981"
---
# Get-AzProfile

## STRESZCZENIe
Pobierz profile usług obsługiwane przez zainstalowane moduły.

## POLECENIA

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## Opis
Pobierz profile usług obsługiwane przez zainstalowane moduły.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

Uzyskiwanie profilu usługi obsługiwanego przez moduł magazynu

## PARAMETRÓW

### -ListAvailable
Lista wszystkich profilów usługi obsługiwanych przez zainstalowane moduły

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModuleName
Nazwa modułu do sprawdzenia

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile

## INFORMACYJN

## LINKI POKREWNE
