---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 56a6afff6551ae0191ac1f17d3a52c47940e045a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546444"
---
# <span data-ttu-id="14317-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="14317-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="14317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14317-102">SYNOPSIS</span></span>
<span data-ttu-id="14317-103">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="14317-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14317-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14317-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14317-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14317-105">DESCRIPTION</span></span>
<span data-ttu-id="14317-106">Użyj funkcji **Update-AzureRmServiceFabricDurability** , aby zaktualizować trwałość lub jednostkę SKU klastra.</span><span class="sxs-lookup"><span data-stu-id="14317-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="14317-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14317-107">EXAMPLES</span></span>

### <span data-ttu-id="14317-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14317-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="14317-109">To polecenie zmienia poziom trwałości NodeType ' NT1 ' na srebrny.</span><span class="sxs-lookup"><span data-stu-id="14317-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="14317-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14317-110">PARAMETERS</span></span>

### <span data-ttu-id="14317-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14317-111">-DefaultProfile</span></span>
<span data-ttu-id="14317-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14317-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14317-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="14317-113">-DurabilityLevel</span></span>
<span data-ttu-id="14317-114">Określ poziom trwałości.</span><span class="sxs-lookup"><span data-stu-id="14317-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14317-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14317-115">-Name</span></span>
<span data-ttu-id="14317-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="14317-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14317-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="14317-117">-NodeType</span></span>
<span data-ttu-id="14317-118">Określ nazwę typu węzła sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="14317-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14317-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14317-119">-ResourceGroupName</span></span>
<span data-ttu-id="14317-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14317-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14317-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="14317-121">-Sku</span></span>
<span data-ttu-id="14317-122">Określ jednostkę SKU typu węzła.</span><span class="sxs-lookup"><span data-stu-id="14317-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14317-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14317-123">-Confirm</span></span>
<span data-ttu-id="14317-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14317-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14317-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14317-125">-WhatIf</span></span>
<span data-ttu-id="14317-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14317-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14317-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14317-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14317-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14317-128">CommonParameters</span></span>
<span data-ttu-id="14317-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14317-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14317-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14317-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14317-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14317-131">INPUTS</span></span>

### <span data-ttu-id="14317-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14317-132">System.String</span></span>
<span data-ttu-id="14317-133">Parametry: NodeType (ByValue), SKU (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14317-133">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="14317-134">Microsoft. Azure. Commands. servicefabric. MODELES. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="14317-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="14317-135">Parametry: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14317-135">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="14317-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14317-136">OUTPUTS</span></span>

### <span data-ttu-id="14317-137">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="14317-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="14317-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14317-138">NOTES</span></span>

## <span data-ttu-id="14317-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14317-139">RELATED LINKS</span></span>
