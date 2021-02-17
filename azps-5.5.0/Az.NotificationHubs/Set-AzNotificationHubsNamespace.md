---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191490"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Ustawia wartości właściwości przestrzeni nazw centrum powiadomień.

## SKŁADNIA

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzNotificationHubsNamespace** ustawia wartości właściwości istniejącej przestrzeni nazw centrum powiadomień.
Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.
Musisz mieć co najmniej jedną przestrzeń nazw centrum powiadomień.
Ponadto wszystkie centra powiadomień muszą mieć przypisaną przestrzeń nazw.
To polecenie cmdlet służy głównie do włączania i wyłączania przestrzeni nazw.
Gdy przestrzeń nazw jest wyłączona, użytkownicy nie mogą łączyć się z żadnymi centrum powiadomień w przestrzeni nazw ani za pomocą tych centrum nie mogą wysyłać powiadomień wypychanych.
Aby ponownie włączyć wyłączną przestrzeń nazw, użyj tego polecenia cmdlet, aby ustawić właściwość **Województwo** przestrzeni nazw na Wartość aktywna.
To polecenie cmdlet umożliwia również otagowanie przestrzeni nazw jako krytycznej.
Zapobiega to usunięciu przestrzeni nazw.
Aby usunąć krytyczną przestrzeń nazw, należy najpierw usunąć tag Krytyczne.

## PRZYKŁADY

### Przykład 1. Wyłączanie przestrzeni nazw
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

To polecenie wyłącza przestrzeń nazw o nazwie ContosoPartners znajdującą się w centrum danych Stanów Zjednoczonych Zachód i przypisaną do grupy zasobów ContosoNotificationsGroup.

### Przykład 2. Włączanie przestrzeni nazw
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

To polecenie umożliwia przestrzeni nazw o nazwie ContosoPartners znajdującej się w centrum danych Stanów Zjednoczonych Zachód i przypisanej do grupy zasobów ContosoNotificationsGroup.

## PARAMETERS

### — Krytyczne
Wskazuje, czy przestrzeń nazw jest krytyczną przestrzenią nazw.
Krytycznych przestrzeni nazw nie można usunąć.
Aby usunąć krytyczną przestrzeń nazw, należy ustawić wartość tej właściwości na Fałsz, aby oznaczyć przestrzeń nazw jako niekrytykową.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### — Wymuszanie
Nie pytaj o potwierdzenie.

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

### — Lokalizacja
Określa nazwę wyświetlaną centrum danych hostatora przestrzeni nazw.
Ten parametr można ustawić na dowolną prawidłową lokalizację na platformie Azure, ale w celu uzyskania optymalnej wydajności należy użyć centrum danych znajdującego się w pobliżu większości użytkowników.
Aby uzyskać dostęp do aktualnej listy lokalizacji platformy Azure, uruchom następujące polecenie: `Get-AzLocation | Select-Object DisplayName`

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

### —Przestrzeń nazw
Określa przestrzeń nazw, która jest zmieniana przez to polecenie cmdlet.
Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.

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

### -ResourceGroup
Określa grupę zasobów, do której jest przypisana przestrzeń nazw.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.

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

### -SkuTier
Warstwa SKU przestrzeni nazw

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — województwo
Określa bieżący stan przestrzeni nazw.
Dopuszczalne wartości dla tego parametru to: Aktywny i Wyłączony.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Określa pary nazwa-wartość, których można używać do kategoryzowania i organizowania elementów platformy Azure.
Tagi działają podobnie do słów kluczowych i działają we wdrożeniu.
Jeśli na przykład wyszukuje się wszystkie elementy z tagiem Department:IT, wyszukiwanie zwróci wszystkie elementy platformy Azure, które mają ten tag, bez względu na elementy, takie jak typ elementu, lokalizacja lub grupa zasobów.
Pojedynczy tag składa się z dwóch części: *nazwa* i (opcjonalnie) *wartość.*
Na przykład w dziale dział:IT nazwa tagu to Dział, a wartością tagu jest IT.
Aby dodać tag, użyj składni tabeli skrótów podobnej do tej, co powoduje utworzenie tagu Rok_kalendarza:2016: -Tagi @{Name="Rok_kalendarza"; Value="2016"} Aby dodać wiele tagów za pomocą tego samego polecenia, oddziel poszczególne tagi przecinkami: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="Rok Obrachunkowy"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


