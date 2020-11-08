---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232912"
---
# <span data-ttu-id="4b4eb-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="4b4eb-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="4b4eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4eb-103">Usuwa zakres adresów lub podsieć z obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="4b4eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b4eb-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b4eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4eb-106">Polecenie cmdlet **Remove-AzTrafficManagerIpAddressRange** usuwa zakres adresów IP z obiektu punktu końcowego lokalnego programu Azure Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="4b4eb-107">Punkt końcowy można uzyskać przy użyciu New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="4b4eb-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="4b4eb-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="4b4eb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b4eb-110">EXAMPLES</span></span>

### <span data-ttu-id="4b4eb-111">Przykład 1: usuwanie zakresów adresów IP z punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="4b4eb-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="4b4eb-112">Pierwsze polecenie uzyskuje punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="4b4eb-113">Drugie polecenie usuwa zakres adresów IP z punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="4b4eb-114">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="4b4eb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b4eb-115">PARAMETERS</span></span>

### <span data-ttu-id="4b4eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4eb-116">-DefaultProfile</span></span>
<span data-ttu-id="4b4eb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b4eb-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4eb-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="4b4eb-119">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="4b4eb-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="4b4eb-120">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4b4eb-121">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="4b4eb-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b4eb-122">-Confirm</span></span>
<span data-ttu-id="4b4eb-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4eb-124">-WhatIf</span></span>
<span data-ttu-id="4b4eb-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b4eb-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4eb-127">-First</span><span class="sxs-lookup"><span data-stu-id="4b4eb-127">-First</span></span>
<span data-ttu-id="4b4eb-128">Określa pierwszy adres IP z zakresu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="4b4eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4eb-129">CommonParameters</span></span>
<span data-ttu-id="4b4eb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4eb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4eb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4eb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b4eb-132">INPUTS</span></span>

### <span data-ttu-id="4b4eb-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4eb-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b4eb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b4eb-134">OUTPUTS</span></span>

### <span data-ttu-id="4b4eb-135">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4eb-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b4eb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b4eb-136">NOTES</span></span>

## <span data-ttu-id="4b4eb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b4eb-137">RELATED LINKS</span></span>

[<span data-ttu-id="4b4eb-138">Dodaj-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="4b4eb-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="4b4eb-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b4eb-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="4b4eb-140">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4eb-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="4b4eb-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4eb-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
