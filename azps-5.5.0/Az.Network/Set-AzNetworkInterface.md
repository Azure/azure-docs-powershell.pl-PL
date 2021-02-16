---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186851"
---
# Set-AzNetworkInterface

## SYNOPSIS
Aktualizuje interfejs sieciowy.

## SKŁADNIA

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
**Set-AzNetworkInterface** aktualizuje interfejs sieciowy.

## PRZYKŁADY

### Przykład 1. Konfigurowanie interfejsu sieciowego
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

W tym przykładzie skonfigurowano interfejs sieciowy.
Pierwsze polecenie otrzymuje interfejs sieciowy o nazwie NetworkInterface1 w grupie zasobów ResourceGroup1.
Drugie polecenie ustawia prywatny adres IP konfiguracji ip.
Trzecie polecenie ustawia dla prywatnej metody alokacji adresów IP ustawienie Statyczne.
Czwarte polecenie ustawia tag w interfejsie sieciowym.
Piąte polecenie używa informacji przechowywanych w $Nic sieciowej do ustawienia interfejsu sieciowego.

### Przykład 2. Zmienianie ustawień DNS w interfejsie sieciowym
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Pierwsze polecenie otrzymuje interfejs sieciowy o nazwie NetworkInterface1, który istnieje w grupie zasobów ResourceGroup1. Drugie polecenie dodaje do tego interfejsu serwer DNS 192.168.1.100. Trzecie polecenie powoduje zastosowanie tych zmian do interfejsu sieciowego. Aby usunąć serwer DNS, postępuj zgodnie z poleceniami wymienionymi powyżej, ale zastąp ". Dodaj" z ". Usuń" w drugim poleceniu.

### Przykład 3. Włączanie przesyłania dalej adresów IP w interfejsie sieciowym
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie NetworkInterface1 i przechowuje je w $nic zmienną. Drugie polecenie zmienia wartość przesyłania dalej adresów IP na prawda. Trzecie polecenie powoduje zastosowanie zmian do interfejsu sieciowego. Aby wyłączyć przesyłanie dalej adresów IP w interfejsie sieciowym, wykonaj przykład, ale pamiętaj, aby zmienić drugie polecenie na "$nic. EnableIPForwarding = 0".

### Przykład 4. Zmienianie podsieci interfejsu sieciowego
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Pierwsze polecenie pobiera interfejs sieciowy NetworkInterface1 i zapisuje je w zmiennej $nic sieci. Drugie polecenie pobiera sieć wirtualną skojarzoną z podsiecią, z która zostanie skojarzony interfejs sieciowy. Drugie polecenie pobiera podsieci i przechowuje je w zmiennej $subnet 2. Trzecie polecenie skojarzyło podstawowy prywatny adres IP interfejsu sieciowego z nową podsiecią. Ostatnie polecenie zastosować te zmiany w interfejsie sieciowym.
>[!NOTE] 
>Konfiguracje adresów IP muszą być dynamiczne, aby można było zmienić podsieci. Jeśli masz statyczne konfiguracje ADRESÓW IP, zmień je na dynamiczne przed rozpoczęciem pracy. 
>[!NOTE]
>Jeśli interfejs sieciowy ma wiele konfiguracji adresów IP, należy wykonać następujące polecenie dla wszystkich tych konfiguracji adresów IP, zanim zostanie Set-AzNetworkInterface wykonania ostatecznego polecenia adresu IP. Można to zrobić zgodnie z poleceniami, ale zamieniając liczbę "0" na odpowiednią liczbę. Jeśli interfejs sieciowy ma konfiguracje protokołu IP N, musi istnieć N-1 tych poleceń.

### Przykład 5. Kojarzenie/kojarzenie grupy zabezpieczeń sieciowych z interfejsem sieciowym
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie NetworkInterface1 i przechowuje je w $nic zmienną. Drugie polecenie pobiera istniejącą grupę zabezpieczeń sieciową o nazwie MyNSG i przechowuje ją w $nsg sieci. Trzecie polecenie przypisuje $nsg do $nic. Na koniec polecenie z drugiej strony powoduje zastosowanie zmian do interfejsu sieciowego. Aby rozdzielić grupy zabezpieczeń sieciowych z interfejsu sieciowego, $nsg zastąpić je trzecim poleceniem $null.

## PARAMETERS

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

### - NetworkInterface
Określa obiekt interfejsu sieciowego reprezentujący stan, dla którego powinien zostać ustawiony interfejs sieciowy.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTATKI

## LINKI POKREWNE

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
