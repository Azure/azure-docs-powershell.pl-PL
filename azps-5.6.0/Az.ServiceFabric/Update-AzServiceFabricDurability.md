---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955546"
---
# <span data-ttu-id="4e1f6-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="4e1f6-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="4e1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1f6-103">Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="4e1f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e1f6-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e1f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="4e1f6-106">Użyj **funkcji Update-AzServiceFabricDurability, aby** zaktualizować niezawodność lub sKU klastrów.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="4e1f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e1f6-107">EXAMPLES</span></span>

### <span data-ttu-id="4e1f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e1f6-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="4e1f6-109">To polecenie zmienia warstwę właściwości NodeType 'nt1' na srebrną.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="4e1f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e1f6-110">PARAMETERS</span></span>

### <span data-ttu-id="4e1f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1f6-111">-DefaultProfile</span></span>
<span data-ttu-id="4e1f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e1f6-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4e1f6-113">-DurabilityLevel</span></span>
<span data-ttu-id="4e1f6-114">Określ poziom niezawodności.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-114">Specify durability level.</span></span>

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

### <span data-ttu-id="4e1f6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4e1f6-115">-Name</span></span>
<span data-ttu-id="4e1f6-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4e1f6-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4e1f6-117">-NodeType</span></span>
<span data-ttu-id="4e1f6-118">Określanie nazwy typu węzła Sieć szkieletowa usługi.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="4e1f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e1f6-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4e1f6-121">- SKU</span><span class="sxs-lookup"><span data-stu-id="4e1f6-121">-Sku</span></span>
<span data-ttu-id="4e1f6-122">Określ sku typu węzła.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="4e1f6-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e1f6-123">-Confirm</span></span>
<span data-ttu-id="4e1f6-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e1f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e1f6-125">-WhatIf</span></span>
<span data-ttu-id="4e1f6-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e1f6-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e1f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1f6-128">CommonParameters</span></span>
<span data-ttu-id="4e1f6-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e1f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1f6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e1f6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1f6-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e1f6-131">INPUTS</span></span>

### <span data-ttu-id="4e1f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4e1f6-132">System.String</span></span>

### <span data-ttu-id="4e1f6-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4e1f6-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="4e1f6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e1f6-134">OUTPUTS</span></span>

### <span data-ttu-id="4e1f6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4e1f6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4e1f6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e1f6-136">NOTES</span></span>

## <span data-ttu-id="4e1f6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e1f6-137">RELATED LINKS</span></span>
