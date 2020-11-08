---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224424"
---
# <span data-ttu-id="6f998-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="6f998-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="6f998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f998-102">SYNOPSIS</span></span>
<span data-ttu-id="6f998-103">Usuwa określony dedykowany klaster Eventhub z poziomu zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f998-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="6f998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f998-104">SYNTAX</span></span>

### <span data-ttu-id="6f998-105">ClusterPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f998-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f998-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f998-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f998-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f998-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f998-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6f998-108">DESCRIPTION</span></span>
<span data-ttu-id="6f998-109">Polecenie cmdlet Remove-AzEventHubCluster usuwa określoną nazwę dedykowanego klastra eventhub z danego źródła zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f998-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="6f998-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f998-110">EXAMPLES</span></span>

### <span data-ttu-id="6f998-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f998-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="6f998-112">Usuwa klaster Eventhub-Cluster-5557 z RSG-Cluster27651 zasobów</span><span class="sxs-lookup"><span data-stu-id="6f998-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="6f998-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f998-113">PARAMETERS</span></span>

### <span data-ttu-id="6f998-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f998-114">-AsJob</span></span>
<span data-ttu-id="6f998-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6f998-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f998-116">-DefaultProfile</span></span>
<span data-ttu-id="6f998-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f998-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f998-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6f998-118">-InputObject</span></span>
<span data-ttu-id="6f998-119">Obiekt klastra</span><span class="sxs-lookup"><span data-stu-id="6f998-119">Cluster Object</span></span>

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

### <span data-ttu-id="6f998-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f998-120">-Name</span></span>
<span data-ttu-id="6f998-121">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="6f998-121">Cluster Name</span></span>

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

### <span data-ttu-id="6f998-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f998-122">-PassThru</span></span>
<span data-ttu-id="6f998-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6f998-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6f998-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f998-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f998-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f998-125">Resource Group Name</span></span>

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

### <span data-ttu-id="6f998-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f998-126">-ResourceId</span></span>
<span data-ttu-id="6f998-127">Identyfikator zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="6f998-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="6f998-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f998-128">-Confirm</span></span>
<span data-ttu-id="6f998-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f998-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f998-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f998-130">-WhatIf</span></span>
<span data-ttu-id="6f998-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f998-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f998-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f998-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f998-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f998-133">CommonParameters</span></span>
<span data-ttu-id="6f998-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f998-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f998-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f998-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f998-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f998-136">INPUTS</span></span>

### <span data-ttu-id="6f998-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6f998-137">System.String</span></span>

### <span data-ttu-id="6f998-138">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6f998-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="6f998-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f998-139">OUTPUTS</span></span>

### <span data-ttu-id="6f998-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f998-140">System.Boolean</span></span>

## <span data-ttu-id="6f998-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f998-141">NOTES</span></span>

## <span data-ttu-id="6f998-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f998-142">RELATED LINKS</span></span>
