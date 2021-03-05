---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: 7ba6a5f95c1cc37f7cdef7d8ead7a2514927e089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992727"
---
# <span data-ttu-id="160a2-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="160a2-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="160a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="160a2-102">SYNOPSIS</span></span>
<span data-ttu-id="160a2-103">Usuwa określony dedykowany klaster eventhub z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="160a2-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="160a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="160a2-104">SYNTAX</span></span>

### <span data-ttu-id="160a2-105">ClusterPropertiesSet (default)</span><span class="sxs-lookup"><span data-stu-id="160a2-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160a2-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="160a2-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160a2-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="160a2-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160a2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="160a2-108">DESCRIPTION</span></span>
<span data-ttu-id="160a2-109">Polecenie Remove-AzEventHubCluster cmdlet usuwa nazwę dedykowanego klastra w aplikacji Eventhub z danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="160a2-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="160a2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="160a2-110">EXAMPLES</span></span>

### <span data-ttu-id="160a2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="160a2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="160a2-112">Usuwa klaster Eventhub-Cluster-5557 z RSG-Cluster27651 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="160a2-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="160a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="160a2-113">PARAMETERS</span></span>

### <span data-ttu-id="160a2-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="160a2-114">-AsJob</span></span>
<span data-ttu-id="160a2-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="160a2-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="160a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160a2-116">-DefaultProfile</span></span>
<span data-ttu-id="160a2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="160a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="160a2-118">-InputObject</span></span>
<span data-ttu-id="160a2-119">Obiekt klasterowy</span><span class="sxs-lookup"><span data-stu-id="160a2-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="160a2-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="160a2-120">-Name</span></span>
<span data-ttu-id="160a2-121">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="160a2-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160a2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="160a2-122">-PassThru</span></span>
<span data-ttu-id="160a2-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="160a2-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="160a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="160a2-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="160a2-125">Resource Group Name</span></span>

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

### <span data-ttu-id="160a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="160a2-126">-ResourceId</span></span>
<span data-ttu-id="160a2-127">Identyfikator zasobu klastrów</span><span class="sxs-lookup"><span data-stu-id="160a2-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160a2-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="160a2-128">-Confirm</span></span>
<span data-ttu-id="160a2-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="160a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160a2-130">-WhatIf</span></span>
<span data-ttu-id="160a2-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="160a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160a2-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="160a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160a2-133">CommonParameters</span></span>
<span data-ttu-id="160a2-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160a2-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="160a2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160a2-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="160a2-136">INPUTS</span></span>

### <span data-ttu-id="160a2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="160a2-137">System.String</span></span>

### <span data-ttu-id="160a2-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="160a2-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="160a2-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="160a2-139">OUTPUTS</span></span>

### <span data-ttu-id="160a2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="160a2-140">System.Boolean</span></span>

## <span data-ttu-id="160a2-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="160a2-141">NOTES</span></span>

## <span data-ttu-id="160a2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="160a2-142">RELATED LINKS</span></span>
