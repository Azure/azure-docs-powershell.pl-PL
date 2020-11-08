---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 871583629936afe763032d1ce3e98ed4464298f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052686"
---
# <span data-ttu-id="84b2f-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="84b2f-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="84b2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="84b2f-103">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="84b2f-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="84b2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84b2f-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="84b2f-106">Użyj funkcji **Update-AzServiceFabricDurability** , aby zaktualizować trwałość lub jednostkę SKU klastra.</span><span class="sxs-lookup"><span data-stu-id="84b2f-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="84b2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="84b2f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84b2f-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="84b2f-109">To polecenie zmienia poziom trwałości NodeType ' NT1 ' na srebrny.</span><span class="sxs-lookup"><span data-stu-id="84b2f-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="84b2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="84b2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b2f-111">-DefaultProfile</span></span>
<span data-ttu-id="84b2f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b2f-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="84b2f-113">-DurabilityLevel</span></span>
<span data-ttu-id="84b2f-114">Określ poziom trwałości.</span><span class="sxs-lookup"><span data-stu-id="84b2f-114">Specify durability level.</span></span>

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

### <span data-ttu-id="84b2f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84b2f-115">-Name</span></span>
<span data-ttu-id="84b2f-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="84b2f-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="84b2f-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="84b2f-117">-NodeType</span></span>
<span data-ttu-id="84b2f-118">Określ nazwę typu węzła sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="84b2f-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="84b2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="84b2f-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84b2f-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="84b2f-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="84b2f-121">-Sku</span></span>
<span data-ttu-id="84b2f-122">Określ jednostkę SKU typu węzła.</span><span class="sxs-lookup"><span data-stu-id="84b2f-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="84b2f-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84b2f-123">-Confirm</span></span>
<span data-ttu-id="84b2f-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b2f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b2f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b2f-125">-WhatIf</span></span>
<span data-ttu-id="84b2f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b2f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84b2f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84b2f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b2f-128">CommonParameters</span></span>
<span data-ttu-id="84b2f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b2f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b2f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b2f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84b2f-131">INPUTS</span></span>

### <span data-ttu-id="84b2f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="84b2f-132">System.String</span></span>

### <span data-ttu-id="84b2f-133">Microsoft. Azure. Commands. servicefabric. MODELES. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="84b2f-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="84b2f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84b2f-134">OUTPUTS</span></span>

### <span data-ttu-id="84b2f-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="84b2f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="84b2f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84b2f-136">NOTES</span></span>

## <span data-ttu-id="84b2f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84b2f-137">RELATED LINKS</span></span>
