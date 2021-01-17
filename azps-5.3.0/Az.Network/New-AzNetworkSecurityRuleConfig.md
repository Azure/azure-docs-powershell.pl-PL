---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379071"
---
# New-AzNetworkSecurityRuleConfig

## STRESZCZENIe
Tworzy konfigurację reguły zabezpieczeń sieci.

## POLECENIA

### SetByResource (domyślny)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzNetworkSecurityRuleConfig** umożliwia utworzenie konfiguracji reguły zabezpieczeń sieci Azure dla grupy zabezpieczeń sieci.

## Przykłady

### Przykład 1. Tworzenie reguły zabezpieczeń sieci zezwalającej na protokół RDP
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 3389

### Przykład 2: Tworzenie reguły zabezpieczeń sieci zezwalającej na protokół HTTP
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 80

## PARAMETRÓW

### — Dostęp
Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.
Dopuszczalne wartości tego parametru to: Allow i Deny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### — Opis
Określa opis konfiguracji reguły zabezpieczeń sieci do utworzenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Określa prefiks adresu docelowego.
Dopuszczalne wartości tego parametru to:
- Adres międzydomenowy (Classless indomain Routing) 
- Zakres docelowego adresu IP 
- Symbol wieloznaczny (*), aby dopasować dowolny adres IP, za pomocą których można korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły. Nie można go użyć z parametrem "DestinationAddressPrefix".

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły. Nie można go użyć z parametrem "DestinationAddressPrefix".

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Określa port docelowy lub zakres.
Dopuszczalne wartości tego parametru to:
- Liczba całkowita
- Zakres liczb całkowitych z zakresu od 0 do 65535
- Znak wieloznaczny (*), aby dopasować port

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direction
Określa, czy reguła jest obliczana na ruch przychodzący lub wychodzący.
Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konfiguracji reguł zabezpieczeń sieci, którą to polecenie cmdlet tworzy.

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

### -Priority (priorytet)
Określa priorytet konfiguracji reguły.
Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.
Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.
Niższy numer priorytetu, wyższy priorytet reguły.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół sieciowy, którego dotyczy Nowa konfiguracja reguły.
Dopuszczalne wartości tego parametru to:
- Protokoł
- Obsługiwane
- Symbol wieloznaczny (*), aby dopasować oba te znaki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Określa prefiks adresu źródłowego.
Dopuszczalne wartości tego parametru to:
- CIDR
- Zakres źródłowy adresu IP
- Znak wieloznaczny (*), aby dopasować dowolny adres IP.
Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły. Nie można go użyć z parametrem "SourceAddressPrefix".

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły. Nie można go użyć z parametrem "SourceAddressPrefix".

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Określa port źródłowy lub zakres.
Dopuszczalne wartości tego parametru to:
- Liczba całkowita
- Zakres liczb całkowitych z zakresu od 0 do 65535
- Znak wieloznaczny (*), aby dopasować port

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSSecurityRule

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


