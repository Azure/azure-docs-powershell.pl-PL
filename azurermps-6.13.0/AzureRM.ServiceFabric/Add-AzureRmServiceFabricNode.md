---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716914"
---
# <span data-ttu-id="969c2-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="969c2-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="969c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="969c2-102">SYNOPSIS</span></span>
<span data-ttu-id="969c2-103">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="969c2-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="969c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="969c2-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="969c2-105">DESCRIPTION</span></span>
<span data-ttu-id="969c2-106">Dodaj węzły do określonego typu węzła za pomocą **dodatku Add-AzureRmServiceFabricNode** .</span><span class="sxs-lookup"><span data-stu-id="969c2-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="969c2-107">Wystarczy określić liczbę węzłów, które mają zostać dodane do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="969c2-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="969c2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="969c2-108">EXAMPLES</span></span>

### <span data-ttu-id="969c2-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="969c2-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="969c2-110">To polecenie doda 2 węzły do węzła typu "N1".</span><span class="sxs-lookup"><span data-stu-id="969c2-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="969c2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="969c2-111">PARAMETERS</span></span>

### <span data-ttu-id="969c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969c2-112">-DefaultProfile</span></span>
<span data-ttu-id="969c2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="969c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="969c2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="969c2-114">-Name</span></span>
<span data-ttu-id="969c2-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="969c2-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="969c2-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="969c2-116">-NodeType</span></span>
<span data-ttu-id="969c2-117">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="969c2-117">Node type name.</span></span>

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

### <span data-ttu-id="969c2-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="969c2-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="969c2-119">Numer wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="969c2-119">VM instance number.</span></span>

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

### <span data-ttu-id="969c2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969c2-120">-ResourceGroupName</span></span>
<span data-ttu-id="969c2-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="969c2-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="969c2-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="969c2-122">-Confirm</span></span>
<span data-ttu-id="969c2-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969c2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969c2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969c2-124">-WhatIf</span></span>
<span data-ttu-id="969c2-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969c2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="969c2-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="969c2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969c2-127">CommonParameters</span></span>
<span data-ttu-id="969c2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969c2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969c2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="969c2-130">INPUTS</span></span>

### <span data-ttu-id="969c2-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="969c2-131">System.Int32</span></span>
<span data-ttu-id="969c2-132">Parametry: NumberOfNodesToAdd (ByValue)</span><span class="sxs-lookup"><span data-stu-id="969c2-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="969c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="969c2-133">System.String</span></span>
<span data-ttu-id="969c2-134">Parametry: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="969c2-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="969c2-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="969c2-135">OUTPUTS</span></span>

### <span data-ttu-id="969c2-136">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="969c2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="969c2-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="969c2-137">NOTES</span></span>

## <span data-ttu-id="969c2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="969c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="969c2-139">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="969c2-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
