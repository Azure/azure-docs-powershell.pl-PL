---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356629"
---
# <span data-ttu-id="901c0-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="901c0-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="901c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="901c0-102">SYNOPSIS</span></span>
<span data-ttu-id="901c0-103">Utwórz klaster</span><span class="sxs-lookup"><span data-stu-id="901c0-103">Create cluster</span></span>

## <span data-ttu-id="901c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="901c0-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="901c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="901c0-105">DESCRIPTION</span></span>

<span data-ttu-id="901c0-106">Utwórz klaster</span><span class="sxs-lookup"><span data-stu-id="901c0-106">Create cluster</span></span>

## <span data-ttu-id="901c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="901c0-107">EXAMPLES</span></span>

### <span data-ttu-id="901c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="901c0-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="901c0-109">Utwórz klaster</span><span class="sxs-lookup"><span data-stu-id="901c0-109">Create cluster</span></span>

## <span data-ttu-id="901c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="901c0-110">PARAMETERS</span></span>

### <span data-ttu-id="901c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="901c0-111">-AsJob</span></span>
<span data-ttu-id="901c0-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="901c0-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="901c0-113">-ClusterName</span></span>
<span data-ttu-id="901c0-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="901c0-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901c0-115">-DefaultProfile</span></span>
<span data-ttu-id="901c0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="901c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="901c0-117">-IdentityType</span></span>
<span data-ttu-id="901c0-118">Typ tożsamości, wartość może być wartością "SystemAssigned", "none".</span><span class="sxs-lookup"><span data-stu-id="901c0-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="901c0-119">-Location</span></span>
<span data-ttu-id="901c0-120">Region geograficzny, w którym klaster zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="901c0-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="901c0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="901c0-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="901c0-123">-SkuCapacity</span></span>
<span data-ttu-id="901c0-124">Pojemność SKU, wartość musi być wielokrotnością 100 i zakresem 1000-2000.</span><span class="sxs-lookup"><span data-stu-id="901c0-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="901c0-125">-SkuName</span></span>
<span data-ttu-id="901c0-126">Nazwa SKU, teraz może być tylko "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="901c0-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="901c0-127">-Tags</span></span>
<span data-ttu-id="901c0-128">Tagi klastra</span><span class="sxs-lookup"><span data-stu-id="901c0-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="901c0-129">-Confirm</span></span>
<span data-ttu-id="901c0-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="901c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901c0-131">-WhatIf</span></span>
<span data-ttu-id="901c0-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="901c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="901c0-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="901c0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901c0-134">CommonParameters</span></span>
<span data-ttu-id="901c0-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901c0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="901c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901c0-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="901c0-137">INPUTS</span></span>

### <span data-ttu-id="901c0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="901c0-138">System.String</span></span>

## <span data-ttu-id="901c0-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="901c0-139">OUTPUTS</span></span>

### <span data-ttu-id="901c0-140">Microsoft. Azure. Commands. OperationalInsights. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="901c0-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="901c0-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="901c0-141">NOTES</span></span>

## <span data-ttu-id="901c0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="901c0-142">RELATED LINKS</span></span>
