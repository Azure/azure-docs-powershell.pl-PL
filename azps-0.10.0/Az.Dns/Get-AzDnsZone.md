---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893173"
---
# Get-AzDnsZone

## STRESZCZENIe
Pobiera strefę DNS.

## POLECENIA

### Domyślne (domyślnie)
```
Get-AzDnsZone [<CommonParameters>]
```

### Przysourceing
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDnsZone** pobiera strefę DNS (Domain Name System) z określonej grupy zasobów.
Jeśli określisz parametr *name* , zwracany jest jeden obiekt **dnsZone** .
Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.
Za pomocą obiektu **dnsZone** można aktualizować strefę, na przykład dodawać do niej obiekty **Recordset** .

## Przykłady

### Przykład 1: uzyskiwanie strefy
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

W tym przykładzie otrzymano strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.

### Przykład 2: pobieranie wszystkich stref w grupie zasobów
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

W tym przykładzie są pobierane wszystkie strefy DNS w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Zones.

### Przykład 3: uzyskiwanie wszystkich stref w ramach abonamentu
```
PS C:\> $Zones = Get-AzDnsZone
```

W tym przykładzie są pobierane wszystkie strefy DNS w bieżącej subskrypcji platformy Azure, a następnie są one przechowywane w zmiennej $Zones.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę strefy DNS do pobrania.

Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet będzie pobierać wszystkie strefy DNS w określonej grupie zasobów.
W przypadku pominięcia parametru *ResourceGroupName* to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej strefę DNS do pobrania.

Jeśli nie określisz *ResourceGroupName* , musisz także pominąć parametr *name (nazwa* ).
W tym przypadku to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie umożliwia wprowadzania danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. DNS. DnsZone
To polecenie cmdlet zwraca obiekt reprezentujący strefę DNS.
Jeśli nie określono nazwy strefy, zwracana jest tablica obiektów strefy.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
