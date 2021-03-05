---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 11481d2063b6acb2938361726de45f72dba539c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960426"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
Dodaje konfigurację reguły zabezpieczeń sieciowych do grupy zabezpieczeń sieci.

## SKŁADNIA

### SetByResource (Domyślne)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzNetworkSecurityRuleConfig** dodaje konfigurację reguły zabezpieczeń sieciowych do grupy zabezpieczeń sieci platformy Azure.

## PRZYKŁADY

### 1. Dodawanie grupy zabezpieczeń sieciowych
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Pierwsze polecenie pobiera grupę zabezpieczeń sieci azure o nazwie "nsg1" z grupy zasobów "rg1". Drugie polecenie dodaje regułę zabezpieczeń sieci o nazwie "reguła rdp", która zezwala na ruch z Internetu na porcie 3389 do obiektu pobranej grupy zabezpieczeń sieci. Utrzymuje zmodyfikowaną grupę zabezpieczeń sieci platformy Azure.

### 2. Dodawanie nowej reguły zabezpieczeń za pomocą grup zabezpieczeń aplikacji
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Najpierw tworzymy dwie nowe grupy zabezpieczeń aplikacji. Następnie pobieramy grupę zabezpieczeń sieci azure o nazwie "nsg1" z grupy zasobów "rg1". i dodaj do tej reguły regułę zabezpieczeń sieciową o nazwie "reguła rdp". Ta reguła zezwala na ruch ze wszystkich konfiguracji adresów IP w grupie zabezpieczeń aplikacji "srcAsg" do wszystkich konfiguracji adresów IP w ciągu "destAsg" na porcie 3389. Po dodaniu reguły zachowywana jest zmodyfikowana grupa zabezpieczeń sieci platformy Azure.

## PARAMETERS

### — Access
Określa, czy ruch sieciowy jest dozwolony, czy odrzucony.
Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).

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
Określa opis konfiguracji reguły zabezpieczeń sieci.

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
Określa nazwę konfiguracji reguły zabezpieczeń sieci.

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
Określa obiekt **NetworkSecurityGroup.**
To polecenie cmdlet dodaje konfigurację reguły zabezpieczeń sieci do obiektu, który określa ten parametr.

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
Dopuszczalne wartości dla tego parametru to: liczba całkowita z między 100 a 4096.
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
Dopuszczalne wartości dla tego parametru to:
- Tcp
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
- Symbol wieloznaczny (*) do dopasowania dowolnego adresu IP.
Możesz również używać tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

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
Ta wartość jest wyrażana jako liczba całkowita, w zakresie od 0 do 65 535 lub jako symbol wieloznaczny (*) w celu dopasowania do dowolnego portu źródłowego.

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

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


