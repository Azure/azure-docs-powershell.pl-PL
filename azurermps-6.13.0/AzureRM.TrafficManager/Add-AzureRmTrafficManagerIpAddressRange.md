---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525953"
---
# <span data-ttu-id="5683b-101">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="5683b-101">Add-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="5683b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5683b-102">SYNOPSIS</span></span>
<span data-ttu-id="5683b-103">Dodaje zakres adresów lub podsieć do obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="5683b-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5683b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5683b-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5683b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5683b-105">DESCRIPTION</span></span>
<span data-ttu-id="5683b-106">Polecenie cmdlet **Add-AzureRmTrafficManagerIpAddressRange** umożliwia dodanie zakresu adresów IP do obiektu punktu końcowego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="5683b-106">The **Add-AzureRmTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="5683b-107">Punkt końcowy można uzyskać przy użyciu New-AzureRmTrafficManagerEndpoint lub Get-AzureRmTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5683b-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="5683b-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5683b-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="5683b-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="5683b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5683b-110">EXAMPLES</span></span>

### <span data-ttu-id="5683b-111">Przykład 1: Dodawanie zakresów adresów IP do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="5683b-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="5683b-112">Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="5683b-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="5683b-113">Polecenie zapisuje lokalny punkt końcowy w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="5683b-114">Drugie polecenie dodaje zakres adresów IP 1.2.3.4, aby 5.6.7.8 do punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5683b-115">Trzecie polecenie dodaje zakres adresów IP 9.10.11.0 do 9.10.11.255 w punkcie końcowym przechowywanym w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5683b-116">Czwarte polecenie sprawdza, czy zakres jest zgodny z rozmiarem zakresu, a następnie dodaje zakres adresów IP 12.13.14.0 do 12.13.14.31 w punkcie końcowym przechowywanym w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5683b-117">Piąte polecenie powoduje dodanie zakresu adresów IP 15.16.17.18 do 15.16.17.18 w punkcie końcowym przechowywanym w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5683b-118">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="5683b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5683b-119">PARAMETERS</span></span>

### <span data-ttu-id="5683b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5683b-120">-DefaultProfile</span></span>
<span data-ttu-id="5683b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5683b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5683b-122">-Last</span><span class="sxs-lookup"><span data-stu-id="5683b-122">-Last</span></span>
<span data-ttu-id="5683b-123">Określa ostatni adres IP w zakresie, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="5683b-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="5683b-124">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5683b-124">-Scope</span></span>
<span data-ttu-id="5683b-125">Określa zakres zakresu adresów IP, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="5683b-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5683b-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5683b-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5683b-127">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="5683b-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="5683b-128">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="5683b-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5683b-129">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint lub New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5683b-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5683b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5683b-130">-Confirm</span></span>
<span data-ttu-id="5683b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5683b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5683b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5683b-132">-WhatIf</span></span>
<span data-ttu-id="5683b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5683b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5683b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5683b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5683b-135">-First</span><span class="sxs-lookup"><span data-stu-id="5683b-135">-First</span></span>
<span data-ttu-id="5683b-136">Określa pierwszy adres IP w zakresie, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="5683b-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="5683b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5683b-137">CommonParameters</span></span>
<span data-ttu-id="5683b-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5683b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5683b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5683b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5683b-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5683b-140">INPUTS</span></span>

### <span data-ttu-id="5683b-141">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5683b-141">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="5683b-142">To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5683b-142">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="5683b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5683b-143">OUTPUTS</span></span>

### <span data-ttu-id="5683b-144">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5683b-144">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="5683b-145">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="5683b-145">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="5683b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5683b-146">NOTES</span></span>

## <span data-ttu-id="5683b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5683b-147">RELATED LINKS</span></span>

[<span data-ttu-id="5683b-148">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="5683b-148">Remove-AzureRmTrafficManagerIpAddressRange</span></span>](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="5683b-149">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5683b-149">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5683b-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5683b-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5683b-151">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5683b-151">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
