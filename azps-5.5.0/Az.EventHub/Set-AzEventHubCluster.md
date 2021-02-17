---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180675"
---
# <span data-ttu-id="b35bc-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b35bc-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="b35bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b35bc-103">Aktualizacja tagu dla danego klastra</span><span class="sxs-lookup"><span data-stu-id="b35bc-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="b35bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b35bc-104">SYNTAX</span></span>

### <span data-ttu-id="b35bc-105">ClusterPropertiesSet (default)</span><span class="sxs-lookup"><span data-stu-id="b35bc-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35bc-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35bc-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35bc-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b35bc-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35bc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b35bc-108">DESCRIPTION</span></span>
<span data-ttu-id="b35bc-109">Polecenie Set-AzEventHubCluster aktualizuje tagi danego klastra</span><span class="sxs-lookup"><span data-stu-id="b35bc-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="b35bc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b35bc-110">EXAMPLES</span></span>

### <span data-ttu-id="b35bc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b35bc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="b35bc-112">Aktualizuje tagi danego klastra.</span><span class="sxs-lookup"><span data-stu-id="b35bc-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="b35bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b35bc-113">PARAMETERS</span></span>

### <span data-ttu-id="b35bc-114">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="b35bc-114">-Capacity</span></span>
<span data-ttu-id="b35bc-115">Wydajność klastrów (CU), curerntrly, dozwolona wartość = 1</span><span class="sxs-lookup"><span data-stu-id="b35bc-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="b35bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35bc-116">-DefaultProfile</span></span>
<span data-ttu-id="b35bc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b35bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35bc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b35bc-118">-InputObject</span></span>
<span data-ttu-id="b35bc-119">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="b35bc-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35bc-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b35bc-120">-Location</span></span>
<span data-ttu-id="b35bc-121">Lokalizacja klastrów</span><span class="sxs-lookup"><span data-stu-id="b35bc-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35bc-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b35bc-122">-Name</span></span>
<span data-ttu-id="b35bc-123">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="b35bc-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="b35bc-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b35bc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b35bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b35bc-126">-ResourceId</span></span>
<span data-ttu-id="b35bc-127">Identyfikator zasobu klastrów</span><span class="sxs-lookup"><span data-stu-id="b35bc-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="b35bc-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="b35bc-128">-Tag</span></span>
<span data-ttu-id="b35bc-129">Skróty reprezentujące tag zasobów dla klastrów</span><span class="sxs-lookup"><span data-stu-id="b35bc-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35bc-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b35bc-130">-Confirm</span></span>
<span data-ttu-id="b35bc-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b35bc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35bc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35bc-132">-WhatIf</span></span>
<span data-ttu-id="b35bc-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35bc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b35bc-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b35bc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35bc-135">CommonParameters</span></span>
<span data-ttu-id="b35bc-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35bc-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b35bc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35bc-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35bc-138">INPUTS</span></span>

### <span data-ttu-id="b35bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b35bc-139">System.String</span></span>

### <span data-ttu-id="b35bc-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b35bc-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b35bc-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="b35bc-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="b35bc-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b35bc-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b35bc-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35bc-143">OUTPUTS</span></span>

### <span data-ttu-id="b35bc-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="b35bc-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="b35bc-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b35bc-145">NOTES</span></span>

## <span data-ttu-id="b35bc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b35bc-146">RELATED LINKS</span></span>
