---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707389"
---
# <span data-ttu-id="67126-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="67126-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67126-102">SYNOPSIS</span></span>
<span data-ttu-id="67126-103">Dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="67126-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="67126-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67126-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67126-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67126-105">DESCRIPTION</span></span>
<span data-ttu-id="67126-106">Polecenie cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="67126-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="67126-107">Punkt końcowy można uzyskać przy użyciu New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67126-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="67126-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="67126-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="67126-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="67126-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="67126-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67126-110">EXAMPLES</span></span>

### <span data-ttu-id="67126-111">Przykład 1: Dodawanie niestandardowych informacji nagłówka do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="67126-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="67126-112">Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="67126-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="67126-113">Polecenie zapisuje lokalny punkt końcowy w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="67126-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="67126-114">Drugie polecenie dodaje niestandardowe informacje nagłówka do punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="67126-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="67126-115">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="67126-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="67126-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67126-116">PARAMETERS</span></span>

### <span data-ttu-id="67126-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67126-117">-DefaultProfile</span></span>
<span data-ttu-id="67126-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67126-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67126-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67126-119">-Name</span></span>
<span data-ttu-id="67126-120">Określa nazwę informacji nagłówka niestandardowego, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="67126-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="67126-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="67126-122">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="67126-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="67126-123">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="67126-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="67126-124">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="67126-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="67126-125">-Value</span><span class="sxs-lookup"><span data-stu-id="67126-125">-Value</span></span>
<span data-ttu-id="67126-126">Określa wartość niestandardowych informacji nagłówka, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="67126-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="67126-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67126-127">-Confirm</span></span>
<span data-ttu-id="67126-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67126-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67126-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67126-129">-WhatIf</span></span>
<span data-ttu-id="67126-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67126-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67126-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67126-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67126-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67126-132">CommonParameters</span></span>
<span data-ttu-id="67126-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67126-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67126-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67126-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67126-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67126-135">INPUTS</span></span>

### <span data-ttu-id="67126-136">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="67126-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67126-137">OUTPUTS</span></span>

### <span data-ttu-id="67126-138">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="67126-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67126-139">NOTES</span></span>

## <span data-ttu-id="67126-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67126-140">RELATED LINKS</span></span>

[<span data-ttu-id="67126-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="67126-142">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="67126-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="67126-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="67126-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="67126-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)