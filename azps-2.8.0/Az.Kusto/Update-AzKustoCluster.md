---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705062"
---
# <span data-ttu-id="b02ea-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b02ea-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="b02ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b02ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b02ea-103">Zaktualizuj istniejący klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b02ea-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="b02ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b02ea-104">SYNTAX</span></span>

### <span data-ttu-id="b02ea-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b02ea-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b02ea-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02ea-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b02ea-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b02ea-108">DESCRIPTION</span></span>
<span data-ttu-id="b02ea-109">Zaktualizuj istniejący klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b02ea-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="b02ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b02ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b02ea-111">Przykład 1 — Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="b02ea-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="b02ea-112">Powyższe polecenie aktualizuje warstwę klastra Kusto "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="b02ea-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="b02ea-113">Przykład 2 — Aktualizowanie istniejącego klastra za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="b02ea-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="b02ea-114">Powyższe polecenie pobiera klaster Kusto "mykustocluster" znajdujący się w grupie zasobów "testrg" przy użyciu `Get-AzKustoCluster` polecenia cmdlet, a następnie powoduje przełączenie wyniku w celu `Update-AzKustoCluster` zaktualizowania warstwy klastra na wartość "standard".</span><span class="sxs-lookup"><span data-stu-id="b02ea-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="b02ea-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b02ea-115">PARAMETERS</span></span>

### <span data-ttu-id="b02ea-116">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="b02ea-116">-Capacity</span></span>
<span data-ttu-id="b02ea-117">Numer wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b02ea-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02ea-118">-DefaultProfile</span></span>
<span data-ttu-id="b02ea-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b02ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b02ea-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b02ea-120">-InputObject</span></span>
<span data-ttu-id="b02ea-121">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="b02ea-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b02ea-122">-Name</span></span>
<span data-ttu-id="b02ea-123">Nazwa klastra do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b02ea-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="b02ea-125">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="b02ea-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b02ea-126">-ResourceId</span></span>
<span data-ttu-id="b02ea-127">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="b02ea-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b02ea-128">-SkuName</span></span>
<span data-ttu-id="b02ea-129">Nazwa jednostki SKU użytej do utworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="b02ea-129">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-130">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="b02ea-130">-Tier</span></span>
<span data-ttu-id="b02ea-131">Nazwa warstwy użytej do utworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="b02ea-131">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b02ea-132">-Confirm</span></span>
<span data-ttu-id="b02ea-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02ea-134">-WhatIf</span></span>
<span data-ttu-id="b02ea-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02ea-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b02ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02ea-137">CommonParameters</span></span>
<span data-ttu-id="b02ea-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02ea-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02ea-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02ea-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02ea-140">INPUTS</span></span>

### <span data-ttu-id="b02ea-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b02ea-141">System.String</span></span>

### <span data-ttu-id="b02ea-142">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b02ea-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b02ea-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b02ea-143">OUTPUTS</span></span>

### <span data-ttu-id="b02ea-144">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b02ea-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b02ea-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b02ea-145">NOTES</span></span>

## <span data-ttu-id="b02ea-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b02ea-146">RELATED LINKS</span></span>
