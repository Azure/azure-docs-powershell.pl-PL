---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504448"
---
# <span data-ttu-id="84770-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84770-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="84770-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84770-102">SYNOPSIS</span></span>
<span data-ttu-id="84770-103">Usuń zasób tabeli tras centrum skojarzony z VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="84770-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="84770-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84770-104">SYNTAX</span></span>

### <span data-ttu-id="84770-105">ByVHubRouteTableName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84770-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84770-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="84770-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84770-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="84770-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84770-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="84770-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84770-109">Opis</span><span class="sxs-lookup"><span data-stu-id="84770-109">DESCRIPTION</span></span>
<span data-ttu-id="84770-110">Usuwa określoną tabelę tras centrum, która jest skojarzona z określonym koncentratorem wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="84770-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="84770-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84770-111">EXAMPLES</span></span>

### <span data-ttu-id="84770-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84770-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="84770-113">To polecenie powoduje usunięcie tabeli routingu centrum wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="84770-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="84770-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84770-114">PARAMETERS</span></span>

### <span data-ttu-id="84770-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84770-115">-AsJob</span></span>
<span data-ttu-id="84770-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="84770-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84770-117">-DefaultProfile</span></span>
<span data-ttu-id="84770-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84770-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84770-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84770-119">-Force</span></span>
<span data-ttu-id="84770-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="84770-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="84770-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84770-121">-InputObject</span></span>
<span data-ttu-id="84770-122">Zasób vhubroutetable do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="84770-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="84770-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84770-123">-Name</span></span>
<span data-ttu-id="84770-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="84770-124">The resource name.</span></span>

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

### <span data-ttu-id="84770-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="84770-125">-ParentObject</span></span>
<span data-ttu-id="84770-126">Nadrzędny wirtualny obiekt piasta tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="84770-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="84770-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="84770-127">-ParentResourceName</span></span>
<span data-ttu-id="84770-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="84770-128">The parent resource name.</span></span>

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

### <span data-ttu-id="84770-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84770-129">-PassThru</span></span>
<span data-ttu-id="84770-130">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="84770-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="84770-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84770-131">-ResourceGroupName</span></span>
<span data-ttu-id="84770-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84770-132">The resource group name.</span></span>

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

### <span data-ttu-id="84770-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84770-133">-ResourceId</span></span>
<span data-ttu-id="84770-134">Identyfikator zasobu vhubroutetable, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="84770-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="84770-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84770-135">-Confirm</span></span>
<span data-ttu-id="84770-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84770-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84770-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84770-137">-WhatIf</span></span>
<span data-ttu-id="84770-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84770-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84770-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84770-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84770-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84770-140">CommonParameters</span></span>
<span data-ttu-id="84770-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84770-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84770-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84770-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84770-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84770-143">INPUTS</span></span>

### <span data-ttu-id="84770-144">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="84770-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="84770-145">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84770-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="84770-146">System. String</span><span class="sxs-lookup"><span data-stu-id="84770-146">System.String</span></span>

## <span data-ttu-id="84770-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84770-147">OUTPUTS</span></span>

### <span data-ttu-id="84770-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84770-148">System.Boolean</span></span>

## <span data-ttu-id="84770-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84770-149">NOTES</span></span>

## <span data-ttu-id="84770-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84770-150">RELATED LINKS</span></span>

[<span data-ttu-id="84770-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84770-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="84770-152">Nowe — AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="84770-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="84770-153">Nowe — AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84770-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="84770-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84770-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)