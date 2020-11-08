---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054919"
---
# <span data-ttu-id="3253f-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="3253f-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="3253f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3253f-102">SYNOPSIS</span></span>
<span data-ttu-id="3253f-103">Modyfikuje wszystkie punkty końcowe w zestawie modułów równoważenia obciążenia w ramach usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="3253f-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="3253f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3253f-104">SYNTAX</span></span>

### <span data-ttu-id="3253f-105">DefaultProbe (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3253f-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3253f-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="3253f-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3253f-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="3253f-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3253f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3253f-108">DESCRIPTION</span></span>
<span data-ttu-id="3253f-109">Polecenie cmdlet **Set-AzureLoadBalancedEndpoint** modyfikuje wszystkie punkty końcowe w zestawie modułów równoważenia obciążenia w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3253f-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="3253f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3253f-110">EXAMPLES</span></span>

### <span data-ttu-id="3253f-111">Przykład 1: modyfikowanie punktów końcowych w zestawie modułów równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3253f-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="3253f-112">To polecenie powoduje zmodyfikowanie wszystkich punktów końcowych zestawu modułów równoważenia obciążenia o nazwie LBSet01 w celu użycia protokołu TCP i portu prywatnego 80.</span><span class="sxs-lookup"><span data-stu-id="3253f-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="3253f-113">To polecenie ustawia sondę modułu równoważenia obciążenia w celu użycia protokołu TCP na porcie 8080.</span><span class="sxs-lookup"><span data-stu-id="3253f-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="3253f-114">Przykład 2: Określanie innego wirtualnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="3253f-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="3253f-115">To polecenie powoduje zmodyfikowanie modułu równoważenia obciążenia z nazwą zestawu modułów równoważenia obciążenia w celu używania wirtualnego adresu IP o nazwie Vip01.</span><span class="sxs-lookup"><span data-stu-id="3253f-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="3253f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3253f-116">PARAMETERS</span></span>

### <span data-ttu-id="3253f-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="3253f-117">-ACL</span></span>
<span data-ttu-id="3253f-118">Określa obiekt konfiguracji listy kontroli dostępu (ACL), którego to polecenie cmdlet dotyczy punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="3253f-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="3253f-119">-DirectServerReturn</span></span>
<span data-ttu-id="3253f-120">Określa, czy to polecenie cmdlet włącza bezpośrednią zwracanie serwera.</span><span class="sxs-lookup"><span data-stu-id="3253f-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="3253f-121">Określ, $True włączyć lub $False do wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="3253f-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3253f-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3253f-123">Określa okres czasu bezczynności protokołu TCP (w minutach) dla punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="3253f-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="3253f-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3253f-124">-InformationAction</span></span>
<span data-ttu-id="3253f-125">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="3253f-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3253f-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3253f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3253f-127">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="3253f-127">Continue</span></span>
- <span data-ttu-id="3253f-128">Ignorować</span><span class="sxs-lookup"><span data-stu-id="3253f-128">Ignore</span></span>
- <span data-ttu-id="3253f-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="3253f-129">Inquire</span></span>
- <span data-ttu-id="3253f-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3253f-130">SilentlyContinue</span></span>
- <span data-ttu-id="3253f-131">Przestaw</span><span class="sxs-lookup"><span data-stu-id="3253f-131">Stop</span></span>
- <span data-ttu-id="3253f-132">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="3253f-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3253f-133">-InformationVariable</span></span>
<span data-ttu-id="3253f-134">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="3253f-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3253f-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="3253f-136">Określa nazwę wewnętrznego modułu równoważenia obciążenia, które obejmuje ten aplet polecenia w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3253f-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="3253f-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="3253f-137">-LBSetName</span></span>
<span data-ttu-id="3253f-138">Określa nazwę zestawu modułów równoważenia obciążenia, które są aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3253f-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3253f-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="3253f-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="3253f-140">Określa algorytm dystrybucji modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3253f-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="3253f-141">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3253f-141">Valid values are:</span></span> 

