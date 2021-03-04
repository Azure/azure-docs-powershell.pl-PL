---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958225"
---
# New-AzPublicIpAddress

## SYNOPSIS
Tworzy publiczny adres IP.

## SKŁADNIA

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzPublicIpAddress** tworzy publiczny adres IP.

## PRZYKŁADY

### Przykład 1. Tworzenie nowego publicznego adresu IP
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

To polecenie tworzy nowy zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu. Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ wartość -AllocationMethod jest określana jako statyczna. Jeśli zostanie on określony jako "Dynamiczny", publiczny adres IP zostanie przydzielony tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (na przykład maszyny wirtualnej lub równoważenia obciążenia).

### Przykład 2. Tworzenie publicznego adresu IP z odwrotną domeną FQDN
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

To polecenie tworzy nowy zasób publicznych adresów IP. W przypadku parametru -ReverseFqdn platforma Azure tworzy rekord PTR DNS (odnośnik odwrotny) dla publicznego adresu IP przydzielonego do tego zasobu, który $customFqdn określony w poleceniu. Jako wymaganie wstępne $customFqdn (na przykład webapp.contoso.com) powinien mieć rekord CNAME DNS (odnośnik do przodu) który wskaże adres $dnsPrefix.$location.cloudapp.azure.com.

### Przykład 3. Tworzenie nowego publicznego adresu IP przy użyciu tagu IpTag
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

To polecenie tworzy nowy zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu. Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ wartość -AllocationMethod jest określana jako statyczna. Jeśli zostanie on określony jako "Dynamiczny", publiczny adres IP zostanie przydzielony tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (na przykład maszyny wirtualnej lub równoważenia obciążenia). Tag Ip jest używany do oznaczania znaczników skojarzonych z zasobem. Tag Iptag można określić przy użyciu New-AzPublicIpTag i przekazany jako dane wejściowe za pośrednictwem -IpTags.

### Przykład 4. Tworzenie nowego publicznego adresu IP z prefiksem
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

To polecenie tworzy nowy zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu. Publiczny adres IP jest natychmiast przydzielany do tego zasobu z określonego publicIpPrefix.
Ta opcja jest obsługiwana tylko dla standardowej wersji SKU i statycznej metody AllocationMethod.

### Przykład 5. Tworzenie nowego globalnego publicznego adresu IP
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

To polecenie tworzy nowy globalny zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu. Do tego zasobu zostanie natychmiast przydzielony globalny publiczny adres IP.
Ta opcja jest obsługiwana tylko dla standardowej wersji SKU i statycznej metody AllocationMethod.

## PARAMETERS

### -AllocationMethod
Określa metodę przydzielania publicznego adresu IP.
Dopuszczalne wartości dla tego parametru to: statyczny lub dynamiczny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — AsJob
Uruchamianie polecenia cmdlet w tle

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -DomainNameLabel
Określa względną nazwę DNS dla publicznego adresu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.

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

### -IdleTimeoutInMinutes
Określa czas bezczynności (w minutach).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
Określa wersję adresu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Lista tagów IP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa region, w którym ma być tworzyć publiczny adres IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę publicznego adresu IP, który tworzy to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - PublicIpPrefix
Określa ustawienie PSPublicIpPrefix, z którego należy przydzielić publiczny adres IP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której ma być tworzyć publiczny adres IP.

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

### -ReverseFqdn
Określa w pełni kwalifikowaną nazwę domeny (FQDN).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - SKU
Nazwa publicznej sku adresu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="wartość2"}

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

### - Warstwa
Publiczna warstwa SKU adresu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Strefa
Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]

### Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix

### System.Int32

### System.String[]

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## NOTATKI

## LINKI POKREWNE

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
