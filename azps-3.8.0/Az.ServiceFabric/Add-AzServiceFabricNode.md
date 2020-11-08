---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 7f19e7e1891eb7dee4edbe382d2fb3936b401549
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053269"
---
# <span data-ttu-id="7ec92-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7ec92-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="7ec92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ec92-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec92-103">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="7ec92-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="7ec92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ec92-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ec92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ec92-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec92-106">Dodaj węzły do określonego typu węzła za pomocą **dodatku Add-AzServiceFabricNode** .</span><span class="sxs-lookup"><span data-stu-id="7ec92-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="7ec92-107">Wystarczy określić liczbę węzłów, które mają zostać dodane do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="7ec92-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="7ec92-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ec92-108">EXAMPLES</span></span>

### <span data-ttu-id="7ec92-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ec92-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="7ec92-110">To polecenie doda 2 węzły do węzła typu "N1".</span><span class="sxs-lookup"><span data-stu-id="7ec92-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="7ec92-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ec92-111">PARAMETERS</span></span>

### <span data-ttu-id="7ec92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec92-112">-DefaultProfile</span></span>
<span data-ttu-id="7ec92-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec92-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ec92-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ec92-114">-Name</span></span>
<span data-ttu-id="7ec92-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="7ec92-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="7ec92-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7ec92-116">-NodeType</span></span>
<span data-ttu-id="7ec92-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="7ec92-117">Node type name</span></span>

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

### <span data-ttu-id="7ec92-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="7ec92-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="7ec92-119">Liczba węzłów do dodania</span><span class="sxs-lookup"><span data-stu-id="7ec92-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="7ec92-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec92-120">-ResourceGroupName</span></span>
<span data-ttu-id="7ec92-121">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec92-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7ec92-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ec92-122">-Confirm</span></span>
<span data-ttu-id="7ec92-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec92-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec92-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec92-124">-WhatIf</span></span>
<span data-ttu-id="7ec92-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec92-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ec92-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ec92-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec92-127">CommonParameters</span></span>
<span data-ttu-id="7ec92-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec92-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec92-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec92-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ec92-130">INPUTS</span></span>

### <span data-ttu-id="7ec92-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ec92-131">System.Int32</span></span>

### <span data-ttu-id="7ec92-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec92-132">System.String</span></span>

## <span data-ttu-id="7ec92-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ec92-133">OUTPUTS</span></span>

### <span data-ttu-id="7ec92-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7ec92-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7ec92-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ec92-135">NOTES</span></span>

## <span data-ttu-id="7ec92-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ec92-136">RELATED LINKS</span></span>

[<span data-ttu-id="7ec92-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7ec92-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
