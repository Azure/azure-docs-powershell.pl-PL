---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054699"
---
# <span data-ttu-id="3aa19-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa19-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="3aa19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3aa19-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa19-103">Dodaje punkt końcowy do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3aa19-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="3aa19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3aa19-104">SYNTAX</span></span>

### <span data-ttu-id="3aa19-105">NoLB (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3aa19-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3aa19-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="3aa19-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3aa19-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="3aa19-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3aa19-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="3aa19-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3aa19-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3aa19-109">DESCRIPTION</span></span>
<span data-ttu-id="3aa19-110">Polecenie cmdlet **Add-AzureEndpoint** umożliwia dodanie punktu końcowego do obiektu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa19-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="3aa19-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3aa19-111">EXAMPLES</span></span>

### <span data-ttu-id="3aa19-112">Przykład 1: Dodawanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="3aa19-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="3aa19-113">To polecenie pobiera konfigurację maszyny wirtualnej o nazwie VirtualMachine01 przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="3aa19-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="3aa19-114">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3aa19-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3aa19-115">To polecenie cmdlet umożliwia dodanie punktu końcowego o nazwie http.</span><span class="sxs-lookup"><span data-stu-id="3aa19-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3aa19-116">Punkt końcowy ma port publiczny 80 i port lokalny 8080.</span><span class="sxs-lookup"><span data-stu-id="3aa19-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3aa19-117">Polecenie przekazuje obiekt maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="3aa19-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="3aa19-118">Przykład 2: Dodawanie punktu końcowego należącego do grupy równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3aa19-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="3aa19-119">To polecenie umożliwia pobranie konfiguracji maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3aa19-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="3aa19-120">Bieżące polecenie cmdlet umożliwia dodanie punktu końcowego o nazwie http.</span><span class="sxs-lookup"><span data-stu-id="3aa19-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3aa19-121">Punkt końcowy ma port publiczny 80 i port lokalny 8080.</span><span class="sxs-lookup"><span data-stu-id="3aa19-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3aa19-122">Punkt końcowy należy do udostępnionej grupy zrównoważonego obciążenia o nazwie webfarmie.</span><span class="sxs-lookup"><span data-stu-id="3aa19-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="3aa19-123">Sonda HTTP na porcie 80 z ścieżką "/" — monitoruje dostępność punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="3aa19-124">To polecenie implementuje zmiany.</span><span class="sxs-lookup"><span data-stu-id="3aa19-124">The command implements your changes.</span></span>

### <span data-ttu-id="3aa19-125">Przykład 3: Kojarzenie wirtualnego adresu IP z punktem końcowym</span><span class="sxs-lookup"><span data-stu-id="3aa19-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="3aa19-126">To polecenie umożliwia pobranie konfiguracji maszyny wirtualnej o nazwie VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="3aa19-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="3aa19-127">Bieżące polecenie cmdlet umożliwia dodanie punktu końcowego o nazwie http.</span><span class="sxs-lookup"><span data-stu-id="3aa19-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3aa19-128">Punkt końcowy ma port publiczny 80 i port lokalny 8080.</span><span class="sxs-lookup"><span data-stu-id="3aa19-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3aa19-129">To polecenie kojarzy wirtualny adres IP z punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="3aa19-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="3aa19-130">To polecenie implementuje zmiany.</span><span class="sxs-lookup"><span data-stu-id="3aa19-130">The command implements your changes.</span></span>

## <span data-ttu-id="3aa19-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3aa19-131">PARAMETERS</span></span>

### <span data-ttu-id="3aa19-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="3aa19-132">-ACL</span></span>
<span data-ttu-id="3aa19-133">Określa obiekt konfiguracji listy kontroli dostępu (ACL) dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="3aa19-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="3aa19-134">-DefaultProbe</span></span>
<span data-ttu-id="3aa19-135">Wskazuje, że w tym poleceniu cmdlet użyto domyślnego ustawienia sondowania.</span><span class="sxs-lookup"><span data-stu-id="3aa19-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="3aa19-136">-DirectServerReturn</span></span>
<span data-ttu-id="3aa19-137">Określa, czy to polecenie cmdlet włącza bezpośrednią zwracanie serwera.</span><span class="sxs-lookup"><span data-stu-id="3aa19-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="3aa19-138">Określ, $True włączyć lub $False do wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="3aa19-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="3aa19-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3aa19-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3aa19-140">Określa okres czasu bezczynności protokołu TCP (w minutach) dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="3aa19-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3aa19-141">-InformationAction</span></span>
<span data-ttu-id="3aa19-142">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="3aa19-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3aa19-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3aa19-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3aa19-144">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="3aa19-144">Continue</span></span>
- <span data-ttu-id="3aa19-145">Ignorować</span><span class="sxs-lookup"><span data-stu-id="3aa19-145">Ignore</span></span>
- <span data-ttu-id="3aa19-146">Inquire</span><span class="sxs-lookup"><span data-stu-id="3aa19-146">Inquire</span></span>
- <span data-ttu-id="3aa19-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3aa19-147">SilentlyContinue</span></span>
- <span data-ttu-id="3aa19-148">Przestaw</span><span class="sxs-lookup"><span data-stu-id="3aa19-148">Stop</span></span>
- <span data-ttu-id="3aa19-149">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="3aa19-149">Suspend</span></span>

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

### <span data-ttu-id="3aa19-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3aa19-150">-InformationVariable</span></span>
<span data-ttu-id="3aa19-151">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="3aa19-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3aa19-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3aa19-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="3aa19-153">Określa nazwę wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3aa19-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="3aa19-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="3aa19-154">-LBSetName</span></span>
<span data-ttu-id="3aa19-155">Określa nazwę zestawu modułu równoważenia obciążenia dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="3aa19-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="3aa19-157">Określa algorytm dystrybucji modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3aa19-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="3aa19-158">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3aa19-158">Valid values are:</span></span> 

