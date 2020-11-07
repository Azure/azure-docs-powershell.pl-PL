---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718566"
---
# <span data-ttu-id="891ae-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="891ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="891ae-102">SYNOPSIS</span></span>
<span data-ttu-id="891ae-103">Tworzy profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="891ae-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="891ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="891ae-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="891ae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="891ae-105">DESCRIPTION</span></span>
<span data-ttu-id="891ae-106">Polecenie cmdlet **New-AzureRmTrafficManagerProfile** tworzy profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="891ae-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="891ae-107">Określ parametr *name* oraz wymagane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="891ae-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="891ae-108">To polecenie cmdlet zwraca obiekt lokalny reprezentujący nowy profil.</span><span class="sxs-lookup"><span data-stu-id="891ae-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="891ae-109">To polecenie cmdlet nie powoduje skonfigurowania punktów końcowych w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="891ae-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="891ae-110">Obiekt profilu lokalnego można zaktualizować przy użyciu polecenia cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="891ae-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="891ae-111">Następnie Przekaż zmiany w usłudze Traffic Manager przy użyciu Set-AzureRmTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891ae-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="891ae-112">Możesz też dodać punkty końcowe przy użyciu New-AzureRmTrafficManagerEndpoint polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891ae-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="891ae-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="891ae-113">EXAMPLES</span></span>

### <span data-ttu-id="891ae-114">Przykład 1. Tworzenie profilu</span><span class="sxs-lookup"><span data-stu-id="891ae-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="891ae-115">To polecenie tworzy profil usługi Azure Traffic Manager o nazwie ContosoProfile w grupie zasób ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="891ae-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="891ae-116">Nazwa FQDN DNS to contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="891ae-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="891ae-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="891ae-117">PARAMETERS</span></span>

### <span data-ttu-id="891ae-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="891ae-118">-CustomHeader</span></span>
<span data-ttu-id="891ae-119">Lista niestandardowych par nazw nagłówków i wartości dla żądań sondujące.</span><span class="sxs-lookup"><span data-stu-id="891ae-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="891ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-120">-DefaultProfile</span></span>
<span data-ttu-id="891ae-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="891ae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891ae-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="891ae-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="891ae-123">Lista oczekiwanych zakresów kodów stanu HTTP dla żądań sondujące.</span><span class="sxs-lookup"><span data-stu-id="891ae-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="891ae-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="891ae-124">-MaxReturn</span></span>
<span data-ttu-id="891ae-125">Maksymalna liczba odpowiedzi zwracanych w przypadku profilów przy użyciu metody routingu z wieloma wartościami.</span><span class="sxs-lookup"><span data-stu-id="891ae-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="891ae-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="891ae-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="891ae-127">Interwał (w sekundach) sprawdzania kondycji poszczególnych punktów końcowych w tym profilu przez Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="891ae-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="891ae-128">Wartość domyślna to 30.</span><span class="sxs-lookup"><span data-stu-id="891ae-128">The default is 30.</span></span>

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

### <span data-ttu-id="891ae-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="891ae-129">-MonitorPath</span></span>
<span data-ttu-id="891ae-130">Określa ścieżkę używaną do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="891ae-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="891ae-131">Określ wartość odnoszącą się do nazwy domeny punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="891ae-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="891ae-132">Ta wartość musi zaczynać się od ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="891ae-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="891ae-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="891ae-133">-MonitorPort</span></span>
<span data-ttu-id="891ae-134">Określa port TCP, który jest wykorzystywany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="891ae-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="891ae-135">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 65535.</span><span class="sxs-lookup"><span data-stu-id="891ae-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="891ae-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="891ae-136">-MonitorProtocol</span></span>
<span data-ttu-id="891ae-137">Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="891ae-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="891ae-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="891ae-138">Valid values are:</span></span>

- <span data-ttu-id="891ae-139">URL</span><span class="sxs-lookup"><span data-stu-id="891ae-139">HTTP</span></span>
- <span data-ttu-id="891ae-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="891ae-140">HTTPS</span></span>

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

