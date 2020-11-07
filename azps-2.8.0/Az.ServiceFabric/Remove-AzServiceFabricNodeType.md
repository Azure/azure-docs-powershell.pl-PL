---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: b83e6738ec16b8f2700f71e066430148332ca3ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871507"
---
# <span data-ttu-id="a767f-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a767f-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="a767f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a767f-102">SYNOPSIS</span></span>
<span data-ttu-id="a767f-103">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="a767f-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="a767f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a767f-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a767f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a767f-105">DESCRIPTION</span></span>
<span data-ttu-id="a767f-106">Usuń wszystkie węzły z określonego typu węzła i typu węzła z klastra za pomocą narzędzia **Remove-AzServiceFabricNodeType** .</span><span class="sxs-lookup"><span data-stu-id="a767f-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="a767f-107">Tego polecenia nie można użyć w celu usunięcia podstawowego typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a767f-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="a767f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a767f-108">EXAMPLES</span></span>

### <span data-ttu-id="a767f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a767f-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="a767f-110">To polecenie usunie NodeType "NT1" z klastra.</span><span class="sxs-lookup"><span data-stu-id="a767f-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="a767f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a767f-111">PARAMETERS</span></span>

### <span data-ttu-id="a767f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a767f-112">-DefaultProfile</span></span>
<span data-ttu-id="a767f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a767f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a767f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a767f-114">-Name</span></span>
<span data-ttu-id="a767f-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="a767f-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a767f-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a767f-116">-NodeType</span></span>
<span data-ttu-id="a767f-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="a767f-117">The node type name</span></span>

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

### <span data-ttu-id="a767f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a767f-118">-ResourceGroupName</span></span>
<span data-ttu-id="a767f-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a767f-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a767f-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a767f-120">-Confirm</span></span>
<span data-ttu-id="a767f-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a767f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a767f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a767f-122">-WhatIf</span></span>
<span data-ttu-id="a767f-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a767f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a767f-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a767f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a767f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a767f-125">CommonParameters</span></span>
<span data-ttu-id="a767f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a767f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a767f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a767f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a767f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a767f-128">INPUTS</span></span>

### <span data-ttu-id="a767f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a767f-129">System.String</span></span>

## <span data-ttu-id="a767f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a767f-130">OUTPUTS</span></span>

### <span data-ttu-id="a767f-131">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a767f-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a767f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a767f-132">NOTES</span></span>

## <span data-ttu-id="a767f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a767f-133">RELATED LINKS</span></span>
