---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 347f590ecd6e2825264e6bb0b980dd94450b0f06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898490"
---
# Set-AzureRmDnsZone

## STRESZCZENIe
Aktualizuje właściwości strefy DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Field
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Stream
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmDnsZone** aktualizuje określoną strefę DNS w usłudze DNS Azure.
To polecenie cmdlet nie powoduje zaktualizowania zestawów rekordów w strefie.

Obiekt **dnsZone** można przekazać jako parametr lub za pomocą operatora potoku albo też można określić parametry *zonename* i *ResourceGroupName* .

Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.

Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone. Zapewnia to ochronę współbieżnych zmian. Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.

## Przykłady

### Przykład 1: aktualizowanie strefy DNS
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

Pierwsze polecenie pobiera strefę o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.

Drugie polecenie aktualizuje znaczniki $Zone.

Polecenie ostatnie zatwierdza zmianę.

### Przykład 2: aktualizowanie znaczników dla strefy
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

To polecenie aktualizuje znaczniki strefy o nazwie myzone.com bez uprzedniego uzyskania tej strefy.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę strefy DNS do zaktualizowania.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone. Zapewnia to ochronę współbieżnych zmian. Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.
Należy również określić parametr zonename.

Możesz też określić strefę za pomocą obiektu DnsZone z parametrem *Zone* lub Pipeline.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Określa strefę DNS do zaktualizowania.

Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .

```yaml
Type: DnsZone
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. DNS. DnsZone
Do tego polecenia cmdlet można nawiązać obiekt DnsZone.

## WYSYŁA

### Microsoft. Azure. Commands. DNS. DnsZone
To polecenie cmdlet zwraca obiekt DnsZone, który reprezentuje zaktualizowaną strefę DNS przy użyciu nowego elementu ETag.

## INFORMACYJN
Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.

Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.
Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.

## LINKI POKREWNE

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[Nowe — AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
