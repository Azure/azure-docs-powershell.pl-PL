---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685028"
---
# <span data-ttu-id="9b45c-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="9b45c-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="9b45c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b45c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b45c-103">Aktualizowanie warstwy niezawodności lub maszyny wirtualnej typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="9b45c-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="9b45c-104">Zaktualizuje także warstwę wytrzymałości w rozszerzeniu maszyny wirtualnej service Fabric na skojarzonym zestawie skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9b45c-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b45c-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b45c-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b45c-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b45c-106">DESCRIPTION</span></span>
<span data-ttu-id="9b45c-107">Użyj **funkcji Update-AzureRmServiceFabricDurability, aby** zaktualizować niezawodność lub sKU klastru.</span><span class="sxs-lookup"><span data-stu-id="9b45c-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="9b45c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b45c-108">EXAMPLES</span></span>

### <span data-ttu-id="9b45c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b45c-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="9b45c-110">To polecenie zmienia warstwę właściwości NodeType 'nt1' na srebrną.</span><span class="sxs-lookup"><span data-stu-id="9b45c-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="9b45c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b45c-111">PARAMETERS</span></span>

### <span data-ttu-id="9b45c-112">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9b45c-112">-DurabilityLevel</span></span>
<span data-ttu-id="9b45c-113">Określ poziom niezawodności.</span><span class="sxs-lookup"><span data-stu-id="9b45c-113">Specify durability level.</span></span>

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

### <span data-ttu-id="9b45c-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b45c-114">-Name</span></span>
<span data-ttu-id="9b45c-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9b45c-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9b45c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="9b45c-116">-NodeType</span></span>
<span data-ttu-id="9b45c-117">Określanie nazwy typu węzła Sieć szkieletowa usługi.</span><span class="sxs-lookup"><span data-stu-id="9b45c-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="9b45c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b45c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9b45c-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b45c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9b45c-120">- SKU</span><span class="sxs-lookup"><span data-stu-id="9b45c-120">-Sku</span></span>
<span data-ttu-id="9b45c-121">Określ sku typu węzła.</span><span class="sxs-lookup"><span data-stu-id="9b45c-121">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="9b45c-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b45c-122">-Confirm</span></span>
<span data-ttu-id="9b45c-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b45c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b45c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b45c-124">-WhatIf</span></span>
<span data-ttu-id="9b45c-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b45c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b45c-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b45c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b45c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b45c-127">-DefaultProfile</span></span>
<span data-ttu-id="9b45c-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b45c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b45c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b45c-129">CommonParameters</span></span>
<span data-ttu-id="9b45c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b45c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b45c-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b45c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b45c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b45c-132">INPUTS</span></span>

### <span data-ttu-id="9b45c-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9b45c-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="9b45c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9b45c-134">System.String</span></span>

## <span data-ttu-id="9b45c-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b45c-135">OUTPUTS</span></span>

### <span data-ttu-id="9b45c-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="9b45c-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="9b45c-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b45c-137">NOTES</span></span>

## <span data-ttu-id="9b45c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b45c-138">RELATED LINKS</span></span>

