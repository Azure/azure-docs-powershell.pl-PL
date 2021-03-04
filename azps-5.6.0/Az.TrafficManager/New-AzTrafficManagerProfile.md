---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: a17f88a23399fda7f4775ca52fbe1d4aec35594d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950817"
---
# <span data-ttu-id="9617b-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="9617b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9617b-102">SYNOPSIS</span></span>
<span data-ttu-id="9617b-103">Tworzy profil Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="9617b-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="9617b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9617b-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9617b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9617b-105">DESCRIPTION</span></span>
<span data-ttu-id="9617b-106">Polecenie **cmdlet New-AzTrafficManagerProfile** tworzy profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9617b-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9617b-107">Określ parametr *Name* i wymagane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="9617b-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="9617b-108">To polecenie cmdlet zwraca obiekt lokalny reprezentujący nowy profil.</span><span class="sxs-lookup"><span data-stu-id="9617b-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="9617b-109">To polecenie cmdlet nie konfiguruje punktów końcowych menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="9617b-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="9617b-110">Obiekt profilu lokalnego można zaktualizować za pomocą Add-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9617b-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="9617b-111">Następnie przekaż zmiany do Menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9617b-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9617b-112">Możesz również dodać punkty końcowe za pomocą New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9617b-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9617b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9617b-113">EXAMPLES</span></span>

### <span data-ttu-id="9617b-114">Przykład 1. Tworzenie profilu</span><span class="sxs-lookup"><span data-stu-id="9617b-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="9617b-115">To polecenie tworzy profil usługi Azure Traffic Manager o nazwie ContosoProfile w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9617b-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="9617b-116">Nazwa FQDN DNS contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="9617b-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="9617b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9617b-117">PARAMETERS</span></span>

### <span data-ttu-id="9617b-118">- CustomHeader</span><span class="sxs-lookup"><span data-stu-id="9617b-118">-CustomHeader</span></span>
<span data-ttu-id="9617b-119">Lista niestandardowych par nazw nagłówków i wartości dla żądań zakupu.</span><span class="sxs-lookup"><span data-stu-id="9617b-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-120">-DefaultProfile</span></span>
<span data-ttu-id="9617b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9617b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9617b-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9617b-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="9617b-123">Lista przewidywanych zakresów kodów stanu HTTP dla żądań użytkowników.</span><span class="sxs-lookup"><span data-stu-id="9617b-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-124">— MaxReturn</span><span class="sxs-lookup"><span data-stu-id="9617b-124">-MaxReturn</span></span>
<span data-ttu-id="9617b-125">Maksymalna liczba odpowiedzi zwróconych dla profilów przy użyciu metody routingu wielowartościowego.</span><span class="sxs-lookup"><span data-stu-id="9617b-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9617b-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="9617b-127">Interwał (w sekundach), w którym Menedżer ruchu sprawdzi kondycję każdego punktu końcowego w tym profilu.</span><span class="sxs-lookup"><span data-stu-id="9617b-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="9617b-128">Wartość domyślna to 30.</span><span class="sxs-lookup"><span data-stu-id="9617b-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-129">- MonitorPath</span><span class="sxs-lookup"><span data-stu-id="9617b-129">-MonitorPath</span></span>
<span data-ttu-id="9617b-130">Określa ścieżkę używaną do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9617b-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="9617b-131">Określ wartość względem nazwy domeny punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9617b-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="9617b-132">Ta wartość musi rozpoczynać się od ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="9617b-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-133">- MonitorPort</span><span class="sxs-lookup"><span data-stu-id="9617b-133">-MonitorPort</span></span>
<span data-ttu-id="9617b-134">Określa port TCP używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9617b-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="9617b-135">Prawidłowe wartości to liczby całkowite z od 1 do 65535.</span><span class="sxs-lookup"><span data-stu-id="9617b-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="9617b-136">-MonitorProtocol</span></span>
<span data-ttu-id="9617b-137">Określa protokół używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9617b-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="9617b-138">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="9617b-138">Valid values are:</span></span>

