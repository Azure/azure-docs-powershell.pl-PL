---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180746"
---
# Remove-AzDnsZone

## SYNOPSIS
Usuwa strefę DNS z grupy zasobów.

## SKŁADNIA

### Pola
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Obiekt
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Remove-AzDnsZone** trwale usuwa strefę DNS (Domain Name System) z określonej grupy zasobów.
Usuwane są również wszystkie zestawy rekordów zawarte w strefie.
Obiekt **DnsZone** można przekazać za pomocą parametru *Name* lub za pomocą operatora potoku. Można też określić parametry *Nazwa_strefy* i *NazwaGrupy Zasobów.*
Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.
Podczas określania strefy przy użyciu obiektu **DnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **DnsZone** (tylko operacje bezpośrednio na zasobie strefy DNS liczą się jako zmiany, operacje na zestawach rekordów w strefie nie).
Zapewnia to ochronę przed jednoczesnym zmianą strefy.
Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.

## PRZYKŁADY

### Przykład 1. Usuwanie strefy
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie MyResourceGroup.

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

### — Nazwa
Określa nazwę strefy DNS, która jest usuwana przez to polecenie cmdlet.
Musisz także określić parametr *ResourceGroupName.*
Możesz również określić strefę DNS, używając *parametru Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Zastąp
Podczas określania strefy przy użyciu obiektu **DnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **DnsZone** (tylko operacje bezpośrednio na zasobie strefy DNS liczą się jako zmiany, operacje na zestawach rekordów w strefie nie).
Zapewnia to ochronę przed jednoczesnym zmianą strefy.
Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej strefę do usunięcia.
Musisz także określić parametr *ZoneName.*
Możesz również określić strefę DNS, używając obiektu **DnsZone,** przekazywanego przez parametr pipeline lub *Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Strefa
Określa strefę DNS do usunięcia.
Obiekt **DnsZone** może być również przekazany za pośrednictwem potoku.
Możesz również określić strefę DNS do usunięcia, używając parametrów *ZoneName* i *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.Commands.Dns.DnsZone

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI
Ze względu na potencjalnie duży wpływ usuwania strefy DNS to polecenie cmdlet domyślnie wyświetla monit o potwierdzenie, jeśli zmienna programu $ConfirmPreference Windows PowerShell ma dowolną wartość inną niż Brak.
Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.
Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie. 

## LINKI POKREWNE

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
