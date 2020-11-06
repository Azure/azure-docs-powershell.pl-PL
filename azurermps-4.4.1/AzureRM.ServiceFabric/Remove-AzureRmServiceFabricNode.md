---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542939"
---
# <span data-ttu-id="4149b-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4149b-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="4149b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4149b-102">SYNOPSIS</span></span>
<span data-ttu-id="4149b-103">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="4149b-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4149b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4149b-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4149b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4149b-105">DESCRIPTION</span></span>
<span data-ttu-id="4149b-106">Za pomocą narzędzia **Remove-AzureRmServiceFabricNode** można usuwać węzły z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="4149b-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="4149b-107">Usuwanie jest kontynuowane tylko wtedy, gdy spełnia on metryki kondycji klastra.</span><span class="sxs-lookup"><span data-stu-id="4149b-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="4149b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4149b-108">EXAMPLES</span></span>

### <span data-ttu-id="4149b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4149b-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="4149b-110">To polecenie usunie 2 węzły z NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="4149b-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="4149b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4149b-111">PARAMETERS</span></span>

### <span data-ttu-id="4149b-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4149b-112">-Name</span></span>
<span data-ttu-id="4149b-113">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="4149b-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4149b-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4149b-114">-NodeType</span></span>
<span data-ttu-id="4149b-115">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="4149b-115">Node type name.</span></span>

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

### <span data-ttu-id="4149b-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="4149b-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="4149b-117">Liczba węzłów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4149b-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="4149b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4149b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4149b-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4149b-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4149b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4149b-120">-Confirm</span></span>
<span data-ttu-id="4149b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4149b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4149b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4149b-122">-WhatIf</span></span>
<span data-ttu-id="4149b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4149b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4149b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4149b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4149b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4149b-125">-DefaultProfile</span></span>
<span data-ttu-id="4149b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4149b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4149b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4149b-127">CommonParameters</span></span>
<span data-ttu-id="4149b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4149b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4149b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4149b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4149b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4149b-130">INPUTS</span></span>

### <span data-ttu-id="4149b-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4149b-131">System.Int32</span></span>
<span data-ttu-id="4149b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4149b-132">System.String</span></span>

## <span data-ttu-id="4149b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4149b-133">OUTPUTS</span></span>

### <span data-ttu-id="4149b-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="4149b-134">System.Object</span></span>

## <span data-ttu-id="4149b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4149b-135">NOTES</span></span>

## <span data-ttu-id="4149b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4149b-136">RELATED LINKS</span></span>

[<span data-ttu-id="4149b-137">Dodaj-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4149b-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
