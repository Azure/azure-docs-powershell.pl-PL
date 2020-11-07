---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892777"
---
# Set-AzLoadBalancerProbeConfig

## STRESZCZENIe
Umożliwia ustawienie stanu celu dla konfiguracji sondy.

## POLECENIA

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzLoadBalancerProbeConfig** ustawia stan celu dla konfiguracji sondy.

## Przykłady

### Przykład 1: modyfikowanie konfiguracji sondy w usłudze równoważenia obciążenia
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

Pierwsze polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.

Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerProbeConfig, które umożliwia dodanie nowej konfiguracji sondy.

Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancerProbeConfig** , co ustawia nową konfigurację.
Należy zauważyć, że konieczne jest określenie kilku parametrów, które zostały określone w poprzednim poleceniu, ponieważ są one wymagane przez bieżące polecenie cmdlet.

## PARAMETRÓW

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

### -IntervalInSeconds
Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Moduł równoważenia obciążenia
Umożliwia określenie modułu równoważenia obciążenia.
To polecenie cmdlet ustawia stan celu dla konfiguracji sondy dla modułu równoważenia obciążenia, który określa ten parametr.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konfiguracji sondy, która jest ustawiana przez to polecenie cmdlet.

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

### -Port
Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeCount
Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół, który ma być używany do sondowania.
Dopuszczalne wartości tego parametru to: TCP lub http.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestPath
Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSLoadBalancer
Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSLoadBalancer

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzLoadBalancerProbeConfig](./Add-AzLoadBalancerProbeConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerProbeConfig](./Get-AzLoadBalancerProbeConfig.md)

[Nowe — AzLoadBalancerProbeConfig](./New-AzLoadBalancerProbeConfig.md)

[Remove-AzLoadBalancerProbeConfig](./Remove-AzLoadBalancerProbeConfig.md)


