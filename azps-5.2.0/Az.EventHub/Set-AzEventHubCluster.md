---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329243"
---
# <span data-ttu-id="b4dc2-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b4dc2-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="b4dc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4dc2-103">Umożliwia zaktualizowanie znacznika dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="b4dc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4dc2-104">SYNTAX</span></span>

### <span data-ttu-id="b4dc2-105">ClusterPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4dc2-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dc2-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4dc2-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dc2-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4dc2-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4dc2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b4dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="b4dc2-109">Polecenie cmdlet Set-AzEventHubCluster aktualizuje Tagi określonego klastra</span><span class="sxs-lookup"><span data-stu-id="b4dc2-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="b4dc2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="b4dc2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4dc2-111">Example 1</span></span>
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

<span data-ttu-id="b4dc2-112">Aktualizuje znaczniki określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="b4dc2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4dc2-113">PARAMETERS</span></span>

### <span data-ttu-id="b4dc2-114">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="b4dc2-114">-Capacity</span></span>
<span data-ttu-id="b4dc2-115">Pojemność klastra (CU), curerntrly, dozwolona wartość = 1</span><span class="sxs-lookup"><span data-stu-id="b4dc2-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="b4dc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4dc2-116">-DefaultProfile</span></span>
<span data-ttu-id="b4dc2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4dc2-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4dc2-118">-InputObject</span></span>
<span data-ttu-id="b4dc2-119">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="b4dc2-119">Cluster Name</span></span>

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

### <span data-ttu-id="b4dc2-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4dc2-120">-Location</span></span>
<span data-ttu-id="b4dc2-121">Lokalizacja klastra</span><span class="sxs-lookup"><span data-stu-id="b4dc2-121">Location of Cluster</span></span>

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

### <span data-ttu-id="b4dc2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4dc2-122">-Name</span></span>
<span data-ttu-id="b4dc2-123">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="b4dc2-123">Cluster Name</span></span>

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

### <span data-ttu-id="b4dc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4dc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4dc2-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4dc2-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b4dc2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4dc2-126">-ResourceId</span></span>
<span data-ttu-id="b4dc2-127">Identyfikator zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="b4dc2-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="b4dc2-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4dc2-128">-Tag</span></span>
<span data-ttu-id="b4dc2-129">Tagi skrótów przedstawiające tag zasobu dla klastrów</span><span class="sxs-lookup"><span data-stu-id="b4dc2-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="b4dc2-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4dc2-130">-Confirm</span></span>
<span data-ttu-id="b4dc2-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4dc2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4dc2-132">-WhatIf</span></span>
<span data-ttu-id="b4dc2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4dc2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4dc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4dc2-135">CommonParameters</span></span>
<span data-ttu-id="b4dc2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4dc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4dc2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4dc2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4dc2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4dc2-138">INPUTS</span></span>

### <span data-ttu-id="b4dc2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4dc2-139">System.String</span></span>

### <span data-ttu-id="b4dc2-140">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b4dc2-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b4dc2-141">Microsoft. Azure. Commands. EventHub. modele. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="b4dc2-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="b4dc2-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4dc2-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4dc2-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4dc2-143">OUTPUTS</span></span>

### <span data-ttu-id="b4dc2-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="b4dc2-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="b4dc2-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4dc2-145">NOTES</span></span>

## <span data-ttu-id="b4dc2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4dc2-146">RELATED LINKS</span></span>
