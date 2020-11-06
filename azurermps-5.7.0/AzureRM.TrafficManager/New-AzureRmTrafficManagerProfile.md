---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544043"
---
# <span data-ttu-id="34202-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="34202-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34202-102">SYNOPSIS</span></span>
<span data-ttu-id="34202-103">Tworzy profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="34202-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34202-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34202-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34202-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34202-105">DESCRIPTION</span></span>
<span data-ttu-id="34202-106">Polecenie cmdlet **New-AzureRmTrafficManagerProfile** tworzy profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="34202-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="34202-107">Określ parametr *name* oraz wymagane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="34202-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="34202-108">To polecenie cmdlet zwraca obiekt lokalny reprezentujący nowy profil.</span><span class="sxs-lookup"><span data-stu-id="34202-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="34202-109">To polecenie cmdlet nie powoduje skonfigurowania punktów końcowych w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="34202-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="34202-110">Obiekt profilu lokalnego można zaktualizować przy użyciu polecenia cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="34202-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="34202-111">Następnie Przekaż zmiany w usłudze Traffic Manager przy użyciu Set-AzureRmTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34202-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="34202-112">Możesz też dodać punkty końcowe przy użyciu New-AzureRmTrafficManagerEndpoint polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34202-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="34202-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34202-113">EXAMPLES</span></span>

### <span data-ttu-id="34202-114">Przykład 1. Tworzenie profilu</span><span class="sxs-lookup"><span data-stu-id="34202-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="34202-115">To polecenie tworzy profil usługi Azure Traffic Manager o nazwie ContosoProfile w grupie zasób ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="34202-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="34202-116">Nazwa FQDN DNS to contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="34202-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="34202-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34202-117">PARAMETERS</span></span>

### <span data-ttu-id="34202-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34202-118">-DefaultProfile</span></span>
<span data-ttu-id="34202-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34202-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34202-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="34202-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="34202-121">Interwał (w sekundach) sprawdzania kondycji poszczególnych punktów końcowych w tym profilu przez Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="34202-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="34202-122">Wartość domyślna to 30.</span><span class="sxs-lookup"><span data-stu-id="34202-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="34202-123">-MonitorPath</span></span>
<span data-ttu-id="34202-124">Określa ścieżkę używaną do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="34202-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="34202-125">Określ wartość odnoszącą się do nazwy domeny punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="34202-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="34202-126">Ta wartość musi zaczynać się od ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="34202-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="34202-127">-MonitorPort</span></span>
<span data-ttu-id="34202-128">Określa port TCP, który jest wykorzystywany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="34202-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="34202-129">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 65535.</span><span class="sxs-lookup"><span data-stu-id="34202-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="34202-130">-MonitorProtocol</span></span>
<span data-ttu-id="34202-131">Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="34202-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="34202-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="34202-132">Valid values are:</span></span>

- <span data-ttu-id="34202-133">URL</span><span class="sxs-lookup"><span data-stu-id="34202-133">HTTP</span></span>
- <span data-ttu-id="34202-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="34202-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="34202-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="34202-136">Czas (w sekundach), w którym Menedżer ruchu umożliwia reagowanie punktów końcowych w tym profilu na kontrolę kondycji.</span><span class="sxs-lookup"><span data-stu-id="34202-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="34202-137">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="34202-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="34202-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="34202-139">Liczba kolejnych nieprawidłowych testów kondycji, które czekają przed zadeklarowaniem punktu końcowego w tym profilu po następnym kolejnym sprawdzeniu kondycji.</span><span class="sxs-lookup"><span data-stu-id="34202-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="34202-140">Wartość domyślna to 3.</span><span class="sxs-lookup"><span data-stu-id="34202-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34202-141">-Name</span></span>
<span data-ttu-id="34202-142">Określa nazwę profilu usługi Traffic Managera, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34202-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="34202-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="34202-143">-ProfileStatus</span></span>
<span data-ttu-id="34202-144">Określa stan profilu.</span><span class="sxs-lookup"><span data-stu-id="34202-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="34202-145">Prawidłowe wartości to: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="34202-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="34202-146">-RelativeDnsName</span></span>
<span data-ttu-id="34202-147">Określa względną nazwę DNS, jaką zapewnia dany profil usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="34202-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="34202-148">Usługa Traffic Manager łączy tę wartość i nazwę domeny DNS używaną przez usługę Azure Traffic Manager do utworzenia w pełni kwalifikowanej nazwy domeny (FQDN) profilu.</span><span class="sxs-lookup"><span data-stu-id="34202-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="34202-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34202-149">-ResourceGroupName</span></span>
<span data-ttu-id="34202-150">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34202-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="34202-151">To polecenie cmdlet tworzy profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="34202-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34202-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="34202-152">-Tag</span></span>
<span data-ttu-id="34202-153">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="34202-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="34202-154">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="34202-154">For example:</span></span>

<span data-ttu-id="34202-155">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="34202-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="34202-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="34202-157">Określa metodę routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="34202-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="34202-158">Ta metoda określa, który Menedżer ruchu punktu końcowego zwraca odpowiedź na przychodzące kwerendy DNS.</span><span class="sxs-lookup"><span data-stu-id="34202-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="34202-159">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="34202-159">Valid values are:</span></span>

- <span data-ttu-id="34202-160">Pracy</span><span class="sxs-lookup"><span data-stu-id="34202-160">Performance</span></span>
- <span data-ttu-id="34202-161">Ważona</span><span class="sxs-lookup"><span data-stu-id="34202-161">Weighted</span></span>
- <span data-ttu-id="34202-162">Priorytet</span><span class="sxs-lookup"><span data-stu-id="34202-162">Priority</span></span>
- <span data-ttu-id="34202-163">Geograficznego</span><span class="sxs-lookup"><span data-stu-id="34202-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-164">-TTL</span><span class="sxs-lookup"><span data-stu-id="34202-164">-Ttl</span></span>
<span data-ttu-id="34202-165">Określa wartość TTL (czas wygaśnięcia).</span><span class="sxs-lookup"><span data-stu-id="34202-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34202-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34202-166">CommonParameters</span></span>
<span data-ttu-id="34202-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34202-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34202-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34202-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34202-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34202-169">INPUTS</span></span>

### <span data-ttu-id="34202-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34202-170">None</span></span>
<span data-ttu-id="34202-171">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="34202-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34202-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34202-172">OUTPUTS</span></span>

### <span data-ttu-id="34202-173">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="34202-174">To polecenie cmdlet zwraca nowy obiekt TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="34202-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="34202-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34202-175">NOTES</span></span>

## <span data-ttu-id="34202-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34202-176">RELATED LINKS</span></span>

[<span data-ttu-id="34202-177">Dodaj-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="34202-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="34202-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="34202-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="34202-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="34202-181">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="34202-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34202-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


