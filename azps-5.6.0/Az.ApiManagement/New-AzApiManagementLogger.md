---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: e704be2fba35ab52ff8fd0be7d5fba7870dc7774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988534"
---
# New-AzApiManagementLogger

## SYNOPSIS
Tworzy Loglogię zarządzania interfejsem API.

## SKŁADNIA

### EventHubHubSet (domyślne)
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationInsights Jednakset
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzApiManagementLog tworzy** **Loglog** usługi Azure API Management.

## PRZYKŁADY

### Przykład 1. Tworzenie rejestratora
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

To polecenie tworzy loger o nazwie ContosoSdkEventHub przy użyciu określonych parametrów połączenia.

### Przykład 2

Tworzy Loglogię zarządzania interfejsem API. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementLogger -Context <PsApiManagementContext> -InstrumentationKey <String> -LoggerId 'Logger123'
```

## PARAMETERS

### - ConnectionString
Określa parametrów połączenia usługi Azure Event Hubs, które zaczynają się od następujących parametrów: `Endpoint=endpoint and key from Azure classic portal`
Klucz z prawami do wysyłania w ciągach połączenia musi być skonfigurowany.

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — kontekst
Określa obiekt **PsApiManagementContext.**

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

### — Opis
Określa opis.

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

### -InstrumentationKey
Klucz instrumentacji aplikacji Insights. Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - IsBuffered
Określa, czy rekordy w rejestratorze są buforowane przed opublikowaniem.
Wartość domyślna to $True.
Gdy rekordy są buforowane, są wysyłane do Centrum zdarzeń co 15 sekund lub zawsze, gdy bufor otrzymuje 256 KB wiadomości.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogId
Określa identyfikator loglogii.
Jeśli nie określisz identyfikatora, to polecenie cmdlet go wygeneruje.

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

### — Nazwa
Określa nazwę jednostki centrum zdarzeń z klasycznego portalu Azure.

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagement Jednakowy

## NOTATKI

## LINKI POKREWNE

[Get-AzApiManagement Jednakowy](./Get-AzApiManagementLogger.md)

[Remove-AzApiManagement Jednakowy](./Remove-AzApiManagementLogger.md)

[Set-AzApiManagement Jednakowy](./Set-AzApiManagementLogger.md)


