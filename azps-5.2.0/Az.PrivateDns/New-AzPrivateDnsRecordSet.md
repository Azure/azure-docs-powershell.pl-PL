---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358141"
---
# New-AzPrivateDnsRecordSet

## STRESZCZENIe
Tworzy zestaw rekordów w prywatnej strefie DNS.

## POLECENIA

### Pola (domyślnie)
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Stream
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Zasobów
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzPrivateDnsRecordSet tworzy nowy, prywatny zestaw rekordów DNS (Domain Name System) z określoną nazwą i typem w określonej strefie prywatnej. Obiekt RecordSet jest zestawem prywatnych rekordów DNS o tej samej nazwie i typie. Należy pamiętać, że nazwa jest określana względem strefy prywatnej, a nie w pełni kwalifikowanej nazwie. Parametr PrivateDnsRecord określa rekordy w zestawie rekordów. Ten parametr pobiera tablicę prywatnych rekordów DNS zbudowanych przy użyciu funkcji New-AzPrivateDnsRecordConfig. Za pomocą operatora potoku możesz przekazać obiekt PSPrivateDnsZone do tego polecenia cmdlet lub przekazać obiekt PSPrivateDnsZone jako parametr Zone lub określić strefę jako identyfikator zasobu, lub możesz określić strefę według nazwy. Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie. Jeśli pasujący zestaw rekordów już istnieje (ta sama nazwa i typ rekordu), należy określić parametr zastępowania, w przeciwnym razie polecenie cmdlet nie spowoduje utworzenia nowego zestawu rekordów.

## Przykłady

### Przykład 1. Tworzenie zestawu rekordów typu A
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com. Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS.

### Przykład 2: Tworzenie zestawu rekordów typu AAAA
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com. Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 3: Tworzenie zestawu rekordów typu CNAME
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com. Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 4: Tworzenie zestawu rekordów typu MX
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie www w strefie prywatnej myzone.com. Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 5: Tworzenie zestawu rekordów typu PTR
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie 4 w strefie prywatnej 3.2.1.in-addr. arpa. Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 6: Tworzenie zestawu rekordów typu SRV
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie _sip. _tcp w strefie prywatnej myzone.com. Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera pojedynczy prywatny rekord DNS, wskazujący adres IP 2001.2.3.4. Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 7: Tworzenie zestawu rekordów typu TXT
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie tekst w strefie prywatnej myzone.com. Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund). Zawiera jeden prywatny rekord DNS. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 8: Tworzenie zestawu rekordów w strefie Apex
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów na wierzchołku (lub korzeniu) strefy myzone.com. W tym celu nazwa zestawu rekordów jest określana jako "@" (łącznie z cudzysłowami podwójnymi). Nie można utworzyć rekordów CNAME na wierzchołku strefy. Jest to ograniczenie standardów DNS. nie jest to ograniczenie dotyczące prywatnego systemu DNS platformy Azure. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 9: Tworzenie zestawu rekordów symboli wieloznacznych

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie * w strefie prywatnej myzone.com. To jest zestaw rekordów z symbolami wieloznacznymi. Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.

### Przykład 10: Tworzenie pustego zestawu rekordów

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

To polecenie tworzy zestaw rekordów o nazwie * w strefie prywatnej myzone.com. Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund). To jest pusty zestaw rekordów, który działa jako symbol zastępczy, do którego można później dodawać rekordy.

### Przykład 11: Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

To polecenie tworzy zestaw rekordów. Parametr overwrite zapewnia, że ten zestaw rekordów zastępuje dowolny już istniejący zestaw rekordów o tej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone). Parametr Confirm z wartością $False powoduje pominięcie monitu o potwierdzenie.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Metadata
Tabela skrótów reprezentująca znaczniki zasobów.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwy rekordów w tym zestawie rekordów (w odniesieniu do nazwy strefy i bez kropki przerywanej).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Nie kończy się niepowodzeniem, jeśli zestaw rekordów już istnieje.

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

### -ParentResourceId
Identyfikator zasobu prywatnej strefy DNS.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateDnsRecord
Prywatne rekordy DNS, które są częścią tego zestawu rekordów.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Records
Typ prywatnych rekordów DNS w tym zestawie rekordów.

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, do której należy strefa.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Wartość TTL wszystkich rekordów w tym zestawie rekordów.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Obiekt PrivateDnsZone reprezentujący strefę, w której ma zostać utworzony zestaw rekordów.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nazwa_strefy
Strefa, w której ma zostać utworzony zestaw rekordów (bez przerywanej kropki).

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet

## INFORMACYJN

## LINKI POKREWNE
