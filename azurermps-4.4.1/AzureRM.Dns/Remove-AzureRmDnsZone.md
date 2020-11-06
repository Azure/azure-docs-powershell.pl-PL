---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: a9f277c17d0396127ca1b2678d8c9c77ef3628c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553328"
---
# Remove-AzureRmDnsZone

## STRESZCZENIe
Usuwa strefę DNS z grupy zasobów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Field
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Stream
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmDnsZone** trwale usuwa strefę DNS (Domain Name System) z określonej grupy zasobów.
Wszystkie zestawy rekordów zawarte w tej strefie również zostaną usunięte.

Obiekt **dnsZone** można przekazać przy użyciu parametru *name* lub za pomocą operatora potoku lub można też określić parametry *zonename* i *ResourceGroupName* .

Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.

Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).
Zapewnia to ochronę współbieżnych zmian stref.
Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.

## Przykłady

### Przykład 1. Usuń strefę
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie Moja zasobów.

## PARAMETRÓW

### -Force
Ten parametr jest przestarzały dla tego polecenia cmdlet.
Zostanie on usunięty w przyszłym wydaniu.

Aby określić, czy to polecenie cmdlet monituje o potwierdzenie, użyj parametru *Confirm* .

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

### -Name (nazwa)
Określa nazwę strefy DNS, która zostanie usunięta przez to polecenie cmdlet.
Musisz również określić parametr *ResourceGroupName* .

Możesz też określić strefę DNS przy użyciu parametru *Zone* .

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

### -Overwrite
Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).
Zapewnia to ochronę współbieżnych zmian stref.

Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.

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
Należy również określić parametr *zonename* .

Możesz też określić strefę DNS za pomocą obiektu **dnsZone** , przekazaną za pośrednictwem potoku lub parametru *Zone* .

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

### -Zone
Określa strefę DNS do usunięcia.
Przekazany obiekt **dnsZone** można również przekazywać za pośrednictwem rurociągu.

Możesz też określić strefę DNS do usunięcia przy użyciu parametrów *zonename* i *ResourceGroupName* .

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### Microsoft. Azure. Commands. DNS. DnsZone
Do tego polecenia cmdlet można nawiązać obiekt **dnsZone** .

## WYSYŁA

### Znaleziono
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN
Ze względu na potencjalnie wysoki wpływ usunięcia strefy DNS to polecenie cmdlet domyślnie monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma dowolną wartość inną niż none.

Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.
Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie. 

## LINKI POKREWNE

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[Nowe — AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
