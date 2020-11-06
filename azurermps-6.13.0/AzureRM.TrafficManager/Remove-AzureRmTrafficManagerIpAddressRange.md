---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525918"
---
# <span data-ttu-id="63337-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="63337-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="63337-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63337-102">SYNOPSIS</span></span>
<span data-ttu-id="63337-103">Usuwa zakres adresów lub podsieć z obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="63337-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63337-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63337-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63337-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63337-105">DESCRIPTION</span></span>
<span data-ttu-id="63337-106">Polecenie cmdlet **Remove-AzureRmTrafficManagerIpAddressRange** usuwa zakres adresów IP z obiektu punktu końcowego lokalnego programu Azure Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="63337-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="63337-107">Punkt końcowy można uzyskać przy użyciu New-AzureRmTrafficManagerEndpoint lub Get-AzureRmTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63337-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="63337-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="63337-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="63337-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="63337-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63337-110">EXAMPLES</span></span>

### <span data-ttu-id="63337-111">Przykład 1: usuwanie zakresów adresów IP z punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="63337-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="63337-112">Pierwsze polecenie uzyskuje punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="63337-113">Drugie polecenie usuwa zakres adresów IP z punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="63337-114">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="63337-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63337-115">PARAMETERS</span></span>

### <span data-ttu-id="63337-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63337-116">-DefaultProfile</span></span>
<span data-ttu-id="63337-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63337-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63337-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="63337-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="63337-119">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="63337-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="63337-120">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="63337-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="63337-121">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint lub New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="63337-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63337-122">-Confirm</span></span>
<span data-ttu-id="63337-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63337-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63337-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63337-124">-WhatIf</span></span>
<span data-ttu-id="63337-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63337-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63337-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63337-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63337-127">-First</span><span class="sxs-lookup"><span data-stu-id="63337-127">-First</span></span>
<span data-ttu-id="63337-128">Określa pierwszy adres IP z zakresu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="63337-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="63337-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63337-129">CommonParameters</span></span>
<span data-ttu-id="63337-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63337-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63337-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63337-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63337-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63337-132">INPUTS</span></span>

### <span data-ttu-id="63337-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="63337-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="63337-134">To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63337-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="63337-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63337-135">OUTPUTS</span></span>

### <span data-ttu-id="63337-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="63337-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="63337-137">To polecenie cmdlet zwraca zmodyfikowany obiekt TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63337-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="63337-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63337-138">NOTES</span></span>

## <span data-ttu-id="63337-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63337-139">RELATED LINKS</span></span>

[<span data-ttu-id="63337-140">Dodaj-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="63337-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="63337-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63337-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="63337-142">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="63337-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="63337-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="63337-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
