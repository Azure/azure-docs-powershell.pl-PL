---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231899"
---
# <span data-ttu-id="eac7a-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="eac7a-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="eac7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eac7a-102">SYNOPSIS</span></span>
<span data-ttu-id="eac7a-103">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="eac7a-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="eac7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eac7a-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eac7a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eac7a-105">DESCRIPTION</span></span>
<span data-ttu-id="eac7a-106">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="eac7a-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="eac7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eac7a-107">EXAMPLES</span></span>

### <span data-ttu-id="eac7a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eac7a-108">Example 1</span></span>
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

<span data-ttu-id="eac7a-109">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="eac7a-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="eac7a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eac7a-110">PARAMETERS</span></span>

### <span data-ttu-id="eac7a-111">-Wewnętrzna baza danych</span><span class="sxs-lookup"><span data-stu-id="eac7a-111">-Backend</span></span>
<span data-ttu-id="eac7a-112">Zestaw zakończonych końcem tej puli.</span><span class="sxs-lookup"><span data-stu-id="eac7a-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="eac7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac7a-113">-DefaultProfile</span></span>
<span data-ttu-id="eac7a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eac7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac7a-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="eac7a-115">-FrontDoorName</span></span>
<span data-ttu-id="eac7a-116">Nazwa przednich drzwi, do których należy ta reguła routingu.</span><span class="sxs-lookup"><span data-stu-id="eac7a-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="eac7a-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="eac7a-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="eac7a-118">Nazwa ustawień badania kondycji dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="eac7a-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="eac7a-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="eac7a-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="eac7a-120">Nazwa ustawień równoważenia obciążenia dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="eac7a-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="eac7a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eac7a-121">-Name</span></span>
<span data-ttu-id="eac7a-122">Nazwa BackendPool.</span><span class="sxs-lookup"><span data-stu-id="eac7a-122">BackendPool name.</span></span>

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

### <span data-ttu-id="eac7a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac7a-123">-ResourceGroupName</span></span>
<span data-ttu-id="eac7a-124">Nazwa grupy zasobów, w której zostanie utworzony RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="eac7a-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="eac7a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac7a-125">CommonParameters</span></span>
<span data-ttu-id="eac7a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac7a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac7a-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eac7a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac7a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eac7a-128">INPUTS</span></span>

### <span data-ttu-id="eac7a-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eac7a-129">None</span></span>

## <span data-ttu-id="eac7a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eac7a-130">OUTPUTS</span></span>

### <span data-ttu-id="eac7a-131">Microsoft. Azure. Commands. FrontDoor. models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="eac7a-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="eac7a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eac7a-132">NOTES</span></span>

## <span data-ttu-id="eac7a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eac7a-133">RELATED LINKS</span></span>

<span data-ttu-id="eac7a-134">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Nowe — AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="eac7a-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
