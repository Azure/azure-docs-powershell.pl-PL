---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232568"
---
# <span data-ttu-id="f3832-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3832-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="f3832-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3832-102">SYNOPSIS</span></span>
<span data-ttu-id="f3832-103">Usuwanie zasobu tabeli routingu centrum wirtualnego skojarzonego z koncentratorem wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="f3832-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="f3832-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3832-104">SYNTAX</span></span>

### <span data-ttu-id="f3832-105">ByVirtualHubRouteTableName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3832-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3832-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f3832-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3832-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="f3832-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3832-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="f3832-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3832-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f3832-109">DESCRIPTION</span></span>
<span data-ttu-id="f3832-110">Usuwa określoną tabelę tras skojarzoną z określonym koncentratorem wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="f3832-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="f3832-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3832-111">EXAMPLES</span></span>

### <span data-ttu-id="f3832-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3832-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="f3832-113">To polecenie usuwa routeTable1 wirtualnego centrum westushub.</span><span class="sxs-lookup"><span data-stu-id="f3832-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="f3832-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3832-114">PARAMETERS</span></span>

### <span data-ttu-id="f3832-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3832-115">-AsJob</span></span>
<span data-ttu-id="f3832-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f3832-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3832-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3832-117">-DefaultProfile</span></span>
<span data-ttu-id="f3832-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3832-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3832-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f3832-119">-Force</span></span>
<span data-ttu-id="f3832-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f3832-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3832-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="f3832-121">-HubName</span></span>
<span data-ttu-id="f3832-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f3832-122">The parent resource name.</span></span>

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

### <span data-ttu-id="f3832-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3832-123">-InputObject</span></span>
<span data-ttu-id="f3832-124">Zasób virtualhubroutetable do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f3832-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="f3832-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3832-125">-Name</span></span>
<span data-ttu-id="f3832-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3832-126">The resource name.</span></span>

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

### <span data-ttu-id="f3832-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3832-127">-PassThru</span></span>
<span data-ttu-id="f3832-128">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="f3832-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="f3832-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3832-129">-ResourceGroupName</span></span>
<span data-ttu-id="f3832-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3832-130">The resource group name.</span></span>

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

### <span data-ttu-id="f3832-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3832-131">-ResourceId</span></span>
<span data-ttu-id="f3832-132">Identyfikator zasobu virtualhubroutetable, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f3832-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="f3832-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f3832-133">-VirtualHub</span></span>
<span data-ttu-id="f3832-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="f3832-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="f3832-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3832-135">-Confirm</span></span>
<span data-ttu-id="f3832-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3832-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3832-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3832-137">-WhatIf</span></span>
<span data-ttu-id="f3832-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3832-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3832-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3832-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3832-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3832-140">CommonParameters</span></span>
<span data-ttu-id="f3832-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3832-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3832-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3832-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3832-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3832-143">INPUTS</span></span>

### <span data-ttu-id="f3832-144">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f3832-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f3832-145">Microsoft. Azure. Commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3832-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="f3832-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f3832-146">System.String</span></span>

## <span data-ttu-id="f3832-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3832-147">OUTPUTS</span></span>

### <span data-ttu-id="f3832-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3832-148">System.Boolean</span></span>

## <span data-ttu-id="f3832-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3832-149">NOTES</span></span>

## <span data-ttu-id="f3832-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3832-150">RELATED LINKS</span></span>
