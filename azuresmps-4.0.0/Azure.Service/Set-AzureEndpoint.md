---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055023"
---
# <span data-ttu-id="8f2bb-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2bb-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="8f2bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2bb-103">Modyfikuje punkt końcowy przypisany do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="8f2bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f2bb-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8f2bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f2bb-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2bb-106">Polecenie cmdlet **Set-AzureEndpoint** modyfikuje punkt końcowy przypisany do maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="8f2bb-107">Możesz określić zmiany w punkcie końcowym, który nie jest zrównoważony względem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="8f2bb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f2bb-108">EXAMPLES</span></span>

### <span data-ttu-id="8f2bb-109">Przykład 1: modyfikowanie punktu końcowego w celu nasłuchiwania na porcie</span><span class="sxs-lookup"><span data-stu-id="8f2bb-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="8f2bb-110">To polecenie pobiera konfigurację maszyny wirtualnej o nazwie VirtualMachine01 przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8f2bb-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="8f2bb-111">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f2bb-112">To polecenie cmdlet modyfikuje punkt końcowy o nazwie sieć Web w celu odsłuchiwania na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="8f2bb-113">Polecenie przekazuje obiekt maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="8f2bb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f2bb-114">PARAMETERS</span></span>

### <span data-ttu-id="8f2bb-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="8f2bb-115">-ACL</span></span>
<span data-ttu-id="8f2bb-116">Określa obiekt konfiguracji listy kontroli dostępu (ACL), którego to polecenie cmdlet dotyczy punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="8f2bb-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="8f2bb-117">-DirectServerReturn</span></span>
<span data-ttu-id="8f2bb-118">Określa, czy to polecenie cmdlet włącza bezpośrednią zwracanie serwera.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="8f2bb-119">Określ, $True włączyć lub $False do wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="8f2bb-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8f2bb-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8f2bb-121">Określa okres czasu bezczynności protokołu TCP (w minutach) dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="8f2bb-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8f2bb-122">-InformationAction</span></span>
<span data-ttu-id="8f2bb-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8f2bb-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f2bb-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f2bb-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="8f2bb-125">Continue</span></span>
- <span data-ttu-id="8f2bb-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="8f2bb-126">Ignore</span></span>
- <span data-ttu-id="8f2bb-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="8f2bb-127">Inquire</span></span>
- <span data-ttu-id="8f2bb-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8f2bb-128">SilentlyContinue</span></span>
- <span data-ttu-id="8f2bb-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="8f2bb-129">Stop</span></span>
- <span data-ttu-id="8f2bb-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="8f2bb-130">Suspend</span></span>

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

### <span data-ttu-id="8f2bb-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8f2bb-131">-InformationVariable</span></span>
<span data-ttu-id="8f2bb-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8f2bb-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="8f2bb-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="8f2bb-134">Określa nazwę wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="8f2bb-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="8f2bb-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="8f2bb-136">Określa algorytm dystrybucji modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="8f2bb-137">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8f2bb-137">Valid values are:</span></span> 

- <span data-ttu-id="8f2bb-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-138">sourceIP.</span></span>
<span data-ttu-id="8f2bb-139">Koligacja dwóch krotek: źródłowy adres IP, docelowy adres IP</span><span class="sxs-lookup"><span data-stu-id="8f2bb-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="8f2bb-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-140">sourceIPProtocol.</span></span>
<span data-ttu-id="8f2bb-141">Koligacja trzech krotek: źródłowy adres IP, docelowy adres IP, protokół</span><span class="sxs-lookup"><span data-stu-id="8f2bb-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="8f2bb-142">znaleziono.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-142">none.</span></span>
<span data-ttu-id="8f2bb-143">Koligacja pięciu krotek: źródłowy adres IP, port źródłowy, docelowy adres IP, port docelowy, protokół</span><span class="sxs-lookup"><span data-stu-id="8f2bb-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="8f2bb-144">Wartość domyślna to None.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-144">The default value is none.</span></span>

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

### <span data-ttu-id="8f2bb-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="8f2bb-145">-LocalPort</span></span>
<span data-ttu-id="8f2bb-146">Określa lokalny, prywatny, port, którego używa dany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="8f2bb-147">Aplikacje w ramach maszyny wirtualnej nasłuchują na tym porcie żądań wejścia usług dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bb-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f2bb-148">-Name</span></span>
<span data-ttu-id="8f2bb-149">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-149">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bb-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="8f2bb-150">-Profile</span></span>
<span data-ttu-id="8f2bb-151">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f2bb-152">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f2bb-153">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="8f2bb-153">-Protocol</span></span>
<span data-ttu-id="8f2bb-154">Określa protokół punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="8f2bb-155">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8f2bb-155">Valid values are:</span></span> 

- <span data-ttu-id="8f2bb-156">protokoł</span><span class="sxs-lookup"><span data-stu-id="8f2bb-156">tcp</span></span> 
- <span data-ttu-id="8f2bb-157">obsługiwane</span><span class="sxs-lookup"><span data-stu-id="8f2bb-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bb-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="8f2bb-158">-PublicPort</span></span>
<span data-ttu-id="8f2bb-159">Określa port publiczny używany przez punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="8f2bb-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="8f2bb-160">-VirtualIPName</span></span>
<span data-ttu-id="8f2bb-161">Określa nazwę wirtualnego adresu IP, który jest skojarzony z platformą Azure do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="8f2bb-162">Usługa może mieć wiele wirtualnych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="8f2bb-163">Aby utworzyć wirtualne adresy IP, użyj polecenia cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="8f2bb-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="8f2bb-164">-VM</span><span class="sxs-lookup"><span data-stu-id="8f2bb-164">-VM</span></span>
<span data-ttu-id="8f2bb-165">Umożliwia określenie maszyny wirtualnej, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2bb-166">CommonParameters</span></span>
<span data-ttu-id="8f2bb-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2bb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2bb-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2bb-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2bb-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f2bb-169">INPUTS</span></span>

## <span data-ttu-id="8f2bb-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f2bb-170">OUTPUTS</span></span>

### <span data-ttu-id="8f2bb-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="8f2bb-171">System.Object</span></span>

## <span data-ttu-id="8f2bb-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f2bb-172">NOTES</span></span>

## <span data-ttu-id="8f2bb-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f2bb-173">RELATED LINKS</span></span>

[<span data-ttu-id="8f2bb-174">Dodaj-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2bb-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="8f2bb-175">Dodaj-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="8f2bb-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="8f2bb-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2bb-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="8f2bb-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8f2bb-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8f2bb-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2bb-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="8f2bb-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8f2bb-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


