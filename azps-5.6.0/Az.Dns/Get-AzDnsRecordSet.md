---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984831"
---
# Get-AzDnsRecordSet

## SYNOPSIS
Pobiera zestaw rekordów DNS.

## SKŁADNIA

### Pola
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Obiekt
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDnsRecordSet** pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.
Jeśli parametry Name  (Nazwa) lub *RecordType* (Typ Rekordu) nie zostaną określone, to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.
Jeśli określisz parametr *RecordType,* ale nie parametr *Name,* to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.
Za pomocą operatora potoku możesz przekazać obiekt **DnsZone** do tego polecenia cmdlet lub przekazać obiekt **DnsZone** jako parametr *Strefy* lub możesz też określić grupę strefy i zasobów według nazwy.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie zestawów rekordów o określonej nazwie i typie
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

To polecenie pobiera zestaw rekordów typu A o nazwie www w określonej grupie zasobów i strefie, a następnie przechowuje go w $RecordSet zmienną.
Ponieważ parametry *Name (Nazwa)* *i RecordType (Typ* Rekordu) są określone, zwracany jest tylko jeden obiekt **RecordSet.**

### Przykład 2. Uzyskiwanie zestawów rekordów określonego typu
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

To polecenie pobiera tablicę wszystkich zestawów rekordów typu A w strefie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w zmiennej $RecordSets zasobów.

### Przykład 3. Uzyskiwanie wszystkich zestawów rekordów w strefie
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w $RecordSets zmienną.

### Przykład 4. Uzyskiwanie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Ten przykład jest odpowiednikiem powyższego przykładu 3.
Tym razem strefa jest określana przy użyciu obiektu strefy.

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
Określa nazwę zestawu **rekordów do** uzyskania.
Jeśli parametr Name nie zostanie *określony,* zostaną zwrócone wszystkie zestawy rekordów określonego typu.

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

### -RecordType
Określa typ rekordu DNS, który otrzymuje to polecenie cmdlet.
Prawidłowe wartości to: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Jeśli nie określisz *parametru RecordType,* musisz również pominąć parametr *Name.* To polecenie cmdlet zwraca następnie wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów zawierającą strefę DNS.
Należy również określić nazwę strefy przy użyciu *parametru ZoneName.*
Możesz również określić strefę i grupę zasobów, przechodząc do obiektu **DnsZone** przy użyciu *parametru Zone.*

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
Określa strefę DNS zawierającą zestaw rekordów, który otrzymuje to polecenie cmdlet.
Można również określić strefę przy użyciu parametrów *Nazwa_strefy* i *ResourceGroupName.*

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

### -ZoneName
Określa nazwę strefy DNS zawierającej zestaw rekordów do uzyskania.
Grupę zasobów zawierającą strefę należy również określić przy użyciu *parametru ResourceGroupName.*
Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTATKI

## LINKI POKREWNE

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


