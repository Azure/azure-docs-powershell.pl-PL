---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200995"
---
# New-AzAutomationWebhook

## SYNOPSIS
Tworzy element webhook dla podręcznika uruchamiania automatyzacji.

## SKŁADNIA

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzAutomationWebhook** tworzy witrynę webhook dla podręcznika azure Automation.
Pamiętaj, aby zapisać adres URL webhook, który zwraca to polecenie cmdlet, ponieważ nie można go odzyskać ponownie.

## PRZYKŁADY

### Przykład 1. Tworzenie witryny sieci Web
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

To polecenie tworzy dla podręcznika o nazwie ContosoRunbook webhook o nazwie Webhook06 na koncie automatyzacji o nazwie AutomationAccount01.
Polecenie przechowuje webhook w $Webhook zmienną.
Webhook jest włączony.
Webhook wygasa w określonym czasie.
To polecenie nie zawiera żadnych wartości parametrów webhook.
To polecenie określa *parametr Force.*
Dlatego nie jest wyświetlany monit o potwierdzenie.

### Przykład 2. Tworzenie webhooku z parametrami
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Pierwsze polecenie tworzy słownik parametrów i zapisuje je w $Params zmienną.
Drugie polecenie tworzy webhook Webhook o nazwie Webhook11 dla podręcznika o nazwie ContosoRunbook w koncie automatyzacji o nazwie AutomationAccount01.
To polecenie przypisuje parametry w $Params sieci Web.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, na którym to polecenie cmdlet tworzy element webhook.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -ExpiryTime
Określa czas wygaśnięcia obiektu **DateTimeOffset** dla sieci Web.
Możesz określić ciąg lub wartość **datetime,** która może zostać przekonwertowana na prawidłowy **dateTimeOffset.**

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wymuszanie
ps_force

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

### -IsEnabled
Określa, czy sieć Webhook jest włączona.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę sieci Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Parametry
Określa słownik par klucz/wartość.
Klucze to nazwy parametrów podręcznika obsługi.
Wartości są wartościami parametrów podręcznika uruchamiania.
Po uruchomieniu podręcznika w odpowiedzi na witrynę internetową te parametry są przekazywane do tego podręcznika.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy witrynę webhook.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunbookName
Określa nazwę podręcznika do skojarzenia z siecią Webhook.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - RunOn
Opcjonalna nazwa grupy pracowników hybrydowych, która powinna wykonywać podręcznik

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.Boolean

### System.DateTimeOffset

## OUTPUTS

### Microsoft.Azure.Commands.Automation.Model.Webhook

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationWebhook](./Get-AzAutomationWebhook.md)

[Remove-AzAutomationWebhook](./Remove-AzAutomationWebhook.md)

[Set-AzAutomationWebhook](./Set-AzAutomationWebhook.md)


