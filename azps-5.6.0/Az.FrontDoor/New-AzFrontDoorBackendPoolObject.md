---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965905"
---
# <span data-ttu-id="fa7d7-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="fa7d7-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="fa7d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7d7-103">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa7d7-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa7d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa7d7-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa7d7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="fa7d7-106">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa7d7-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa7d7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa7d7-107">EXAMPLES</span></span>

### <span data-ttu-id="fa7d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa7d7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="fa7d7-109">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa7d7-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa7d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="fa7d7-111">- Backend</span><span class="sxs-lookup"><span data-stu-id="fa7d7-111">-Backend</span></span>
<span data-ttu-id="fa7d7-112">Zestaw zaplecza dla tej puli.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7d7-113">-DefaultProfile</span></span>
<span data-ttu-id="fa7d7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7d7-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="fa7d7-115">-FrontDoorName</span></span>
<span data-ttu-id="fa7d7-116">Nazwa drzwi frontowych, do których należy ta reguła przekierowania.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="fa7d7-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="fa7d7-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="fa7d7-118">Nazwa ustawień kondycji tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="fa7d7-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="fa7d7-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="fa7d7-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="fa7d7-120">Nazwa ustawień równoważenia obciążenia dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="fa7d7-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="fa7d7-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fa7d7-121">-Name</span></span>
<span data-ttu-id="fa7d7-122">Nazwa backendPool.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-122">BackendPool name.</span></span>

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

### <span data-ttu-id="fa7d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa7d7-124">Nazwa grupy zasobów, w których zostanie utworzony routingRule.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="fa7d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7d7-125">CommonParameters</span></span>
<span data-ttu-id="fa7d7-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7d7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa7d7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7d7-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa7d7-128">INPUTS</span></span>

### <span data-ttu-id="fa7d7-129">Brak</span><span class="sxs-lookup"><span data-stu-id="fa7d7-129">None</span></span>

## <span data-ttu-id="fa7d7-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa7d7-130">OUTPUTS</span></span>

### <span data-ttu-id="fa7d7-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="fa7d7-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="fa7d7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa7d7-132">NOTES</span></span>

## <span data-ttu-id="fa7d7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa7d7-133">RELATED LINKS</span></span>

<span data-ttu-id="fa7d7-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="fa7d7-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
