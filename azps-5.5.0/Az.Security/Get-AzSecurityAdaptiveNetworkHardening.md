---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242411"
---
# <span data-ttu-id="97de0-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="97de0-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="97de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97de0-102">SYNOPSIS</span></span>
<span data-ttu-id="97de0-103">Pobiera listę zasobów adaptacyjnego zdyseksowania sieci w zakresie rozszerzonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="97de0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97de0-104">SYNTAX</span></span>

### <span data-ttu-id="97de0-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="97de0-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="97de0-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="97de0-106">DESCRIPTION</span></span>
<span data-ttu-id="97de0-107">Adaptacyjne połączenia sieciowe są automatycznie obliczane przez Azure Security Center. To polecenie cmdlet pozwala uzyskać listę zasobów adaptacyjnego synchronizowania sieci w zakresie rozszerzonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="97de0-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97de0-108">EXAMPLES</span></span>

### <span data-ttu-id="97de0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97de0-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="97de0-110">Pobiera listę zasobów Adaptacyjne nasycanie sieci w zakresie rozszerzonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="97de0-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97de0-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="97de0-112">Uzyskaj jeden zasób Adaptive Network Nasadki</span><span class="sxs-lookup"><span data-stu-id="97de0-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="97de0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97de0-113">PARAMETERS</span></span>

### <span data-ttu-id="97de0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97de0-114">-DefaultProfile</span></span>
<span data-ttu-id="97de0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97de0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97de0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97de0-116">-ResourceGroupName</span></span>
<span data-ttu-id="97de0-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97de0-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de0-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="97de0-118">-ResourceName</span></span>
<span data-ttu-id="97de0-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de0-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="97de0-120">-ResourceNamespace</span></span>
<span data-ttu-id="97de0-121">Przestrzeń nazw zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de0-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="97de0-122">-ResourceType</span></span>
<span data-ttu-id="97de0-123">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="97de0-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de0-124">-AdaptiveNetworkSourceEningResourceName</span><span class="sxs-lookup"><span data-stu-id="97de0-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="97de0-125">Nazwa zasobu Adaptacyjne nasyłanie sieci.</span><span class="sxs-lookup"><span data-stu-id="97de0-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de0-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97de0-126">-SubscriptionId</span></span>
<span data-ttu-id="97de0-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="97de0-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="97de0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97de0-128">CommonParameters</span></span>
<span data-ttu-id="97de0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97de0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97de0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97de0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97de0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97de0-131">INPUTS</span></span>

### <span data-ttu-id="97de0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="97de0-132">System.String</span></span>

## <span data-ttu-id="97de0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97de0-133">OUTPUTS</span></span>

### <span data-ttu-id="97de0-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkInienings.PSSecurityAdaptiveNetworkDenings</span><span class="sxs-lookup"><span data-stu-id="97de0-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="97de0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97de0-135">NOTES</span></span>

## <span data-ttu-id="97de0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97de0-136">RELATED LINKS</span></span>