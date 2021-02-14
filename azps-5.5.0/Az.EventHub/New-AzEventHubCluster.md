---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237889"
---
# <span data-ttu-id="a8d14-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="a8d14-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="a8d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d14-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d14-103">Tworzy nowy dedykowany klaster w usłudze EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d14-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="a8d14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8d14-104">SYNTAX</span></span>

### <span data-ttu-id="a8d14-105">ClusterPropertiesSet (default)</span><span class="sxs-lookup"><span data-stu-id="a8d14-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8d14-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8d14-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8d14-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8d14-107">DESCRIPTION</span></span>
<span data-ttu-id="a8d14-108">Polecenie New-AzEventHubCluster cmdlet tworzy dedykowany klaster w witrynie Eventhub w danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a8d14-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="a8d14-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8d14-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d14-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8d14-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="a8d14-111">Tworzy klaster dedykowany "Eventhub-Cluster-5557" w grupie zasobów "RSG-Cluster27651" z centralą Lokalizacja w południe i wydajnością jako 1.</span><span class="sxs-lookup"><span data-stu-id="a8d14-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="a8d14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8d14-112">PARAMETERS</span></span>

### <span data-ttu-id="a8d14-113">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="a8d14-113">-Capacity</span></span>
<span data-ttu-id="a8d14-114">Wydajność klastrów (CU), curerntrly, dozwolona wartość = 1</span><span class="sxs-lookup"><span data-stu-id="a8d14-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d14-115">-DefaultProfile</span></span>
<span data-ttu-id="a8d14-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d14-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a8d14-117">-Location</span></span>
<span data-ttu-id="a8d14-118">Lokalizacja klastrów</span><span class="sxs-lookup"><span data-stu-id="a8d14-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8d14-119">-Name</span></span>
<span data-ttu-id="a8d14-120">Nazwa klastrów</span><span class="sxs-lookup"><span data-stu-id="a8d14-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d14-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8d14-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a8d14-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8d14-123">-ResourceId</span></span>
<span data-ttu-id="a8d14-124">Identyfikator zasobu klastrów</span><span class="sxs-lookup"><span data-stu-id="a8d14-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="a8d14-125">-Tag</span></span>
<span data-ttu-id="a8d14-126">Skróty reprezentujące tagi zasobów dla klastrów</span><span class="sxs-lookup"><span data-stu-id="a8d14-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d14-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8d14-127">-Confirm</span></span>
<span data-ttu-id="a8d14-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8d14-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d14-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d14-129">-WhatIf</span></span>
<span data-ttu-id="a8d14-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d14-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8d14-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8d14-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d14-132">CommonParameters</span></span>
<span data-ttu-id="a8d14-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d14-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8d14-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d14-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8d14-135">INPUTS</span></span>

### <span data-ttu-id="a8d14-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a8d14-136">System.String</span></span>

### <span data-ttu-id="a8d14-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a8d14-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a8d14-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8d14-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a8d14-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d14-139">OUTPUTS</span></span>

### <span data-ttu-id="a8d14-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="a8d14-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="a8d14-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8d14-141">NOTES</span></span>

## <span data-ttu-id="a8d14-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8d14-142">RELATED LINKS</span></span>
