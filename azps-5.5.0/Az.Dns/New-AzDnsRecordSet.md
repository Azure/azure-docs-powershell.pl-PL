---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243683"
---
# New-AzDnsRecordSet

## SYNOPSIS
Tworzy zestaw rekordów DNS.

## SKŁADNIA

### Pola (domyślne)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Obiekt
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzDnsRecordSet** tworzy nowy zestaw rekordów DNS (Domain Name System) o określonej nazwie i wpisz w określonej strefie.
Obiekt **RecordSet** to zestaw rekordów DNS o tej samej nazwie i typie.
Pamiętaj, że nazwa jest względna dla strefy, a nie do w pełni kwalifikowanej nazwy.
Parametr *DnsRecords* określa rekordy w zestawie rekordów.
Ten parametr pobiera tablicę rekordów DNS skonstruowanych przy użyciu narzędzia New-AzDnsRecordConfig.
Za pomocą operatora potoku możesz przekazać obiekt **DnsZone** do tego polecenia cmdlet lub przekazać obiekt **DnsZone** jako parametr *Zone* lub alternatywnie możesz określić strefę według nazwy.
Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.
Jeśli zgodny zestaw **rekordów** już istnieje (nazwa i typ rekordu), musisz określić parametr *Zastąp,* w przeciwnym razie polecenie cmdlet nie utworzy **nowego zestawu rekordów.**

## PRZYKŁADY

### Przykład 1. Tworzenie zestawu rekordów typu A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.
Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.

### Przykład 2. Tworzenie zestawu rekordów typu AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.
Zestaw rekordów jest typu AAAA i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 3. Tworzenie zestawu rekordów typu CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.
Zestaw rekordów jest typu CNAME i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 4. Tworzenie zestawu rekordów typu MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy zestaw **rekordów** o nazwie www w strefie myzone.com.
Zestaw rekordów jest typu MX i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 5. Tworzenie zestawu rekordów typu NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy zestaw **rekordów** o nazwie ns1 w strefie myzone.com.
Zestaw rekordów jest typu NS i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 6. Tworzenie zestawu rekordów typu PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

To polecenie tworzy zestaw **rekordów o** nazwie 4 w strefie 3.2.1.in-addr.arpa.
Zestaw rekordów jest typu PTR i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 7. Tworzenie zestawu rekordów typu SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw** rekordów o nazwie _sip._tcp w strefie myzone.com.
Zestaw rekordów jest typu SRV i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera ona jeden rekord DNS, który wskaże adres IP 2001.2.3.4.
Usługa (sip) i protokół (tcp) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 8. Tworzenie zestawu rekordów typu TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **nazwany tekst zestawu** rekordów w strefie myzone.com.
Zestaw rekordów jest typu TXT i ma czas wygaśnięcia 1 godziny (3600 sekund).
Zawiera jeden rekord DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 9. Tworzenie zestawu rekordów w wierzchołku strefy
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów na** wierzchu (lub katalogu głównym) strefy myzone.com.
W tym celu nazwa zestawu rekordów zostanie określona jako "@" (łącznie z cudzysłowami podwójnymi).
Nie można tworzyć rekordów CNAME na początku strefy.
Jest to ograniczenie standardów DNS. nie jest to ograniczenie systemu Azure DNS.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 10. Tworzenie zestawu rekordów z symbolami wieloznacznych
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy zestaw rekordów **o** nazwie * w strefie myzone.com.
Jest to zestaw rekordów z symbolami wieloznacznych.
Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 11. Tworzenie pustego zestawu rekordów
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

To polecenie tworzy zestaw **rekordów** o nazwie www w strefie myzone.com.
Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).
Jest to pusty zestaw rekordów, który pełni rolę symbolu zastępczego, do którego można później dodawać rekordy.

### Przykład 12. Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

To polecenie tworzy zestaw **rekordów.**
Parametr *Zastąp* gwarantuje, że ten zestaw rekordów zastąpi istniejący wcześniej zestaw rekordów o takiej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).
Parametr *Confirm* z wartością $False pomija monit o potwierdzenie.

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

### - DnsRecords
Określa tablicę rekordów DNS, które mają być dołączane do zestawu rekordów.
Możesz użyć polecenia cmdlet New-AzDnsRecordConfig do tworzenia obiektów rekordów DNS.
Zobacz przykłady, aby uzyskać więcej informacji.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Metadane
Określa tablicę metadanych do skojarzenia z zestawem rekordów.
Metadane są określane przy użyciu par nazwa-wartość, które są reprezentowane jako tabele skrótów, na przykład @{"dept"="shopping";" env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę zestawu rekordów **do** utworzenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Zastąp
Wskazuje, że to polecenie cmdlet zastępuje określony zestaw **rekordów,** jeśli już istnieje.

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

### -RecordType
Określa typ rekordu DNS do utworzenia.
Prawidłowe wartości to:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- Rekordy SOA TXT są tworzone automatycznie po utworzeniu strefy i nie można ich utworzyć ręcznie.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów zawierającą strefę DNS.
Aby określić nazwę strefy, musisz także określić parametr *ZoneName.*
Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Identyfikator zasobu docelowego aliasu.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Ttl
Określa czas wygaśnięcia (TTL) zestawu rekordów DNS.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Strefa
Określa strefę DnsZone, w której ma być **tworzyć zestaw rekordów.**
Można również określić strefę, używając parametrów *Nazwa_strefy* i *NazwaGrupy Zasobów.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Określa nazwę strefy, w której ma być tworzyć **zestaw rekordów.**
Grupę zasobów zawierającą strefę należy także określić przy użyciu *parametru ResourceGroupName.*
Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTATKI
Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.
Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.
Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.

## LINKI POKREWNE

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
