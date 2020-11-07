---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9896a8e1cfd2e3c0dc3887513d93e902260b82c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718501"
---
# New-AzureRmDnsRecordSet

## STRESZCZENIe
Tworzy zestaw rekordów DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Field
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Stream
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmDnsRecordSet** tworzy nowy zestaw rekordów DNS (Domain Name System) o określonej nazwie i wpisz w określonej strefie.
Obiekt **Recordset** to zestaw rekordów DNS o tej samej nazwie i typie.
Zauważ, że nazwa jest względna względem strefy, a nie w pełni kwalifikowanej nazwy.

Parametr *DnsRecords* określa rekordy w zestawie rekordów.
Ten parametr pobiera tablicę rekordów DNS konstruowaną przy użyciu funkcji New-AzureRmDnsRecordConfig.

Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy według nazwy.

Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.

Jeśli pasujący **zestaw rekordów** już istnieje (ta sama nazwa i typ rekordu), należy określić parametr *zastępowania* , w przeciwnym razie polecenie cmdlet nie spowoduje utworzenia nowego **zestawu rekordów** .

## Przykłady

### Przykład 1. Tworzenie zestawu rekordów typu A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.
Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

### Przykład 2: Tworzenie zestawu rekordów typu AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.
Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 3: Tworzenie zestawu rekordów typu CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.
Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 4: Tworzenie zestawu rekordów typu MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.
Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 5: Tworzenie zestawu rekordów typu NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie ns1 w strefie MyZone.com.
Zestaw rekordów jest typu NS i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 6: Tworzenie zestawu rekordów typu PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie 4 w strefie 3.2.1.in-addr. arpa.
Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 7: Tworzenie zestawu rekordów typu SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie _sip. _tcp w strefie MyZone.com.
Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS wskazujący adres IP 2001.2.3.4.

Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 8: Tworzenie zestawu rekordów typu TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie tekst w strefie MyZone.com.
Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).
Zawiera jeden rekord DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 9: Tworzenie zestawu rekordów w strefie Apex
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** według wierzchołka (lub głównego) strefy MyZone.com.
W tym celu nazwa zestawu rekordów jest określana jako "@" (łącznie z cudzysłowami podwójnymi).

Nie można utworzyć rekordów CNAME na wierzchołku strefy.
Jest to ograniczenie standardów DNS. nie jest to ograniczenie dotyczące usługi Azure DNS.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 10: Tworzenie zestawu rekordów symboli wieloznacznych
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

To polecenie tworzy **zestaw rekordów** o nazwie * w strefie MyZone.com.
To jest zestaw rekordów z symbolami wieloznacznymi.

Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 11: Tworzenie pustego zestawu rekordów
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.
Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).
To jest pusty zestaw rekordów, który działa jako symbol zastępczy, do którego można później dodawać rekordy.

### Przykład 12: Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

To polecenie tworzy **zestaw rekordów**.
Parametr *overwrite* zapewnia, że ten zestaw rekordów zastępuje dowolny już istniejący zestaw rekordów o tej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).
Parametr *Confirm* z wartością $false powoduje pominięcie monitu o potwierdzenie.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsRecords
Określa tablicę rekordów DNS, które mają zostać uwzględnione w zestawie rekordów.
Za pomocą polecenia cmdlet New-AzureRmDnsRecordConfig możesz tworzyć obiekty rekordów DNS.
Zobacz przykłady, aby uzyskać więcej informacji.

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Ten parametr jest przestarzały dla tego polecenia cmdlet.
Zostanie on usunięty w przyszłym wydaniu.

Aby określić, czy to polecenie cmdlet monituje o comfirmation, użyj parametru *Confirm* .

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

### -Metadata
Określa tablicę metadanych, które należy skojarzyć z zestawem rekordów.
Metadane są określane za pomocą par nazwa-wartość, które są reprezentowane jako tabele skrótów, na przykład @ (@ {"name" = "Dept"; "Wartość" = "zakupy"}, @ {"nazwa" = "ENV"; "Wartość" = "produkcja"}).

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę **zestawu rekordów** , który ma zostać utworzony.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wskazuje, że to polecenie cmdlet zastąpi określony **zestaw rekordów** , jeśli już istnieje.

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

### -Records
Określa typ rekordu DNS, który ma zostać utworzony.

Prawidłowe wartości:

- Sieci
- AAAA
- REKORD
- MX
- REKORDU
- SYSTEMU
- SRV
- ROZSZERZENIEM

Rekordy SOA są tworzone automatycznie podczas tworzenia strefy i nie można ich tworzyć ręcznie.

```yaml
Type: RecordType
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
Aby określić nazwę strefy, należy również określić parametr *zonename* .

Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .

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

### -TTL
Określa czas wygaśnięcia zestawu rekordów DNS (TTL).

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Określa DnsZone, w którym ma zostać utworzony **zestaw rekordów**.
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

### -Nazwa_strefy
Określa nazwę strefy, w której ma zostać utworzony **zestaw rekordów**.
Należy także określić grupę zasobów zawierającą strefę za pomocą parametru *ResourceGroupName* .

Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. DNS. DnsZone
Do tego polecenia cmdlet można nawiązać obiekt DnsZone.

## WYSYŁA

### Microsoft. Azure. Commands. DNS. DnsRecordSet
To polecenie cmdlet zwraca obiekt **Recordset** .

## INFORMACYJN
Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.

Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.
Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.

## LINKI POKREWNE

[Dodaj-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Nowe — AzureRmDnsRecordConfig](./New-AzureRmDnsRecordConfig.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
