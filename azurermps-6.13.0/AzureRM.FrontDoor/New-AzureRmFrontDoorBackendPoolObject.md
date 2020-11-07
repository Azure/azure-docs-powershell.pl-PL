---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717402"
---
# <span data-ttu-id="09f80-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="09f80-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="09f80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09f80-102">SYNOPSIS</span></span>
<span data-ttu-id="09f80-103">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="09f80-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09f80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09f80-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09f80-105">DESCRIPTION</span></span>
<span data-ttu-id="09f80-106">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="09f80-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="09f80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09f80-107">EXAMPLES</span></span>

### <span data-ttu-id="09f80-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09f80-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="09f80-109">Tworzenie obiektu PSBackendPool na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="09f80-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="09f80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09f80-110">PARAMETERS</span></span>

### <span data-ttu-id="09f80-111">-Wewnętrzna baza danych</span><span class="sxs-lookup"><span data-stu-id="09f80-111">-Backend</span></span>
<span data-ttu-id="09f80-112">Zestaw zakończonych końcem tej puli.</span><span class="sxs-lookup"><span data-stu-id="09f80-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="09f80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f80-113">-DefaultProfile</span></span>
<span data-ttu-id="09f80-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09f80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f80-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="09f80-115">-FrontDoorName</span></span>
<span data-ttu-id="09f80-116">Nazwa przednich drzwi, do których należy ta reguła routingu.</span><span class="sxs-lookup"><span data-stu-id="09f80-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="09f80-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="09f80-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="09f80-118">Nazwa ustawień badania kondycji dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="09f80-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="09f80-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="09f80-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="09f80-120">Nazwa ustawień równoważenia obciążenia dla tej puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="09f80-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="09f80-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09f80-121">-Name</span></span>
<span data-ttu-id="09f80-122">Nazwa BackendPool.</span><span class="sxs-lookup"><span data-stu-id="09f80-122">BackendPool name.</span></span>

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

### <span data-ttu-id="09f80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f80-123">-ResourceGroupName</span></span>
<span data-ttu-id="09f80-124">Nazwa grupy zasobów, w której zostanie utworzony RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="09f80-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="09f80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f80-125">CommonParameters</span></span>
<span data-ttu-id="09f80-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f80-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f80-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f80-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f80-128">INPUTS</span></span>

### <span data-ttu-id="09f80-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="09f80-129">None</span></span>

## <span data-ttu-id="09f80-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09f80-130">OUTPUTS</span></span>

### <span data-ttu-id="09f80-131">Microsoft. Azure. Commands. FrontDoor. models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="09f80-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="09f80-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09f80-132">NOTES</span></span>

## <span data-ttu-id="09f80-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09f80-133">RELATED LINKS</span></span>

<span data-ttu-id="09f80-134">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Nowe — AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="09f80-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
