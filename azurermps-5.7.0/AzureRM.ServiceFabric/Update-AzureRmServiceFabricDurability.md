---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549544"
---
# <span data-ttu-id="bfa66-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="bfa66-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="bfa66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfa66-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa66-103">Aktualizowanie warstwy trwałości lub VmSku typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="bfa66-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfa66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfa66-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfa66-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa66-106">Użyj funkcji **Update-AzureRmServiceFabricDurability** , aby zaktualizować trwałość lub jednostkę SKU klastra.</span><span class="sxs-lookup"><span data-stu-id="bfa66-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="bfa66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfa66-107">EXAMPLES</span></span>

### <span data-ttu-id="bfa66-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bfa66-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="bfa66-109">To polecenie zmienia poziom trwałości NodeType ' NT1 ' na srebrny.</span><span class="sxs-lookup"><span data-stu-id="bfa66-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="bfa66-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfa66-110">PARAMETERS</span></span>

### <span data-ttu-id="bfa66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa66-111">-DefaultProfile</span></span>
<span data-ttu-id="bfa66-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bfa66-113">-DurabilityLevel</span></span>
<span data-ttu-id="bfa66-114">Określ poziom trwałości.</span><span class="sxs-lookup"><span data-stu-id="bfa66-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfa66-115">-Name</span></span>
<span data-ttu-id="bfa66-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="bfa66-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bfa66-117">-NodeType</span></span>
<span data-ttu-id="bfa66-118">Określ nazwę typu węzła sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="bfa66-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa66-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfa66-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfa66-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="bfa66-121">-Sku</span></span>
<span data-ttu-id="bfa66-122">Określ jednostkę SKU typu węzła.</span><span class="sxs-lookup"><span data-stu-id="bfa66-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfa66-123">-Confirm</span></span>
<span data-ttu-id="bfa66-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa66-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa66-125">-WhatIf</span></span>
<span data-ttu-id="bfa66-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa66-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfa66-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfa66-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa66-128">CommonParameters</span></span>
<span data-ttu-id="bfa66-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa66-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa66-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa66-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfa66-131">INPUTS</span></span>

### <span data-ttu-id="bfa66-132">Microsoft. Azure. Commands. servicefabric. MODELES. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bfa66-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="bfa66-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bfa66-133">System.String</span></span>

## <span data-ttu-id="bfa66-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfa66-134">OUTPUTS</span></span>

### <span data-ttu-id="bfa66-135">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="bfa66-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="bfa66-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfa66-136">NOTES</span></span>

## <span data-ttu-id="bfa66-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfa66-137">RELATED LINKS</span></span>