- <span data-ttu-id="3253f-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="3253f-142">sourceIP.</span></span>
<span data-ttu-id="3253f-143">Koligacja dwóch krotek: źródłowy adres IP, docelowy adres IP</span><span class="sxs-lookup"><span data-stu-id="3253f-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="3253f-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="3253f-144">sourceIPProtocol.</span></span>
<span data-ttu-id="3253f-145">Koligacja trzech krotek: źródłowy adres IP, docelowy adres IP, protokół</span><span class="sxs-lookup"><span data-stu-id="3253f-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="3253f-146">znaleziono.</span><span class="sxs-lookup"><span data-stu-id="3253f-146">none.</span></span>
<span data-ttu-id="3253f-147">Koligacja pięciu krotek: źródłowy adres IP, port źródłowy, docelowy adres IP, port docelowy, protokół</span><span class="sxs-lookup"><span data-stu-id="3253f-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="3253f-148">Wartość domyślna to None.</span><span class="sxs-lookup"><span data-stu-id="3253f-148">The default value is none.</span></span>

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

### <span data-ttu-id="3253f-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="3253f-149">-LocalPort</span></span>
<span data-ttu-id="3253f-150">Określa lokalny, prywatny, port, którego używają te punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="3253f-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="3253f-151">Aplikacje na maszynie wirtualnej nasłuchują na tym porcie żądań wejścia usług dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3253f-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="3253f-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3253f-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="3253f-153">Określa interwał sondowania sondy (w sekundach) dla punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="3253f-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="3253f-154">-ProbePath</span></span>
<span data-ttu-id="3253f-155">Określa względną ścieżkę badania HTTP.</span><span class="sxs-lookup"><span data-stu-id="3253f-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="3253f-156">-ProbePort</span></span>
<span data-ttu-id="3253f-157">Określa port używany przez sondę modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3253f-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="3253f-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="3253f-159">Określa, że punkty końcowe modułu równoważenia obciążenia wykorzystują sondę HTTP.</span><span class="sxs-lookup"><span data-stu-id="3253f-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="3253f-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="3253f-161">Określa, że punkty końcowe modułu równoważenia obciążenia wykorzystują sondę TCP.</span><span class="sxs-lookup"><span data-stu-id="3253f-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3253f-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="3253f-163">Określa limit czasu sondowania sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3253f-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-164">-Profile</span><span class="sxs-lookup"><span data-stu-id="3253f-164">-Profile</span></span>
<span data-ttu-id="3253f-165">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3253f-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3253f-166">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3253f-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-167">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="3253f-167">-Protocol</span></span>
<span data-ttu-id="3253f-168">Określa protokół punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="3253f-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="3253f-169">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3253f-169">Valid values are:</span></span> 

- <span data-ttu-id="3253f-170">PROTOKOŁ</span><span class="sxs-lookup"><span data-stu-id="3253f-170">TCP</span></span> 
- <span data-ttu-id="3253f-171">OBSŁUGIWANE</span><span class="sxs-lookup"><span data-stu-id="3253f-171">UDP</span></span>

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

### <span data-ttu-id="3253f-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="3253f-172">-PublicPort</span></span>
<span data-ttu-id="3253f-173">Określa port publiczny używany przez punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3253f-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="3253f-174">Jeśli wartość nie zostanie określona, platforma Azure przypisze dostępny port.</span><span class="sxs-lookup"><span data-stu-id="3253f-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="3253f-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3253f-175">-ServiceName</span></span>
<span data-ttu-id="3253f-176">Określa nazwę usługi platformy Azure zawierającej punkty końcowe, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3253f-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3253f-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="3253f-177">-VirtualIPName</span></span>
<span data-ttu-id="3253f-178">Określa nazwę wirtualnego adresu IP, który jest skojarzony z platformą Azure do punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="3253f-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="3253f-179">Aby dodać wirtualne adresy IP do usługi, użyj polecenia cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="3253f-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="3253f-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3253f-180">CommonParameters</span></span>
<span data-ttu-id="3253f-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3253f-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3253f-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3253f-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3253f-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3253f-183">INPUTS</span></span>

## <span data-ttu-id="3253f-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3253f-184">OUTPUTS</span></span>

## <span data-ttu-id="3253f-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3253f-185">NOTES</span></span>

## <span data-ttu-id="3253f-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3253f-186">RELATED LINKS</span></span>

[<span data-ttu-id="3253f-187">Dodaj-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3253f-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="3253f-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3253f-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


