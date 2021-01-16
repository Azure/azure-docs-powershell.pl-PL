---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364758"
---
# <span data-ttu-id="3afbc-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="3afbc-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="3afbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3afbc-102">SYNOPSIS</span></span>
<span data-ttu-id="3afbc-103">Aktualizuj klaster</span><span class="sxs-lookup"><span data-stu-id="3afbc-103">update cluster</span></span>

## <span data-ttu-id="3afbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3afbc-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3afbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3afbc-105">DESCRIPTION</span></span>
<span data-ttu-id="3afbc-106">Aktualizuj klaster</span><span class="sxs-lookup"><span data-stu-id="3afbc-106">update cluster</span></span>

## <span data-ttu-id="3afbc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3afbc-107">EXAMPLES</span></span>

### <span data-ttu-id="3afbc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3afbc-108">Example 1</span></span>
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

<span data-ttu-id="3afbc-109">Aktualizowanie klastra za pomocą właściwości magazynu kluczy i jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="3afbc-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="3afbc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3afbc-110">PARAMETERS</span></span>

### <span data-ttu-id="3afbc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3afbc-111">-AsJob</span></span>
<span data-ttu-id="3afbc-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3afbc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3afbc-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="3afbc-113">-ClusterName</span></span>
<span data-ttu-id="3afbc-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="3afbc-114">The cluster name.</span></span>

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

### <span data-ttu-id="3afbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afbc-115">-DefaultProfile</span></span>
<span data-ttu-id="3afbc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3afbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3afbc-117">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="3afbc-117">-KeyName</span></span>
<span data-ttu-id="3afbc-118">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="3afbc-118">Key Name</span></span>

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

### <span data-ttu-id="3afbc-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3afbc-119">-KeyVaultUri</span></span>
<span data-ttu-id="3afbc-120">Identyfikator URI magazynu kluczy, "Wyczyść ochronę" i "usuwanie nietrwałe" trzeba włączyć dla tego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="3afbc-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="3afbc-121">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="3afbc-121">-KeyVersion</span></span>
<span data-ttu-id="3afbc-122">Wersja klucza</span><span class="sxs-lookup"><span data-stu-id="3afbc-122">Key Version</span></span>

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

### <span data-ttu-id="3afbc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afbc-123">-ResourceGroupName</span></span>
<span data-ttu-id="3afbc-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3afbc-124">The resource group name.</span></span>

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

### <span data-ttu-id="3afbc-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3afbc-125">-SkuCapacity</span></span>
<span data-ttu-id="3afbc-126">Pojemność SKU</span><span class="sxs-lookup"><span data-stu-id="3afbc-126">Sku Capacity</span></span>

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

### <span data-ttu-id="3afbc-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3afbc-127">-SkuName</span></span>
<span data-ttu-id="3afbc-128">Nazwa SKU, teraz może być tylko "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="3afbc-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="3afbc-129">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3afbc-129">-Tags</span></span>
<span data-ttu-id="3afbc-130">Tagi klastra</span><span class="sxs-lookup"><span data-stu-id="3afbc-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="3afbc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3afbc-131">-Confirm</span></span>
<span data-ttu-id="3afbc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3afbc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3afbc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3afbc-133">-WhatIf</span></span>
<span data-ttu-id="3afbc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3afbc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3afbc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3afbc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3afbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afbc-136">CommonParameters</span></span>
<span data-ttu-id="3afbc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afbc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3afbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afbc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3afbc-139">INPUTS</span></span>

### <span data-ttu-id="3afbc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3afbc-140">System.String</span></span>

## <span data-ttu-id="3afbc-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3afbc-141">OUTPUTS</span></span>

### <span data-ttu-id="3afbc-142">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="3afbc-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="3afbc-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3afbc-143">NOTES</span></span>

## <span data-ttu-id="3afbc-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3afbc-144">RELATED LINKS</span></span>
