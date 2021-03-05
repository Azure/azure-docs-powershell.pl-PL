---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980202"
---
# Get-AzActivityLog

## SYNOPSIS
Pobieranie zdarzeń dziennika aktywności.

## SKŁADNIA

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Get-AzActivityLog pobiera zdarzenia dziennika aktywności. Zdarzenia mogą być skojarzone z bieżącym identyfikatorem subskrypcji, identyfikatorem korelacji, grupą zasobów, identyfikatorem zasobu lub dostawcą zasobów.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji
```
PS C:\>Get-AzActivityLog
```

To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 2. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 3. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce w dniu lub po 06-06-01T10:30 czasu lokalnego, jeśli ta data/godzina nie jest starsza niż 90 dni od bieżącej daty/godziny.

### Przykład 4. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia i zakończenia.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

To polecenie wyświetla co najwyżej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce w czasie lokalnym 2017-04-01T10:30 i przed godziną 2017-04-14T11:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, czyli okresu przechowywania.

### Przykład 5. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

To polecenie wyszczególnia co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, który miał miejsce 7 dni od bieżącej daty/godziny. 
**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.

### Przykład 6. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

To polecenie wyszczególnia co najwyżej 100 zdarzeń skojarzonych z określonym identyfikatorem korelacji, które miały miejsce 7 dni od bieżącej daty/godziny. 
**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.

### Przykład 7. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji i godziny rozpoczęcia
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.
**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.

### Przykład 8. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji z godziną rozpoczęcia i zakończenia
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

To polecenie wyszczególnia co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, który miał miejsce w czasie lokalnym 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30 czasu lokalnego, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.

### Przykład 9. Uzyskiwanie dziennika zdarzeń dla grupy zasobów
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

To polecenie zawiera najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 10. Uzyskiwanie dziennika zdarzeń dla grupy zasobów z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

To polecenie wyświetla listę co najwyżej 100 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 11. Uzyskiwanie dziennika zdarzeń dla grupy zasobów według czasu rozpoczęcia
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.

### Przykład 12. Uzyskiwanie dziennika zdarzeń dla grupy zasobów z godziną rozpoczęcia i zakończenia
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w czasie lokalnym w godzinach 2017–04–15T04:30, ale przed godziną 2017-04-25T12:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.

### Przykład 13. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

To polecenie wyświetla listę co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 14. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 15. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.

### Przykład 16. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia i godziną zakończenia
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce w czasie lokalnym w godzinach 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30 czasu lokalnego, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.

### Przykład 17. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 18. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 19. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z godziną rozpoczęcia
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.

### Przykład 20. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z godziną rozpoczęcia i zakończenia
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce w czasie lokalnym w godzinach 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.

## PARAMETERS

### — wywołujący
Wywołujący zdarzenia do pobrania

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

### -CorrelationId
Identyfikator korelacji

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DetailedOutput
Zwróć obiekt ze wszystkimi szczegółami zdarzeń (domyślnie są zwracane tylko niektóre atrybuty, czyli bez szczegółów)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - EndTime
Czas zakończenia kwerendy

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - MaxRecord
Maksymalna liczba rekordów do pobrania.
Alias: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
The ResourceId

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Nazwa zasobuProvider

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — StartTime
Identyfikator korelacji zapytania

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Status
Stan zdarzeń do pobrania

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameters

### System.Int32

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## NOTATKI

## LINKI POKREWNE
