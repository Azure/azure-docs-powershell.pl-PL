---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: 10cd4936ad406be85f840b25c175d7900d66d679
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893158"
---
# Remove-AzDnsRecordSet

## STRESZCZENIe
Usuwa zestaw rekordów.

## POLECENIA

### Field
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Karoten
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Stream
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzDnsRecordSet** umożliwia usunięcie określonego zestawu rekordów z określonej strefy.
Nie można usuwać rekordów serwera SOA ani serwerów nazw (NS), które są tworzone automatycznie w strefie Apex.

Do tego polecenia cmdlet można przekazać obiekt **Recordset** za pomocą operatora potoku lub jako parametru.
Aby zidentyfikować zestaw rekordów i wpisać go bez użycia obiektu **Recordset** , należy przekazać strefę jako obiekt **dnsZone** do tego polecenia cmdlet, korzystając z operatora potoku lub jako parametru lub można też określić parametry *zonename* i *ResourceGroupName* .

Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.

Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .
Zapewnia to ochronę współbieżnych zmian.
Można to pominąć, używając parametru *zastępowania* , który usuwa zestaw rekordów bez względu na zmiany współbieżne.

## Przykłady

### Przykład 1: usuwanie zestawu rekordów
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w zmiennej $RecordSet. Drugie polecenie usuwa zestaw rekordów w $RecordSet.

### Przykład 2: usunięcie zestawu rekordów i pominięcie wszystkich potwierdzeń
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Pierwsze polecenie pobiera określony zestaw rekordów.

Drugie polecenie usuwa zestaw rekordów, nawet jeśli został on zmieniony w międzyczasie.
Monity o potwierdzenie są pomijane.

## PARAMETRÓW

### -Force
Ten parametr jest przestarzały dla tego polecenia cmdlet.
Zostanie on usunięty w przyszłym wydaniu.

Aby określić, czy to polecenie cmdlet monituje o potwierdzenie, użyj parametru *Confirm* .

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę **zestawu rekordów** , który ma zostać usunięty.
Podczas określania zestawu rekordów według nazwy strefa DNS musi być określona przy użyciu parametru *Zone* lub parametry *zonename* i *ResourceGroupName* .

Zestaw rekordów można też określić za pomocą obiektu **Recordset** , przekazano przy użyciu parametru *Recordset* .

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .
Zapewnia to ochronę współbieżnych zmian.
Można to pominąć za pomocą parametru *overwrite* , co powoduje usunięcie zestawu rekordów bez względu na jednoczesne zmiany.

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

### -PassThru
passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
Określa obiekt **zestawu rekordów** , który ma zostać usunięty.

Zestaw rekordów można też określić przy użyciu parametrów *name* i *Zone* albo za pomocą parametrów *name* , *zonename* i *ResourceGroupName* .

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Records
Określa typ rekordu DNS.

Prawidłowe wartości:

- Sieci
- AAAA
- REKORD
- MX
- REKORDU
- SYSTEMU
- SRV
- ROZSZERZENIEM

Rekordy SOA są usuwane automatycznie po usunięciu strefy.
Nie można ręcznie usunąć rekordów SOA.

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów** do usunięcia.
Ten parametr jest stosowany tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu parametrów *name* i *zonename* .

Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* lub *nazwy* i parametrów *strefy* .

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

### -Zone
Określa strefę DNS zawierającą **zestaw rekordów** do usunięcia.
Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu parametru *name* .

Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* albo parametrów *name* , *zonename* i *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nazwa_strefy
Określa nazwę strefy zawierającej **zestaw rekordów** do usunięcia.
Musisz również określić *nazwę* i parametry *ResourceGroupName* .

Zestaw rekordów można też określić przy użyciu parametru *zestaw rekordów* albo *nazwy* i parametrów *strefy* .

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Do tego polecenia cmdlet można przetworzyć obiekt **zestawu rekordów** .

## WYSYŁA

### Znaleziono
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN
Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.

Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.
Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.

## LINKI POKREWNE

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Nowe — AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
