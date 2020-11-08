---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232009"
---
# <span data-ttu-id="0fef3-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="0fef3-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="0fef3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fef3-102">SYNOPSIS</span></span>
<span data-ttu-id="0fef3-103">Umożliwia wyświetlenie listy zasobów dotyczących zwiększania funkcjonalności sieci adaptacyjnych w zakresie zasobu rozszerzonego.</span><span class="sxs-lookup"><span data-stu-id="0fef3-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="0fef3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fef3-104">SYNTAX</span></span>

### <span data-ttu-id="0fef3-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0fef3-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="0fef3-106">Opis</span><span class="sxs-lookup"><span data-stu-id="0fef3-106">DESCRIPTION</span></span>
<span data-ttu-id="0fef3-107">Dodatkowe ograniczenia w sieci są obliczane automatycznie przez usługę Azure Security Center, użyj tego polecenia cmdlet, aby uzyskać listę zasobów adaptacyjnych dotyczących zwiększania sieci w zakresie zasobu rozszerzonego.</span><span class="sxs-lookup"><span data-stu-id="0fef3-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="0fef3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fef3-108">EXAMPLES</span></span>

### <span data-ttu-id="0fef3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0fef3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="0fef3-110">Umożliwia wyświetlenie listy zasobów dotyczących zwiększania funkcjonalności sieci adaptacyjnych w zakresie zasobu rozszerzonego.</span><span class="sxs-lookup"><span data-stu-id="0fef3-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="0fef3-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0fef3-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="0fef3-112">Uzyskiwanie jednego zasobu adaptacyjnego do zabezpieczania sieci</span><span class="sxs-lookup"><span data-stu-id="0fef3-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="0fef3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fef3-113">PARAMETERS</span></span>

### <span data-ttu-id="0fef3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fef3-114">-DefaultProfile</span></span>
<span data-ttu-id="0fef3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fef3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fef3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fef3-116">-ResourceGroupName</span></span>
<span data-ttu-id="0fef3-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fef3-117">Resource group name.</span></span>

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

### <span data-ttu-id="0fef3-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0fef3-118">-ResourceName</span></span>
<span data-ttu-id="0fef3-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fef3-119">Resource name.</span></span>

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

### <span data-ttu-id="0fef3-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="0fef3-120">-ResourceNamespace</span></span>
<span data-ttu-id="0fef3-121">Obszar nazw zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fef3-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="0fef3-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0fef3-122">-ResourceType</span></span>
<span data-ttu-id="0fef3-123">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fef3-123">The type of the resource.</span></span>

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

### <span data-ttu-id="0fef3-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="0fef3-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="0fef3-125">Nazwa zasobu adaptacyjnego dotyczącego zabezpieczania sieci.</span><span class="sxs-lookup"><span data-stu-id="0fef3-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="0fef3-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0fef3-126">-SubscriptionId</span></span>
<span data-ttu-id="0fef3-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fef3-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="0fef3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fef3-128">CommonParameters</span></span>
<span data-ttu-id="0fef3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fef3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fef3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fef3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fef3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fef3-131">INPUTS</span></span>

### <span data-ttu-id="0fef3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0fef3-132">System.String</span></span>

## <span data-ttu-id="0fef3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fef3-133">OUTPUTS</span></span>

### <span data-ttu-id="0fef3-134">Microsoft. Azure. Commands. Security. models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="0fef3-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="0fef3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fef3-135">NOTES</span></span>

## <span data-ttu-id="0fef3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fef3-136">RELATED LINKS</span></span>