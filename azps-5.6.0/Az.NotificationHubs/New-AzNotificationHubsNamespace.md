---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951258"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Tworzy przestrzeń nazw centrum powiadomień.

## SKŁADNIA

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzNotificationHubsNamespace** tworzy przestrzeń nazw centrum powiadomień.
Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.
Musisz mieć co najmniej jedną przestrzeń nazw centrum powiadomień.
Jedna przestrzeń nazw może mieć wiele koncentratorów.
Możesz mieć wiele przestrzeni nazw do organizowania swoich centrów lub nadawać określonym osobom uprawnienia do zarządzania wybranym podzestawem swoich centrów.
Aby utworzyć przestrzeń nazw, należy podać unikatową nazwę przestrzeni nazw. określ centrum danych, w którym będzie się znajdowała przestrzeń nazw; i określ grupę zasobów, do których zostanie przypisana przestrzeń nazw.
Po utworzeniu przestrzeni nazw możesz użyć polecenia cmdlet New-AzNotificationHubsNamespaceAuthorizationRules do przypisywania reguł autoryzacji do tej przestrzeni nazw.
Reguły autoryzacji służą do zarządzania uprawnieniami do przestrzeni nazw.

## PRZYKŁADY

### Przykład 1. Tworzenie centrum powiadomień
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.
Przestrzeń nazw będzie się znajdowała w centrum danych Stanów Zjednoczonych Zachód i zostanie przypisana do grupy zasobów ContosoNotificationsGroup.

### Przykład 2. Tworzenie centrum powiadomień z tagami
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.
Przestrzeń nazw będzie się znajdowała w centrum danych Stanów Zjednoczonych Zachód i zostanie przypisana do grupy zasobów ContosoNotificationsGroup.
Ponadto to polecenie tworzy tag z nazwą Odbiorcy i wartościami organizacji partnerów i jest przypisywany do przestrzeni nazw.
Dzięki temu przestrzeń nazw będzie wyświetlana w dowolnym momencie filtrowania elementów, dla których tag Odbiorcy ma ustawioną wartość PartnerOrganizations.

## PARAMETERS

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

### — Lokalizacja
Określa nazwę wyświetlaną centrum danych, które będzie hostować przestrzeń nazw.
Ten parametr można ustawić na dowolną prawidłową lokalizację, jednak w celu zapewnienia optymalnej wydajności może być konieczne użycie centrum danych znajdującego się w pobliżu większości użytkowników.

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
Określa nazwę nowej przestrzeni nazw.
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
Określa grupę zasobów, do której zostanie przypisana przestrzeń nazw.
Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie nimi.

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

### — Tag
Określa pary nazwa-wartość, których można używać do kategoryzowania i organizowania elementów platformy Azure.
Tagi działają podobnie do słów kluczowych i działają we wdrożeniu.
Jeśli na przykład wyszukuje się wszystkie elementy z tagiem Department:IT, wyszukiwanie zwróci wszystkie elementy platformy Azure, które mają ten tag, bez względu na elementy, takie jak typ elementu, lokalizacja lub grupa zasobów.
Pojedynczy tag składa się z dwóch części: *Nazwa* i (opcjonalnie) *wartości.*
Na przykład w dziale DZIAŁ:IT nazwa tagu to Dział, a wartością tagu jest IT.
Aby dodać tag, użyj składni tabeli skrótów podobnej do poniższej, co powoduje utworzenie tagu Rok_kalendarza:2016:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTATKI

## LINKI POKREWNE

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