- <span data-ttu-id="3aa19-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="3aa19-159">sourceIP.</span></span>
<span data-ttu-id="3aa19-160">Koligacja dwóch krotek: źródłowy adres IP, docelowy adres IP</span><span class="sxs-lookup"><span data-stu-id="3aa19-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="3aa19-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="3aa19-161">sourceIPProtocol.</span></span>
<span data-ttu-id="3aa19-162">Koligacja trzech krotek: źródłowy adres IP, docelowy adres IP, protokół</span><span class="sxs-lookup"><span data-stu-id="3aa19-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="3aa19-163">znaleziono.</span><span class="sxs-lookup"><span data-stu-id="3aa19-163">none.</span></span>
<span data-ttu-id="3aa19-164">Koligacja pięciu krotek: źródłowy adres IP, port źródłowy, docelowy adres IP, port docelowy, protokół</span><span class="sxs-lookup"><span data-stu-id="3aa19-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="3aa19-165">Wartość domyślna to None.</span><span class="sxs-lookup"><span data-stu-id="3aa19-165">The default value is none.</span></span>

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

### <span data-ttu-id="3aa19-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="3aa19-166">-LocalPort</span></span>
<span data-ttu-id="3aa19-167">Określa lokalny, prywatny, port, którego używa dany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3aa19-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="3aa19-168">Aplikacje w ramach maszyny wirtualnej nasłuchują na tym porcie żądań wejścia usług dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-169">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3aa19-169">-Name</span></span>
<span data-ttu-id="3aa19-170">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-170">Specifies a name for the endpoint.</span></span>

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

### <span data-ttu-id="3aa19-171">-Noprobe</span><span class="sxs-lookup"><span data-stu-id="3aa19-171">-NoProbe</span></span>
<span data-ttu-id="3aa19-172">Wskazuje, że w tym poleceniu cmdlet jest używane ustawienie no prob.</span><span class="sxs-lookup"><span data-stu-id="3aa19-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3aa19-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="3aa19-174">Określa interwał sondowania sondy (w sekundach) dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="3aa19-175">-ProbePath</span></span>
<span data-ttu-id="3aa19-176">Określa względną ścieżkę do badania HTTP.</span><span class="sxs-lookup"><span data-stu-id="3aa19-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="3aa19-177">-ProbePort</span></span>
<span data-ttu-id="3aa19-178">Określa port używany przez punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3aa19-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="3aa19-179">-ProbeProtocol</span></span>
<span data-ttu-id="3aa19-180">Określa protokół portów.</span><span class="sxs-lookup"><span data-stu-id="3aa19-180">Specifies the port protocol.</span></span>
<span data-ttu-id="3aa19-181">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3aa19-181">Valid values are:</span></span> 

- <span data-ttu-id="3aa19-182">protokoł</span><span class="sxs-lookup"><span data-stu-id="3aa19-182">tcp</span></span> 
- <span data-ttu-id="3aa19-183">URL</span><span class="sxs-lookup"><span data-stu-id="3aa19-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3aa19-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="3aa19-185">Określa limit czasu sondowania sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3aa19-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-186">-Profile</span><span class="sxs-lookup"><span data-stu-id="3aa19-186">-Profile</span></span>
<span data-ttu-id="3aa19-187">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa19-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3aa19-188">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3aa19-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3aa19-189">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="3aa19-189">-Protocol</span></span>
<span data-ttu-id="3aa19-190">Określa protokół punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="3aa19-191">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3aa19-191">Valid values are:</span></span> 

- <span data-ttu-id="3aa19-192">protokoł</span><span class="sxs-lookup"><span data-stu-id="3aa19-192">tcp</span></span> 
- <span data-ttu-id="3aa19-193">obsługiwane</span><span class="sxs-lookup"><span data-stu-id="3aa19-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa19-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="3aa19-194">-PublicPort</span></span>
<span data-ttu-id="3aa19-195">Określa port publiczny używany przez punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3aa19-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="3aa19-196">Jeśli wartość nie zostanie określona, platforma Azure przypisze dostępny port.</span><span class="sxs-lookup"><span data-stu-id="3aa19-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="3aa19-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="3aa19-197">-VirtualIPName</span></span>
<span data-ttu-id="3aa19-198">Określa nazwę wirtualnego adresu IP, który jest skojarzony z platformą Azure do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3aa19-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="3aa19-199">Usługa może mieć wiele wirtualnych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="3aa19-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="3aa19-200">Aby utworzyć wirtualne adresy IP, użyj polecenia cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="3aa19-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="3aa19-201">-VM</span><span class="sxs-lookup"><span data-stu-id="3aa19-201">-VM</span></span>
<span data-ttu-id="3aa19-202">Umożliwia określenie maszyny wirtualnej, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3aa19-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3aa19-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa19-203">CommonParameters</span></span>
<span data-ttu-id="3aa19-204">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa19-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa19-205">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa19-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa19-206">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aa19-206">INPUTS</span></span>

## <span data-ttu-id="3aa19-207">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3aa19-207">OUTPUTS</span></span>

### <span data-ttu-id="3aa19-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="3aa19-208">System.Object</span></span>

## <span data-ttu-id="3aa19-209">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3aa19-209">NOTES</span></span>

## <span data-ttu-id="3aa19-210">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aa19-210">RELATED LINKS</span></span>

[<span data-ttu-id="3aa19-211">Dodaj-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3aa19-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="3aa19-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa19-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="3aa19-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3aa19-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3aa19-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa19-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="3aa19-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa19-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="3aa19-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3aa19-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


