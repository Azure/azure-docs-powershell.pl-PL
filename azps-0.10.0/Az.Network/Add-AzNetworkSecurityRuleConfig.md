---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890954"
---
# Add-AzNetworkSecurityRuleConfig

## STRESZCZENIe
Dodaje konfigurację reguły zabezpieczeń sieci do grupy zabezpieczeń sieci.

## POLECENIA

### SetByResource (domyślny)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzNetworkSecurityRuleConfig** umożliwia dodanie konfiguracji reguł zabezpieczeń sieci do grupy zabezpieczeń sieci platformy Azure.

## Przykłady

### 1: Dodawanie grupy zabezpieczeń sieci
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Pierwsze polecenie pobiera grupę zabezpieczeń sieci Azure o nazwie "nsg1" z grupy zasobów "RG1". Drugie polecenie dodaje regułę zabezpieczeń sieci o nazwie "RDP-Rule", która umożliwia ruch z Internetu na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci. Utrzymuje zmienioną grupę zabezpieczeń sieci Azure.

### 1: Dodawanie nowej reguły zabezpieczeń za pomocą grup zabezpieczeń aplikacji
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Najpierw tworzymy dwie nowe grupy zabezpieczeń aplikacji. Następnie pobieramy grupę zabezpieczeń sieci Azure o nazwie "nsg1" z grupy zasobów "RG1". i Dodaj do niej regułę zabezpieczeń sieci o nazwie "RDP-Rule". Reguła zezwala na ruch ze wszystkich konfiguracji adresów IP w grupie zabezpieczeń aplikacji "srcAsg" do wszystkich konfiguracji adresów IP w "destAsg" na porcie 3389. Po dodaniu reguły zachowywana jest Twoja zmieniona Grupa zabezpieczeń sieci Azure.

## PARAMETRÓW

### — Dostęp
Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.
Dopuszczalne wartości tego parametru to: Allow i Deny.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Opis
Określa opis konfiguracji reguły zabezpieczeń sieci.

```yaml
Type: String
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
- Znak wieloznaczny (*), aby dopasować dowolny adres IP

Możesz korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: String
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
Określa nazwę konfiguracji reguł zabezpieczeń sieci.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Określa obiekt **NetworkSecurityGroup** .
To polecenie cmdlet umożliwia dodanie konfiguracji reguły zabezpieczeń sieci do obiektu, który ten parametr określa.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority (priorytet)
Określa priorytet konfiguracji reguły.
Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.

Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.
Niższy numer priorytetu, wyższy priorytet reguły.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół sieciowy, którego dotyczy konfiguracja reguły.
Dopuszczalne wartości tego parametru to:

- Protokoł
- Obsługiwane
- Symbol wieloznaczny (*), aby dopasować oba znaki

```yaml
Type: String
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
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
Ta wartość jest wyrażona jako liczba całkowita z zakresu od 0 do 65535 lub jako symbol wieloznaczny (*) w celu dopasowania dowolnego portu źródłowego.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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

### PSNetworkSecurityGroup
Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup

## INFORMACYJN

## LINKI POKREWNE

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Nowe — AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


