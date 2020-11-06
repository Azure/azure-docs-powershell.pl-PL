---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 6df403d432d212e1d0f8d074b9ac57caad438f83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547944"
---
# <span data-ttu-id="5d073-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5d073-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="5d073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d073-102">SYNOPSIS</span></span>
<span data-ttu-id="5d073-103">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="5d073-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d073-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d073-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d073-105">DESCRIPTION</span></span>
<span data-ttu-id="5d073-106">Za pomocą narzędzia **Remove-AzureRmServiceFabricNode** można usuwać węzły z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="5d073-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="5d073-107">Usuwanie jest kontynuowane tylko wtedy, gdy spełnia on metryki kondycji klastra.</span><span class="sxs-lookup"><span data-stu-id="5d073-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="5d073-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d073-108">EXAMPLES</span></span>

### <span data-ttu-id="5d073-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d073-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="5d073-110">To polecenie usunie 2 węzły z NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="5d073-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="5d073-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d073-111">PARAMETERS</span></span>

### <span data-ttu-id="5d073-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d073-112">-DefaultProfile</span></span>
<span data-ttu-id="5d073-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d073-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d073-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d073-114">-Name</span></span>
<span data-ttu-id="5d073-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="5d073-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5d073-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5d073-116">-NodeType</span></span>
<span data-ttu-id="5d073-117">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="5d073-117">Node type name.</span></span>

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

### <span data-ttu-id="5d073-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="5d073-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="5d073-119">Liczba węzłów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5d073-119">Number of nodes to remove.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d073-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d073-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d073-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d073-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d073-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d073-122">-Confirm</span></span>
<span data-ttu-id="5d073-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d073-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d073-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d073-124">-WhatIf</span></span>
<span data-ttu-id="5d073-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d073-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d073-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d073-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d073-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d073-127">CommonParameters</span></span>
<span data-ttu-id="5d073-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d073-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d073-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d073-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d073-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d073-130">INPUTS</span></span>

### <span data-ttu-id="5d073-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5d073-131">System.Int32</span></span>
<span data-ttu-id="5d073-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5d073-132">System.String</span></span>

## <span data-ttu-id="5d073-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d073-133">OUTPUTS</span></span>

### <span data-ttu-id="5d073-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="5d073-134">System.Object</span></span>

## <span data-ttu-id="5d073-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d073-135">NOTES</span></span>

## <span data-ttu-id="5d073-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d073-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d073-137">Dodaj-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5d073-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