### <span data-ttu-id="891ae-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="891ae-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="891ae-142">Czas (w sekundach), w którym Menedżer ruchu umożliwia reagowanie punktów końcowych w tym profilu na kontrolę kondycji.</span><span class="sxs-lookup"><span data-stu-id="891ae-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="891ae-143">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="891ae-143">The default is 10.</span></span>

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

### <span data-ttu-id="891ae-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="891ae-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="891ae-145">Liczba kolejnych nieprawidłowych testów kondycji, które czekają przed zadeklarowaniem punktu końcowego w tym profilu po następnym kolejnym sprawdzeniu kondycji.</span><span class="sxs-lookup"><span data-stu-id="891ae-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="891ae-146">Wartość domyślna to 3.</span><span class="sxs-lookup"><span data-stu-id="891ae-146">The default is 3.</span></span>

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

### <span data-ttu-id="891ae-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="891ae-147">-Name</span></span>
<span data-ttu-id="891ae-148">Określa nazwę profilu usługi Traffic Managera, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891ae-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="891ae-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="891ae-149">-ProfileStatus</span></span>
<span data-ttu-id="891ae-150">Określa stan profilu.</span><span class="sxs-lookup"><span data-stu-id="891ae-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="891ae-151">Prawidłowe wartości to: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="891ae-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="891ae-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="891ae-152">-RelativeDnsName</span></span>
<span data-ttu-id="891ae-153">Określa względną nazwę DNS, jaką zapewnia dany profil usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="891ae-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="891ae-154">Usługa Traffic Manager łączy tę wartość i nazwę domeny DNS używaną przez usługę Azure Traffic Manager do utworzenia w pełni kwalifikowanej nazwy domeny (FQDN) profilu.</span><span class="sxs-lookup"><span data-stu-id="891ae-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="891ae-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="891ae-155">-ResourceGroupName</span></span>
<span data-ttu-id="891ae-156">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="891ae-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="891ae-157">To polecenie cmdlet tworzy profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="891ae-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="891ae-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="891ae-158">-Tag</span></span>
<span data-ttu-id="891ae-159">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="891ae-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="891ae-160">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="891ae-160">For example:</span></span>

<span data-ttu-id="891ae-161">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="891ae-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="891ae-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="891ae-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="891ae-163">Określa metodę routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="891ae-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="891ae-164">Ta metoda określa, który Menedżer ruchu punktu końcowego zwraca odpowiedź na przychodzące kwerendy DNS.</span><span class="sxs-lookup"><span data-stu-id="891ae-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="891ae-165">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="891ae-165">Valid values are:</span></span>

- <span data-ttu-id="891ae-166">Pracy</span><span class="sxs-lookup"><span data-stu-id="891ae-166">Performance</span></span>
- <span data-ttu-id="891ae-167">Ważona</span><span class="sxs-lookup"><span data-stu-id="891ae-167">Weighted</span></span>
- <span data-ttu-id="891ae-168">Priorytet</span><span class="sxs-lookup"><span data-stu-id="891ae-168">Priority</span></span>
- <span data-ttu-id="891ae-169">Geograficznego</span><span class="sxs-lookup"><span data-stu-id="891ae-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891ae-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="891ae-170">-Ttl</span></span>
<span data-ttu-id="891ae-171">Określa wartość TTL (czas wygaśnięcia).</span><span class="sxs-lookup"><span data-stu-id="891ae-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="891ae-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891ae-172">CommonParameters</span></span>
<span data-ttu-id="891ae-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891ae-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891ae-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="891ae-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891ae-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="891ae-175">INPUTS</span></span>

### <span data-ttu-id="891ae-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="891ae-176">None</span></span>
<span data-ttu-id="891ae-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="891ae-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="891ae-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="891ae-178">OUTPUTS</span></span>

### <span data-ttu-id="891ae-179">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="891ae-180">To polecenie cmdlet zwraca nowy obiekt TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="891ae-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="891ae-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="891ae-181">NOTES</span></span>

## <span data-ttu-id="891ae-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="891ae-182">RELATED LINKS</span></span>

[<span data-ttu-id="891ae-183">Dodaj-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="891ae-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="891ae-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="891ae-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="891ae-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="891ae-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="891ae-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="891ae-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


