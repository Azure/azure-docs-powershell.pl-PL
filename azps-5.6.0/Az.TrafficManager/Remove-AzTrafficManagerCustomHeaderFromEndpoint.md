---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987288"
---
# <span data-ttu-id="9d57a-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="9d57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d57a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d57a-103">Usuwa niestandardowe informacje nagłówka z lokalnego obiektu końcowego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="9d57a-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="9d57a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d57a-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d57a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d57a-105">DESCRIPTION</span></span>
<span data-ttu-id="9d57a-106">Polecenie **cmdlet Remove-AzTrafficManagerCustomHeaderFromEndpoint** usuwa niestandardowe informacje nagłówka z lokalnego obiektu końcowego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9d57a-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="9d57a-107">Punkt końcowy można uzyskać za pomocą New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d57a-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="9d57a-108">To polecenie cmdlet działa na lokalnym obiekcie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9d57a-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="9d57a-109">Zatwierdzanie zmian w punkcie końcowym usługi Traffic Manager za pomocą Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d57a-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9d57a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d57a-110">EXAMPLES</span></span>

### <span data-ttu-id="9d57a-111">Przykład 1. Usuwanie informacji z niestandardowej podsieci z punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="9d57a-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9d57a-112">Pierwsze polecenie pobiera punkt końcowy platformy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $TrafficManagerEndpoint zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d57a-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="9d57a-113">Drugie polecenie usuwa niestandardowe informacje nagłówka z punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d57a-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="9d57a-114">Ostatnie polecenie aktualizuje punkt końcowy w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d57a-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9d57a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d57a-115">PARAMETERS</span></span>

### <span data-ttu-id="9d57a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d57a-116">-DefaultProfile</span></span>
<span data-ttu-id="9d57a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d57a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d57a-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d57a-118">-Name</span></span>
<span data-ttu-id="9d57a-119">Określa nazwę nagłówka niestandardowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9d57a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="9d57a-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9d57a-121">Określa lokalny obiekt **TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="9d57a-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9d57a-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="9d57a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9d57a-123">Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d57a-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="9d57a-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d57a-124">-Confirm</span></span>
<span data-ttu-id="9d57a-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d57a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d57a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d57a-126">-WhatIf</span></span>
<span data-ttu-id="9d57a-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d57a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d57a-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d57a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d57a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d57a-129">CommonParameters</span></span>
<span data-ttu-id="9d57a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d57a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d57a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d57a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d57a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d57a-132">INPUTS</span></span>

### <span data-ttu-id="9d57a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9d57a-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d57a-134">OUTPUTS</span></span>

### <span data-ttu-id="9d57a-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9d57a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d57a-136">NOTES</span></span>

## <span data-ttu-id="9d57a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d57a-137">RELATED LINKS</span></span>

[<span data-ttu-id="9d57a-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="9d57a-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d57a-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9d57a-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9d57a-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d57a-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
