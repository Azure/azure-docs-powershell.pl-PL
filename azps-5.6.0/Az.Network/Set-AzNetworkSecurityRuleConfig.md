---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003274"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.

## SKŁADNIA

### SetByResource (Domyślne)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzNetworkSecurityRuleConfig** aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieciowych.

## PRZYKŁADY

### Przykład 1. Zmienianie konfiguracji dostępu w regułę zabezpieczeń sieci
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Pierwsze polecenie pobiera grupę zabezpieczeń sieci o nazwie NSG-FrontEnd, a następnie przechowuje ją w zmiennej $nsg.
Drugie polecenie przekaże grupę zabezpieczeń w programie $nsg do strony Get-AzNetworkSecurityRuleConfig, która pobiera konfigurację reguł zabezpieczeń o nazwie rdp-rule.
Trzecie polecenie zmienia konfigurację dostępu reguły rdp na Odmów. Spowoduje to jednak zastąpienie reguły i ustawienie tylko parametrów przekazywanych do Set-AzNetworkSecurityRuleConfig sieci.   UWAGA: Nie można zmienić pojedynczego atrybutu

### Przykład 2

Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci. (wygenerowane automatycznie)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARAMETERS

### — Access
Określa, czy ruch sieciowy jest dozwolony, czy odrzucony. Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).

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

### — Opis
Określa opis konfiguracji reguły.
Maksymalny rozmiar to 140 znaków.

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
Dopuszczalne wartości dla tego parametru to:
- Adres routingu międzydomenowego (CIDR, Classless Interdomain Routing) 
- Zakres docelowych adresów IP 
- Symbol wieloznaczny (*) do dopasowania dowolnego adresu IP Możesz użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

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
Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły. Nie można jej używać z parametrem "DestinationAddressPrefix".

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
Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły. Nie można jej używać z parametrem "DestinationAddressPrefix".

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
Określa port lub zakres docelowy.
Dopuszczalne wartości dla tego parametru to:
- Liczba całkowita 
- Zakres liczb całkowitych z zakresu od 0 do 65535
- Symbol wieloznaczny (*) do dopasowania dowolnego portu

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

### — Kierunek
Określa, czy reguła jest szacowana dla ruchu przychodzącego lub wychodzącego.
Dopuszczalne wartości dla tego parametru to: Przychodzący i wychodzący.

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

### — Nazwa
Określa nazwę konfiguracji reguły zabezpieczeń sieciowych ustawianą przez to polecenie cmdlet.

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

### - NetworkSecurityGroup
Określa obiekt **NetworkSecurityGroup** zawierający konfigurację reguły zabezpieczeń sieci, która ma być ustawiona.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Priority (Priorytet)
Określa priorytet konfiguracji reguły.
Dopuszczalne wartości dla tego parametru to:Liczba całkowita z między 100 a 4096.
Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.
Im niższy numer priorytetu, tym wyższy priorytet reguły.

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

### — Protokół
Określa protokół sieciowy, do których ma zastosowanie konfiguracja reguły.
Dopuszczalne wartości dla tego parametru to: --Tcp
- Udp
- Symbol wieloznaczny (*) do dopasowania obu

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
Dopuszczalne wartości dla tego parametru to:
- A CIDR
- Źródłowy zakres adresów IP
- Symbol wieloznaczny (*) do dopasowania dowolnego adresu IP Możesz również użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

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
Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły. Nie można jej używać z parametrem "SourceAddressPrefix".

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
Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły. Nie można jej używać z parametrem "SourceAddressPrefix".

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
Określa port lub zakres źródłowy.
Dopuszczalne wartości dla tego parametru to:
- Liczba całkowita
- Zakres liczb całkowitych z zakresu od 0 do 65535
- Symbol wieloznaczny (*) do dopasowania dowolnego portu

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## NOTATKI

## LINKI POKREWNE

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


