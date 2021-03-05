---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: fb7a9933a30760fe3bc33f296b93d6bc739c18eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016193"
---
# <span data-ttu-id="70af8-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="70af8-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="70af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70af8-102">SYNOPSIS</span></span>
<span data-ttu-id="70af8-103">Usuwanie zasobu tabeli trasy centrum skojarzonego z usługą VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="70af8-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="70af8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70af8-104">SYNTAX</span></span>

### <span data-ttu-id="70af8-105">ByVHubRouteTableName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="70af8-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70af8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="70af8-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70af8-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="70af8-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70af8-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="70af8-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70af8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="70af8-109">DESCRIPTION</span></span>
<span data-ttu-id="70af8-110">Usuwa określoną tabelę trasy centrum, która jest skojarzona z określonym centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="70af8-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="70af8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70af8-111">EXAMPLES</span></span>

### <span data-ttu-id="70af8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70af8-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="70af8-113">To polecenie usuwa tabelę trasy centrum w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="70af8-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="70af8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70af8-114">PARAMETERS</span></span>

### <span data-ttu-id="70af8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="70af8-115">-AsJob</span></span>
<span data-ttu-id="70af8-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70af8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70af8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70af8-117">-DefaultProfile</span></span>
<span data-ttu-id="70af8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70af8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70af8-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="70af8-119">-Force</span></span>
<span data-ttu-id="70af8-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="70af8-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="70af8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70af8-121">-InputObject</span></span>
<span data-ttu-id="70af8-122">Zasób, który można usunąć.</span><span class="sxs-lookup"><span data-stu-id="70af8-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="70af8-123">-Name</span></span>
<span data-ttu-id="70af8-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="70af8-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="70af8-125">-ParentObject</span></span>
<span data-ttu-id="70af8-126">Obiekt nadrzędnego centrum wirtualnego tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="70af8-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="70af8-127">-ParentResourceName</span></span>
<span data-ttu-id="70af8-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="70af8-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70af8-129">-PassThru</span></span>
<span data-ttu-id="70af8-130">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="70af8-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="70af8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70af8-131">-ResourceGroupName</span></span>
<span data-ttu-id="70af8-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70af8-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70af8-133">-ResourceId</span></span>
<span data-ttu-id="70af8-134">Identyfikator zasobu, który można usunąć.</span><span class="sxs-lookup"><span data-stu-id="70af8-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70af8-135">-Confirm</span></span>
<span data-ttu-id="70af8-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="70af8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70af8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70af8-137">-WhatIf</span></span>
<span data-ttu-id="70af8-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70af8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70af8-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="70af8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70af8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70af8-140">CommonParameters</span></span>
<span data-ttu-id="70af8-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70af8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70af8-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70af8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70af8-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70af8-143">INPUTS</span></span>

### <span data-ttu-id="70af8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="70af8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="70af8-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="70af8-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="70af8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="70af8-146">System.String</span></span>

## <span data-ttu-id="70af8-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70af8-147">OUTPUTS</span></span>

### <span data-ttu-id="70af8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70af8-148">System.Boolean</span></span>

## <span data-ttu-id="70af8-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70af8-149">NOTES</span></span>

## <span data-ttu-id="70af8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70af8-150">RELATED LINKS</span></span>

[<span data-ttu-id="70af8-151">Get-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="70af8-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="70af8-152">New-AzvHubRoute</span><span class="sxs-lookup"><span data-stu-id="70af8-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="70af8-153">New-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="70af8-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="70af8-154">Update-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="70af8-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)