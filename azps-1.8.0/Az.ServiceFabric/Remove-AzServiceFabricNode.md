---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 22aa963f772a87b97a0a64ccdaef5ad6ef004696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708076"
---
# <span data-ttu-id="79110-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="79110-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="79110-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79110-102">SYNOPSIS</span></span>
<span data-ttu-id="79110-103">Usuwanie węzłów z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="79110-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="79110-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79110-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79110-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79110-105">DESCRIPTION</span></span>
<span data-ttu-id="79110-106">Za pomocą narzędzia **Remove-AzServiceFabricNode** można usuwać węzły z określonego typu węzła z poziomu klastra.</span><span class="sxs-lookup"><span data-stu-id="79110-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="79110-107">Usuwanie jest kontynuowane tylko wtedy, gdy spełnia on metryki kondycji klastra.</span><span class="sxs-lookup"><span data-stu-id="79110-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="79110-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79110-108">EXAMPLES</span></span>

### <span data-ttu-id="79110-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79110-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="79110-110">To polecenie usunie 2 węzły z NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="79110-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="79110-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79110-111">PARAMETERS</span></span>

### <span data-ttu-id="79110-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79110-112">-DefaultProfile</span></span>
<span data-ttu-id="79110-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79110-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79110-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79110-114">-Name</span></span>
<span data-ttu-id="79110-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="79110-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="79110-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="79110-116">-NodeType</span></span>
<span data-ttu-id="79110-117">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="79110-117">Node type name.</span></span>

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

### <span data-ttu-id="79110-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="79110-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="79110-119">Liczba węzłów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="79110-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="79110-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79110-120">-ResourceGroupName</span></span>
<span data-ttu-id="79110-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79110-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="79110-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79110-122">-Confirm</span></span>
<span data-ttu-id="79110-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79110-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79110-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79110-124">-WhatIf</span></span>
<span data-ttu-id="79110-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79110-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79110-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79110-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79110-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79110-127">CommonParameters</span></span>
<span data-ttu-id="79110-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79110-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79110-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79110-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79110-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79110-130">INPUTS</span></span>

### <span data-ttu-id="79110-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="79110-131">System.Int32</span></span>

### <span data-ttu-id="79110-132">System. String</span><span class="sxs-lookup"><span data-stu-id="79110-132">System.String</span></span>

## <span data-ttu-id="79110-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79110-133">OUTPUTS</span></span>

### <span data-ttu-id="79110-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="79110-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="79110-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79110-135">NOTES</span></span>

## <span data-ttu-id="79110-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79110-136">RELATED LINKS</span></span>

[<span data-ttu-id="79110-137">Dodaj-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="79110-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md) 