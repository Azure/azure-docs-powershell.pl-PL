---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180659"
---
# <span data-ttu-id="fa050-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="fa050-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="fa050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa050-102">SYNOPSIS</span></span>
<span data-ttu-id="fa050-103">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa050-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa050-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa050-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa050-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa050-105">DESCRIPTION</span></span>
<span data-ttu-id="fa050-106">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa050-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa050-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa050-107">EXAMPLES</span></span>

### <span data-ttu-id="fa050-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa050-108">Example 1</span></span>
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

<span data-ttu-id="fa050-109">Tworzenie obiektu PSBackendPool do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="fa050-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fa050-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa050-110">PARAMETERS</span></span>

### <span data-ttu-id="fa050-111">- Backend</span><span class="sxs-lookup"><span data-stu-id="fa050-111">-Backend</span></span>
<span data-ttu-id="fa050-112">Zestaw zaplecza dla tej puli.</span><span class="sxs-lookup"><span data-stu-id="fa050-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="fa050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa050-113">-DefaultProfile</span></span>
<span data-ttu-id="fa050-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa050-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="fa050-115">-FrontDoorName</span></span>
<span data-ttu-id="fa050-116">Nazwa drzwi frontowych, do których należy ta reguła przekierowania.</span><span class="sxs-lookup"><span data-stu-id="fa050-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="fa050-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="fa050-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="fa050-118">Nazwa ustawień kondycji tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="fa050-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="fa050-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="fa050-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="fa050-120">Nazwa ustawień równoważenia obciążenia dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="fa050-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="fa050-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fa050-121">-Name</span></span>
<span data-ttu-id="fa050-122">Nazwa backendPool.</span><span class="sxs-lookup"><span data-stu-id="fa050-122">BackendPool name.</span></span>

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

### <span data-ttu-id="fa050-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa050-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa050-124">Nazwa grupy zasobów, w których zostanie utworzony routingRule.</span><span class="sxs-lookup"><span data-stu-id="fa050-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="fa050-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa050-125">CommonParameters</span></span>
<span data-ttu-id="fa050-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa050-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa050-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa050-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa050-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa050-128">INPUTS</span></span>

### <span data-ttu-id="fa050-129">Brak</span><span class="sxs-lookup"><span data-stu-id="fa050-129">None</span></span>

## <span data-ttu-id="fa050-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa050-130">OUTPUTS</span></span>

### <span data-ttu-id="fa050-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="fa050-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="fa050-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa050-132">NOTES</span></span>

## <span data-ttu-id="fa050-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa050-133">RELATED LINKS</span></span>

<span data-ttu-id="fa050-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="fa050-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
