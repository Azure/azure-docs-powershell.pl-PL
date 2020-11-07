---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: e678ceabefac101a70724a8a901a9bf3db08a59b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718536"
---
# Get-AzureRmDnsRecordSet

## STRESZCZENIe
Pobiera zestaw rekordów DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Field
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Stream
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDnsRecordSet** Pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.

Jeśli nie określisz parametrów *name* lub *recordType* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.
Jeśli określisz parametr *recordType* , a nie parametr *name* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.

Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy i grupy zasobów według nazwy.

## Przykłady

### Przykład 1: pobieranie zestawów rekordów o określonej nazwie i typie
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

To polecenie pobiera zestaw rekordów typu rekordu o nazwie www w określonej grupie zasobów i strefie, a następnie zapisuje go w zmiennej $RecordSet.
Ponieważ określono parametry *name* i *recordType* , zwracany jest tylko pojedynczy obiekt **Recordset** .

### Przykład 2: pobieranie zestawów rekordów określonego typu
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

To polecenie pobiera tablicę wszystkich zestawów rekordów typu rekord A w strefie o nazwie myzone.com w grupie zasób o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.

### Przykład 3: pobieranie wszystkich zestawów rekordów w strefie
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $RecordSets.

### Przykład 4: pobieranie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

Ten przykład jest równoważny przykładowi 3 powyżej.
W tym czasie strefa jest określana za pomocą obiektu strefy.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę **zestawu rekordów** , który ma zostać wyświetlony.
Jeśli parametr *name* nie jest określony, zwracane są wszystkie zestawy rekordów określonego typu.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Records
Określa typ rekordu DNS, który jest pobierany przez to polecenie cmdlet.

Prawidłowe wartości: 

- Sieci
- AAAA
- REKORD
- MX
- REKORDU
- SYSTEMU
- REKORD
- SRV
- ROZSZERZENIEM

Jeśli nie określono parametru *recordType* , należy także pominąć parametr *name* . To polecenie cmdlet zwraca następnie wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów zawierającą strefę DNS.
Nazwę strefy należy również określić przy użyciu parametru *zonename* .

Możesz też określić strefę i grupę zasobów, przechodząc do obiektu **dnsZone** przy użyciu parametru *Zone* .

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
Określa strefę DNS zawierającą zestaw rekordów, który jest pobierany przez to polecenie cmdlet.
Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .

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

### -Nazwa_strefy
Określa nazwę strefy DNS zawierającej zestaw rekordów do pobrania.
Grupa zasobów zawierająca strefę musi być również określona przy użyciu parametru *ResourceGroupName* .

Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .

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
Obiekt **dnsZone** reprezentuje strefę, w której należy szukać obiektu **Recordset** .

## WYSYŁA

### Microsoft. Azure. Commands. DNS. DnsRecordSet
To polecenie cmdlet zwraca co najmniej jeden obiekt reprezentujący znalezione zestawy rekordów.
Jeśli jest określony parametr *name* and *recordType* , zostanie zwróconych co najwyżej jeden **zestaw rekordów** , w przeciwnym razie wiele obiektów **Recordset** jest zwracanych jako tablica.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


