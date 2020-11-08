---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234408"
---
# <span data-ttu-id="23cd4-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="23cd4-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="23cd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="23cd4-103">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="23cd4-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="23cd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cd4-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cd4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="23cd4-106">Usuń wszystkie węzły z określonego typu węzła i typu węzła z klastra za pomocą narzędzia **Remove-AzServiceFabricNodeType** .</span><span class="sxs-lookup"><span data-stu-id="23cd4-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="23cd4-107">Tego polecenia nie można użyć w celu usunięcia podstawowego typu węzła.</span><span class="sxs-lookup"><span data-stu-id="23cd4-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="23cd4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cd4-108">EXAMPLES</span></span>

### <span data-ttu-id="23cd4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cd4-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="23cd4-110">To polecenie usunie NodeType "NT1" z klastra.</span><span class="sxs-lookup"><span data-stu-id="23cd4-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="23cd4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cd4-111">PARAMETERS</span></span>

### <span data-ttu-id="23cd4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cd4-112">-DefaultProfile</span></span>
<span data-ttu-id="23cd4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cd4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cd4-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23cd4-114">-Name</span></span>
<span data-ttu-id="23cd4-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="23cd4-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="23cd4-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="23cd4-116">-NodeType</span></span>
<span data-ttu-id="23cd4-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="23cd4-117">The node type name</span></span>

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

### <span data-ttu-id="23cd4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cd4-118">-ResourceGroupName</span></span>
<span data-ttu-id="23cd4-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23cd4-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="23cd4-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23cd4-120">-Confirm</span></span>
<span data-ttu-id="23cd4-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cd4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cd4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cd4-122">-WhatIf</span></span>
<span data-ttu-id="23cd4-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cd4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cd4-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23cd4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cd4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cd4-125">CommonParameters</span></span>
<span data-ttu-id="23cd4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cd4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cd4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23cd4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cd4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cd4-128">INPUTS</span></span>

### <span data-ttu-id="23cd4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="23cd4-129">System.String</span></span>

## <span data-ttu-id="23cd4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cd4-130">OUTPUTS</span></span>

### <span data-ttu-id="23cd4-131">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="23cd4-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="23cd4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cd4-132">NOTES</span></span>

## <span data-ttu-id="23cd4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cd4-133">RELATED LINKS</span></span>
