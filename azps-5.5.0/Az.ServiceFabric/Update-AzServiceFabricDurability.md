---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189066"
---
# <span data-ttu-id="58966-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="58966-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="58966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58966-102">SYNOPSIS</span></span>
<span data-ttu-id="58966-103">Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="58966-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="58966-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58966-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58966-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="58966-105">DESCRIPTION</span></span>
<span data-ttu-id="58966-106">Użyj **funkcji Update-AzServiceFabricDurability, aby** zaktualizować niezawodność lub sKU klastrów.</span><span class="sxs-lookup"><span data-stu-id="58966-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="58966-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58966-107">EXAMPLES</span></span>

### <span data-ttu-id="58966-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58966-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="58966-109">To polecenie zmienia warstwę właściwości NodeType 'nt1' na srebrną.</span><span class="sxs-lookup"><span data-stu-id="58966-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="58966-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58966-110">PARAMETERS</span></span>

### <span data-ttu-id="58966-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58966-111">-DefaultProfile</span></span>
<span data-ttu-id="58966-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58966-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58966-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="58966-113">-DurabilityLevel</span></span>
<span data-ttu-id="58966-114">Określ poziom niezawodności.</span><span class="sxs-lookup"><span data-stu-id="58966-114">Specify durability level.</span></span>

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

### <span data-ttu-id="58966-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58966-115">-Name</span></span>
<span data-ttu-id="58966-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="58966-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="58966-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="58966-117">-NodeType</span></span>
<span data-ttu-id="58966-118">Określanie nazwy typu węzła Sieć szkieletowa usługi.</span><span class="sxs-lookup"><span data-stu-id="58966-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="58966-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58966-119">-ResourceGroupName</span></span>
<span data-ttu-id="58966-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58966-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="58966-121">- SKU</span><span class="sxs-lookup"><span data-stu-id="58966-121">-Sku</span></span>
<span data-ttu-id="58966-122">Określ sku typu węzła.</span><span class="sxs-lookup"><span data-stu-id="58966-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="58966-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58966-123">-Confirm</span></span>
<span data-ttu-id="58966-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58966-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58966-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58966-125">-WhatIf</span></span>
<span data-ttu-id="58966-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58966-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58966-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58966-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58966-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58966-128">CommonParameters</span></span>
<span data-ttu-id="58966-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58966-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58966-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58966-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58966-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58966-131">INPUTS</span></span>

### <span data-ttu-id="58966-132">System.String</span><span class="sxs-lookup"><span data-stu-id="58966-132">System.String</span></span>

### <span data-ttu-id="58966-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="58966-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="58966-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58966-134">OUTPUTS</span></span>

### <span data-ttu-id="58966-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="58966-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="58966-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58966-136">NOTES</span></span>

## <span data-ttu-id="58966-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58966-137">RELATED LINKS</span></span>
