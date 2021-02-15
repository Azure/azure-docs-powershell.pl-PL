---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180747"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Usuwa zestaw rekordów.

## SKŁADNIA

### Pola
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Mieszany
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Obiekt
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzDnsRecordSet** usuwa określony zestaw rekordów z określonej strefy.
Nie można usuwać rekordów SOA ani nazw serwera nazw, które są automatycznie tworzone w wierzchołku strefy.
Obiekt **RecordSet** można przekazać do tego polecenia cmdlet, używając operatora potoku lub parametru.
Aby zidentyfikować zestaw rekordów według nazwy i typu bez użycia obiektu **RecordSet,** należy przekazać strefę jako obiekt **DnsZone** do tego polecenia cmdlet przy użyciu operatora potoku lub parametru albo określić parametry *ZoneName* i *ResourceGroupName.*
Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.
Podczas określania zestawu rekordów przy użyciu obiektu **RecordSet** zestaw rekordów nie jest usuwany, jeśli został zmieniony w systemie Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**
Zapewnia to ochronę w przypadku jednoczesnych zmian.
Można to pominąć przy użyciu *parametru Zastąp,* który usuwa zestaw rekordów niezależnie od jednoczesnych zmian.

## PRZYKŁADY

### Przykład 1. Usuwanie zestawu rekordów
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w $RecordSet zmienną. Drugie polecenie usuwa zestaw rekordów z $RecordSet.

### Przykład 2. Usuwanie zestawu rekordów i pomijanie wszystkich potwierdzeń
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Pierwsze polecenie pobiera określony zestaw rekordów.
Drugie polecenie usuwa zestaw rekordów, nawet jeśli zmienił się w międzyczasie.
Monity o potwierdzenie są pomijane.

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
Określa nazwę zestawu rekordów **do** usunięcia.
Podczas określania rekordu ustawionego według nazwy należy określić strefę DNS przy użyciu parametrów *Zone* lub *ZoneName* i *ResourceGroupName.*
Ewentualnie zestaw rekordów można określić przy użyciu obiektu **RecordSet** przekazywanego przy użyciu *parametru RecordSet.*

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zastąp
Podczas określania zestawu rekordów przy użyciu obiektu **RecordSet** zestaw rekordów nie jest usuwany, jeśli został zmieniony w systemie Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**
Zapewnia to ochronę w przypadku jednoczesnych zmian.
Można to pominąć przy użyciu *parametru Zastąp,* który usuwa zestaw rekordów niezależnie od jednoczesnych zmian.

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

### - RecordSet
Określa obiekt **RecordSet** do usunięcia.
Można również określić zestaw rekordów za  pomocą  parametrów Nazwa i Strefa lub przy użyciu parametrów *Nazwa,* Nazwa Strefy *i* *NazwaGrupy Zasobów.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Określa typ rekordu DNS.
Prawidłowe wartości to:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- Rekordy TXT SOA są usuwane automatycznie po usunięciu strefy.
Nie można ręcznie usuwać rekordów SOA.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów do** usunięcia.
Ten parametr ma zastosowanie tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu *parametrów Name (Nazwa)* *i ZoneName (Nazwa strefy).*
Możesz również określić zestaw rekordów, używając parametru *RecordSet* lub *parametrów Name* i *Zone.*

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
Określa strefę DNS zawierającą **zestaw rekordów do** usunięcia.
Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu *parametru Name.*
Możesz również określić zestaw rekordów za pomocą parametru *RecordSet* lub *parametrów Name* *(Nazwa* strefy) i *ResourceGroupName (Nazwa strefy) i ResourceGroupName (Nazwa* Grupy Zasobów).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Określa nazwę strefy zawierającej zestaw **rekordów do** usunięcia.
Należy także określić parametry *Name (Nazwa) i* *ResourceGroupName (Nazwa grupy zasobów).*
Ewentualnie zestaw rekordów można określić za pomocą parametru *RecordSet* lub *parametrów Name* i *Zone.*

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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI
Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.
Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.
Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.

## LINKI POKREWNE

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
