---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241603"
---
# <span data-ttu-id="54379-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="54379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54379-102">SYNOPSIS</span></span>
<span data-ttu-id="54379-103">Dodaje niestandardowe informacje nagłówka do lokalnego obiektu końcowego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="54379-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="54379-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54379-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54379-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="54379-105">DESCRIPTION</span></span>
<span data-ttu-id="54379-106">Polecenie **cmdlet Add-AzTrafficManagerCustomHeaderToEndpoint** dodaje niestandardowe informacje nagłówka do lokalnego obiektu końcowego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="54379-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="54379-107">Punkt końcowy można uzyskać za pomocą New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54379-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="54379-108">To polecenie cmdlet działa na lokalnym obiekcie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="54379-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="54379-109">Zatwierdzanie zmian w punkcie końcowym usługi Traffic Manager za pomocą Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54379-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="54379-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54379-110">EXAMPLES</span></span>

### <span data-ttu-id="54379-111">Przykład 1. Dodawanie niestandardowych informacji nagłówka do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="54379-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="54379-112">Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="54379-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="54379-113">Polecenie przechowuje lokalny punkt końcowy w $TrafficManagerEndpoint zmienną.</span><span class="sxs-lookup"><span data-stu-id="54379-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="54379-114">Drugie polecenie dodaje niestandardowe informacje nagłówka do punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="54379-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="54379-115">Ostatnie polecenie aktualizuje punkt końcowy w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="54379-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="54379-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54379-116">PARAMETERS</span></span>

### <span data-ttu-id="54379-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54379-117">-DefaultProfile</span></span>
<span data-ttu-id="54379-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54379-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54379-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="54379-119">-Name</span></span>
<span data-ttu-id="54379-120">Określa nazwę nagłówka niestandardowego do dodania.</span><span class="sxs-lookup"><span data-stu-id="54379-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="54379-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="54379-122">Określa lokalny **obiekt TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="54379-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="54379-123">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="54379-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="54379-124">Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54379-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="54379-125">— Wartość</span><span class="sxs-lookup"><span data-stu-id="54379-125">-Value</span></span>
<span data-ttu-id="54379-126">Określa wartość niestandardowych informacji nagłówka do dodania.</span><span class="sxs-lookup"><span data-stu-id="54379-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="54379-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54379-127">-Confirm</span></span>
<span data-ttu-id="54379-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54379-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54379-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54379-129">-WhatIf</span></span>
<span data-ttu-id="54379-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54379-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54379-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="54379-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54379-132">CommonParameters</span></span>
<span data-ttu-id="54379-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54379-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54379-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54379-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54379-135">INPUTS</span></span>

### <span data-ttu-id="54379-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="54379-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54379-137">OUTPUTS</span></span>

### <span data-ttu-id="54379-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="54379-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54379-139">NOTES</span></span>

## <span data-ttu-id="54379-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54379-140">RELATED LINKS</span></span>

[<span data-ttu-id="54379-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="54379-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="54379-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54379-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="54379-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54379-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
