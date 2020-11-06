---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552055"
---
# <span data-ttu-id="ebe6b-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ebe6b-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="ebe6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebe6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe6b-103">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebe6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebe6b-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebe6b-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe6b-106">Za pomocą narzędzia **Remove-AzureRmServiceFabricNode** można usuwać węzły z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="ebe6b-107">Usuwanie jest kontynuowane tylko wtedy, gdy spełnia on metryki kondycji klastra.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="ebe6b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebe6b-108">EXAMPLES</span></span>

### <span data-ttu-id="ebe6b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ebe6b-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="ebe6b-110">To polecenie usunie 2 węzły z NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="ebe6b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebe6b-111">PARAMETERS</span></span>

### <span data-ttu-id="ebe6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe6b-112">-DefaultProfile</span></span>
<span data-ttu-id="ebe6b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebe6b-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebe6b-114">-Name</span></span>
<span data-ttu-id="ebe6b-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ebe6b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ebe6b-116">-NodeType</span></span>
<span data-ttu-id="ebe6b-117">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-117">Node type name.</span></span>

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

### <span data-ttu-id="ebe6b-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="ebe6b-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="ebe6b-119">Liczba węzłów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-119">Number of nodes to remove.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe6b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe6b-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebe6b-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebe6b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebe6b-122">-Confirm</span></span>
<span data-ttu-id="ebe6b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe6b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe6b-124">-WhatIf</span></span>
<span data-ttu-id="ebe6b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebe6b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe6b-127">CommonParameters</span></span>
<span data-ttu-id="ebe6b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe6b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe6b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe6b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebe6b-130">INPUTS</span></span>

### <span data-ttu-id="ebe6b-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ebe6b-131">System.Int32</span></span>
<span data-ttu-id="ebe6b-132">Parametry: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ebe6b-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="ebe6b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ebe6b-133">System.String</span></span>
<span data-ttu-id="ebe6b-134">Parametry: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ebe6b-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="ebe6b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebe6b-135">OUTPUTS</span></span>

### <span data-ttu-id="ebe6b-136">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ebe6b-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ebe6b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebe6b-137">NOTES</span></span>

## <span data-ttu-id="ebe6b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebe6b-138">RELATED LINKS</span></span>

[<span data-ttu-id="ebe6b-139">Dodaj-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ebe6b-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
