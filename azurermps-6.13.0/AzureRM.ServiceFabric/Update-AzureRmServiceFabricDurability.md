---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 7bc55521f04cf4d6e2bff18a01bfbdf4d76410f2
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684995"
---
# <span data-ttu-id="477c1-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="477c1-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="477c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477c1-102">SYNOPSIS</span></span>
<span data-ttu-id="477c1-103">Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="477c1-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="477c1-104">Zaktualizuje także warstwę wytrzymałości w rozszerzeniu maszyny wirtualnej service Fabric na skojarzonym zestawie skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="477c1-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="477c1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="477c1-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="477c1-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="477c1-106">DESCRIPTION</span></span>
<span data-ttu-id="477c1-107">Użyj **funkcji Update-AzureRmServiceFabricDurability, aby** zaktualizować niezawodność lub sKU klastru.</span><span class="sxs-lookup"><span data-stu-id="477c1-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="477c1-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="477c1-108">EXAMPLES</span></span>

### <span data-ttu-id="477c1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="477c1-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="477c1-110">To polecenie zmienia warstwę właściwości NodeType 'nt1' na srebrną.</span><span class="sxs-lookup"><span data-stu-id="477c1-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="477c1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="477c1-111">PARAMETERS</span></span>

### <span data-ttu-id="477c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477c1-112">-DefaultProfile</span></span>
<span data-ttu-id="477c1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="477c1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="477c1-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="477c1-114">-DurabilityLevel</span></span>
<span data-ttu-id="477c1-115">Określ poziom niezawodności.</span><span class="sxs-lookup"><span data-stu-id="477c1-115">Specify durability level.</span></span>

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

### <span data-ttu-id="477c1-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="477c1-116">-Name</span></span>
<span data-ttu-id="477c1-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="477c1-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="477c1-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="477c1-118">-NodeType</span></span>
<span data-ttu-id="477c1-119">Określanie nazwy typu węzła Sieć szkieletowa usługi.</span><span class="sxs-lookup"><span data-stu-id="477c1-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="477c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="477c1-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="477c1-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="477c1-122">- SKU</span><span class="sxs-lookup"><span data-stu-id="477c1-122">-Sku</span></span>
<span data-ttu-id="477c1-123">Określ sku typu węzła.</span><span class="sxs-lookup"><span data-stu-id="477c1-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="477c1-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="477c1-124">-Confirm</span></span>
<span data-ttu-id="477c1-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="477c1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="477c1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477c1-126">-WhatIf</span></span>
<span data-ttu-id="477c1-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="477c1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="477c1-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="477c1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="477c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c1-129">CommonParameters</span></span>
<span data-ttu-id="477c1-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c1-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477c1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c1-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="477c1-132">INPUTS</span></span>

### <span data-ttu-id="477c1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="477c1-133">System.String</span></span>
<span data-ttu-id="477c1-134">Parametry: NodeType (ByValue), SKU (ByValue)</span><span class="sxs-lookup"><span data-stu-id="477c1-134">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="477c1-135">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="477c1-135">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="477c1-136">Parametry: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="477c1-136">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="477c1-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="477c1-137">OUTPUTS</span></span>

### <span data-ttu-id="477c1-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="477c1-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="477c1-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="477c1-139">NOTES</span></span>

## <span data-ttu-id="477c1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="477c1-140">RELATED LINKS</span></span>
