---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221204"
---
# <span data-ttu-id="2fcca-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="2fcca-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="2fcca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fcca-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcca-103">Tworzy nowy dedykowany klaster eventhub</span><span class="sxs-lookup"><span data-stu-id="2fcca-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="2fcca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fcca-104">SYNTAX</span></span>

### <span data-ttu-id="2fcca-105">ClusterPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2fcca-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fcca-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fcca-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fcca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fcca-107">DESCRIPTION</span></span>
<span data-ttu-id="2fcca-108">Polecenie cmdlet New-AzEventHubCluster powoduje utworzenie dedykowanego klastra eventhub w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fcca-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="2fcca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fcca-109">EXAMPLES</span></span>

### <span data-ttu-id="2fcca-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fcca-110">Example 1</span></span>
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

<span data-ttu-id="2fcca-111">Umożliwia utworzenie dedykowanego klastra "Eventhub-Cluster-5557" w przystawce Resources "RSG-Cluster27651" z lokalizacją southcentralus i pojemności jako 1</span><span class="sxs-lookup"><span data-stu-id="2fcca-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="2fcca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fcca-112">PARAMETERS</span></span>

### <span data-ttu-id="2fcca-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="2fcca-113">-Capacity</span></span>
<span data-ttu-id="2fcca-114">Pojemność klastra (CU), curerntrly, dozwolona wartość = 1</span><span class="sxs-lookup"><span data-stu-id="2fcca-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="2fcca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcca-115">-DefaultProfile</span></span>
<span data-ttu-id="2fcca-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fcca-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2fcca-117">-Location</span></span>
<span data-ttu-id="2fcca-118">Lokalizacja klastra</span><span class="sxs-lookup"><span data-stu-id="2fcca-118">Location of Cluster</span></span>

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

### <span data-ttu-id="2fcca-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fcca-119">-Name</span></span>
<span data-ttu-id="2fcca-120">Nazwa klastra</span><span class="sxs-lookup"><span data-stu-id="2fcca-120">Cluster Name</span></span>

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

### <span data-ttu-id="2fcca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fcca-121">-ResourceGroupName</span></span>
<span data-ttu-id="2fcca-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2fcca-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2fcca-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fcca-123">-ResourceId</span></span>
<span data-ttu-id="2fcca-124">Identyfikator zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="2fcca-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="2fcca-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fcca-125">-Tag</span></span>
<span data-ttu-id="2fcca-126">Tagi skrótów przedstawiające znaczniki zasobów dla klastrów</span><span class="sxs-lookup"><span data-stu-id="2fcca-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="2fcca-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fcca-127">-Confirm</span></span>
<span data-ttu-id="2fcca-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fcca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fcca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fcca-129">-WhatIf</span></span>
<span data-ttu-id="2fcca-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fcca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fcca-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fcca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fcca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcca-132">CommonParameters</span></span>
<span data-ttu-id="2fcca-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fcca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcca-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fcca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcca-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fcca-135">INPUTS</span></span>

### <span data-ttu-id="2fcca-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2fcca-136">System.String</span></span>

### <span data-ttu-id="2fcca-137">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2fcca-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2fcca-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2fcca-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2fcca-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fcca-139">OUTPUTS</span></span>

### <span data-ttu-id="2fcca-140">Microsoft. Azure. Commands. EventHub. modele. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="2fcca-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="2fcca-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fcca-141">NOTES</span></span>

## <span data-ttu-id="2fcca-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fcca-142">RELATED LINKS</span></span>
