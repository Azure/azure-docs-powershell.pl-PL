---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: f825d1ba1621a00be6196219d99dc188496ea5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526574"
---
# <span data-ttu-id="a160a-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a160a-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="a160a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a160a-102">SYNOPSIS</span></span>
<span data-ttu-id="a160a-103">Usuwanie kompletnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="a160a-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a160a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a160a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a160a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a160a-105">DESCRIPTION</span></span>
<span data-ttu-id="a160a-106">Usuń wszystkie węzły z określonego typu węzła i typu węzła z klastra za pomocą narzędzia **Remove-AzureRmServiceFabricNodeType** .</span><span class="sxs-lookup"><span data-stu-id="a160a-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="a160a-107">Tego polecenia nie można użyć w celu usunięcia podstawowego typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a160a-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="a160a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a160a-108">EXAMPLES</span></span>

### <span data-ttu-id="a160a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a160a-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="a160a-110">To polecenie usunie NodeType "NT1" z klastra.</span><span class="sxs-lookup"><span data-stu-id="a160a-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="a160a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a160a-111">PARAMETERS</span></span>

### <span data-ttu-id="a160a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a160a-112">-DefaultProfile</span></span>
<span data-ttu-id="a160a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a160a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a160a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a160a-114">-Name</span></span>
<span data-ttu-id="a160a-115">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a160a-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a160a-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a160a-116">-NodeType</span></span>
<span data-ttu-id="a160a-117">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a160a-117">The node type name.</span></span>

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

### <span data-ttu-id="a160a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a160a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a160a-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a160a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a160a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a160a-120">-Confirm</span></span>
<span data-ttu-id="a160a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a160a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a160a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a160a-122">-WhatIf</span></span>
<span data-ttu-id="a160a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a160a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a160a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a160a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a160a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a160a-125">CommonParameters</span></span>
<span data-ttu-id="a160a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a160a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a160a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a160a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a160a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a160a-128">INPUTS</span></span>

### <span data-ttu-id="a160a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a160a-129">System.String</span></span>

## <span data-ttu-id="a160a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a160a-130">OUTPUTS</span></span>

### <span data-ttu-id="a160a-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="a160a-131">System.Object</span></span>

## <span data-ttu-id="a160a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a160a-132">NOTES</span></span>

## <span data-ttu-id="a160a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a160a-133">RELATED LINKS</span></span>