- <span data-ttu-id="9617b-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="9617b-139">HTTP</span></span>
- <span data-ttu-id="9617b-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9617b-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="9617b-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="9617b-142">Czas (w sekundach), na który Menedżer ruchu zezwala punktom końcowym w tym profilu na reagowanie na sprawdzanie kondycji.</span><span class="sxs-lookup"><span data-stu-id="9617b-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="9617b-143">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9617b-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="9617b-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="9617b-145">Liczba następujących po sobie testów kondycji, których kondycja nie powiodła się, przez menedżera ruchu, przed zadeklarowaniem punktu końcowego w tym profilu o pogorszeniu po kolejnym sprawdzaniu kondycji, która zakończyła się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9617b-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="9617b-146">Wartość domyślna to 3.</span><span class="sxs-lookup"><span data-stu-id="9617b-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9617b-147">-Name</span></span>
<span data-ttu-id="9617b-148">Określa nazwę profilu menedżera ruchu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9617b-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9617b-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="9617b-149">-ProfileStatus</span></span>
<span data-ttu-id="9617b-150">Określa stan profilu.</span><span class="sxs-lookup"><span data-stu-id="9617b-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="9617b-151">Prawidłowe wartości to: Włączone i Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="9617b-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="9617b-152">-RelativeDnsName</span></span>
<span data-ttu-id="9617b-153">Określa względną nazwę DNS udostępnianą przez ten profil menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="9617b-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="9617b-154">Menedżer ruchu łączy tę wartość i nazwę domeny DNS używaną przez usługę Azure Traffic Manager do postaci w pełni kwalifikowanej nazwy domeny (FQDN) profilu.</span><span class="sxs-lookup"><span data-stu-id="9617b-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="9617b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9617b-155">-ResourceGroupName</span></span>
<span data-ttu-id="9617b-156">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9617b-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9617b-157">To polecenie cmdlet tworzy w grupie profil menedżera ruchu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9617b-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9617b-158">— Tag</span><span class="sxs-lookup"><span data-stu-id="9617b-158">-Tag</span></span>
<span data-ttu-id="9617b-159">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze.</span><span class="sxs-lookup"><span data-stu-id="9617b-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9617b-160">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="9617b-160">For example:</span></span>

<span data-ttu-id="9617b-161">@{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9617b-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-162">- TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="9617b-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="9617b-163">Określa metodę routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="9617b-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="9617b-164">Ta metoda określa, który punkt końcowy Traffic Manager zwraca w odpowiedzi na przychodzące zapytania DNS.</span><span class="sxs-lookup"><span data-stu-id="9617b-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="9617b-165">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="9617b-165">Valid values are:</span></span>

- <span data-ttu-id="9617b-166">Wydajność</span><span class="sxs-lookup"><span data-stu-id="9617b-166">Performance</span></span>
- <span data-ttu-id="9617b-167">Ważone</span><span class="sxs-lookup"><span data-stu-id="9617b-167">Weighted</span></span>
- <span data-ttu-id="9617b-168">Priorytet</span><span class="sxs-lookup"><span data-stu-id="9617b-168">Priority</span></span>
- <span data-ttu-id="9617b-169">Region geograficzny</span><span class="sxs-lookup"><span data-stu-id="9617b-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-170">— Ttl</span><span class="sxs-lookup"><span data-stu-id="9617b-170">-Ttl</span></span>
<span data-ttu-id="9617b-171">Określa wartość czasu wygaśnięcia (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="9617b-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9617b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9617b-172">CommonParameters</span></span>
<span data-ttu-id="9617b-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9617b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9617b-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9617b-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9617b-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9617b-175">INPUTS</span></span>

### <span data-ttu-id="9617b-176">Brak</span><span class="sxs-lookup"><span data-stu-id="9617b-176">None</span></span>

## <span data-ttu-id="9617b-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9617b-177">OUTPUTS</span></span>

### <span data-ttu-id="9617b-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9617b-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9617b-179">NOTES</span></span>

## <span data-ttu-id="9617b-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9617b-180">RELATED LINKS</span></span>

[<span data-ttu-id="9617b-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9617b-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9617b-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9617b-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9617b-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9617b-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="9617b-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9617b-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


