---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: f76ca0db3f4203bf1906c29c32c1973ea098789c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989626"
---
# <span data-ttu-id="a535d-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="a535d-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="a535d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a535d-102">SYNOPSIS</span></span>
<span data-ttu-id="a535d-103">klaster aktualizacji</span><span class="sxs-lookup"><span data-stu-id="a535d-103">update cluster</span></span>

## <span data-ttu-id="a535d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a535d-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a535d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a535d-105">DESCRIPTION</span></span>
<span data-ttu-id="a535d-106">klaster aktualizacji</span><span class="sxs-lookup"><span data-stu-id="a535d-106">update cluster</span></span>

## <span data-ttu-id="a535d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a535d-107">EXAMPLES</span></span>

### <span data-ttu-id="a535d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a535d-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="a535d-109">Aktualizowanie klastrów za pomocą właściwości magazynu kluczy i wersji SKU</span><span class="sxs-lookup"><span data-stu-id="a535d-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="a535d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a535d-110">PARAMETERS</span></span>

### <span data-ttu-id="a535d-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a535d-111">-AsJob</span></span>
<span data-ttu-id="a535d-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a535d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a535d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a535d-113">-ClusterName</span></span>
<span data-ttu-id="a535d-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="a535d-114">The cluster name.</span></span>

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

### <span data-ttu-id="a535d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a535d-115">-DefaultProfile</span></span>
<span data-ttu-id="a535d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a535d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a535d-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a535d-117">-KeyName</span></span>
<span data-ttu-id="a535d-118">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="a535d-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535d-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a535d-119">-KeyVaultUri</span></span>
<span data-ttu-id="a535d-120">Dla tej funkcji keyvault muszą być włączone usługi Uri magazynu kluczy, "Ochrona przed przeczyszczaniem" i "Niechbędne usunięcie".</span><span class="sxs-lookup"><span data-stu-id="a535d-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535d-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="a535d-121">-KeyVersion</span></span>
<span data-ttu-id="a535d-122">Wersja klucza</span><span class="sxs-lookup"><span data-stu-id="a535d-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a535d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a535d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a535d-124">The resource group name.</span></span>

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

### <span data-ttu-id="a535d-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a535d-125">-SkuCapacity</span></span>
<span data-ttu-id="a535d-126">Pojemność sku</span><span class="sxs-lookup"><span data-stu-id="a535d-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535d-127">-SKUName</span><span class="sxs-lookup"><span data-stu-id="a535d-127">-SkuName</span></span>
<span data-ttu-id="a535d-128">Nazwa SKU, teraz może być tylko nazwą "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="a535d-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="a535d-129">— Tagi</span><span class="sxs-lookup"><span data-stu-id="a535d-129">-Tags</span></span>
<span data-ttu-id="a535d-130">Tagi klastrów</span><span class="sxs-lookup"><span data-stu-id="a535d-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="a535d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a535d-131">-Confirm</span></span>
<span data-ttu-id="a535d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a535d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a535d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a535d-133">-WhatIf</span></span>
<span data-ttu-id="a535d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a535d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a535d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a535d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a535d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a535d-136">CommonParameters</span></span>
<span data-ttu-id="a535d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a535d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a535d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a535d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a535d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a535d-139">INPUTS</span></span>

### <span data-ttu-id="a535d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a535d-140">System.String</span></span>

## <span data-ttu-id="a535d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a535d-141">OUTPUTS</span></span>

### <span data-ttu-id="a535d-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a535d-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="a535d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a535d-143">NOTES</span></span>

## <span data-ttu-id="a535d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a535d-144">RELATED LINKS</span></span>
