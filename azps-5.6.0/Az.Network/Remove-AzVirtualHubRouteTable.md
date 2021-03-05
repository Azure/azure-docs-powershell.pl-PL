---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: ecec3482c06c77063ebac71788d5bf2058c9ce64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006090"
---
# <span data-ttu-id="57fb8-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="57fb8-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="57fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="57fb8-103">Usuń zasób tabeli trasy wirtualnego centrum skojarzonego z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="57fb8-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="57fb8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57fb8-104">SYNTAX</span></span>

### <span data-ttu-id="57fb8-105">ByVirtualHubRouteTableName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="57fb8-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57fb8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="57fb8-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57fb8-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="57fb8-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57fb8-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="57fb8-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57fb8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="57fb8-109">DESCRIPTION</span></span>
<span data-ttu-id="57fb8-110">Usuwa określoną tabelę trasy skojarzoną z określonym centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="57fb8-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="57fb8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57fb8-111">EXAMPLES</span></span>

### <span data-ttu-id="57fb8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57fb8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="57fb8-113">To polecenie usuwa tabelę routeTable1 centrum wirtualnego Westushub.</span><span class="sxs-lookup"><span data-stu-id="57fb8-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="57fb8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57fb8-114">PARAMETERS</span></span>

### <span data-ttu-id="57fb8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="57fb8-115">-AsJob</span></span>
<span data-ttu-id="57fb8-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57fb8-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fb8-117">-DefaultProfile</span></span>
<span data-ttu-id="57fb8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57fb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="57fb8-119">-Force</span></span>
<span data-ttu-id="57fb8-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="57fb8-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="57fb8-121">-HubName</span></span>
<span data-ttu-id="57fb8-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="57fb8-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57fb8-123">-InputObject</span></span>
<span data-ttu-id="57fb8-124">Zasób, który można usunąć w wirtualnej usłudze.</span><span class="sxs-lookup"><span data-stu-id="57fb8-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57fb8-125">-Name</span></span>
<span data-ttu-id="57fb8-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="57fb8-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57fb8-127">-PassThru</span></span>
<span data-ttu-id="57fb8-128">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="57fb8-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fb8-129">-ResourceGroupName</span></span>
<span data-ttu-id="57fb8-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57fb8-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57fb8-131">-ResourceId</span></span>
<span data-ttu-id="57fb8-132">Identyfikator zasobu, który można usunąć w wirtualnej aplikacjiHubroutetable.</span><span class="sxs-lookup"><span data-stu-id="57fb8-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-133">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="57fb8-133">-VirtualHub</span></span>
<span data-ttu-id="57fb8-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="57fb8-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fb8-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57fb8-135">-Confirm</span></span>
<span data-ttu-id="57fb8-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="57fb8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57fb8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57fb8-137">-WhatIf</span></span>
<span data-ttu-id="57fb8-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57fb8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57fb8-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="57fb8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57fb8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fb8-140">CommonParameters</span></span>
<span data-ttu-id="57fb8-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fb8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fb8-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57fb8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fb8-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57fb8-143">INPUTS</span></span>

### <span data-ttu-id="57fb8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="57fb8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="57fb8-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="57fb8-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="57fb8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="57fb8-146">System.String</span></span>

## <span data-ttu-id="57fb8-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57fb8-147">OUTPUTS</span></span>

### <span data-ttu-id="57fb8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57fb8-148">System.Boolean</span></span>

## <span data-ttu-id="57fb8-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57fb8-149">NOTES</span></span>

## <span data-ttu-id="57fb8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57fb8-150">RELATED LINKS</span></span>
