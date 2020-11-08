---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: d3706168a23a32d4338069cb593ef8dd71242896
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051206"
---
# New-AzApiManagementHttpMessageDiagnostic

## STRESZCZENIe
Tworzy wystąpienie **PsApiManagementHttpMessageDiagnostic** , które jest ustawieniem diagnostycznym wiadomości HTTP w diagnostyce.

## POLECENIA

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzApiManagementHttpMessageDiagnostic** tworzy ustawienia diagnostyczne wiadomości HTTP.

## Przykłady

### Przykład 1: Tworzenie podstawowego ustawienia diagnostycznego wiadomości http
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

Tworzenie ustawienia diagnostycznego wiadomości HTTP do rejestrowania `Content-Type` i `User-Agent` nagłówków wraz z 100ą bajtów `body`

## PARAMETRÓW

### -BodyBytesToLog
Liczba bajtów treści żądania do zarejestrowania. Ten parametr jest opcjonalny.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -HeadersToLog
Tablica nagłówków, które mają zostać zarejestrowane. Ten parametr jest opcjonalny.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementHttpMessageDiagnostic

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzApiManagementDiagnostic](./New-AzApiManagementDiagnostic.md)

[Nowe — AzApiManagementSamplingSetting](./New-AzApiManagementHttpMessageDiagnostic.md)