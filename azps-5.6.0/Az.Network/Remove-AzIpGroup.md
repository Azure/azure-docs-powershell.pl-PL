---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: f1c8589663008b0ebc640a052199a11c82d3b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996304"
---
# <span data-ttu-id="66e77-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="66e77-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="66e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e77-102">SYNOPSIS</span></span>
<span data-ttu-id="66e77-103">Usuwa grupę IpGroup platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="66e77-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="66e77-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66e77-104">SYNTAX</span></span>

### <span data-ttu-id="66e77-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e77-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e77-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e77-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e77-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e77-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e77-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="66e77-108">DESCRIPTION</span></span>
<span data-ttu-id="66e77-109">Polecenie **cmdlet Remove-AzIpGroup** usuwa grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="66e77-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="66e77-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66e77-110">EXAMPLES</span></span>

### <span data-ttu-id="66e77-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66e77-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="66e77-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="66e77-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="66e77-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="66e77-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="66e77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66e77-114">PARAMETERS</span></span>

### <span data-ttu-id="66e77-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="66e77-115">-AsJob</span></span>
<span data-ttu-id="66e77-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66e77-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66e77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e77-117">-DefaultProfile</span></span>
<span data-ttu-id="66e77-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66e77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66e77-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="66e77-119">-Force</span></span>
<span data-ttu-id="66e77-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="66e77-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="66e77-121">- IpGroup</span><span class="sxs-lookup"><span data-stu-id="66e77-121">-IpGroup</span></span>
<span data-ttu-id="66e77-122">Obiekt wejściowy ipGroup.</span><span class="sxs-lookup"><span data-stu-id="66e77-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e77-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66e77-123">-Name</span></span>
<span data-ttu-id="66e77-124">Nazwa grupy adresów ip.</span><span class="sxs-lookup"><span data-stu-id="66e77-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e77-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66e77-125">-PassThru</span></span>
<span data-ttu-id="66e77-126">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="66e77-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="66e77-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e77-127">-ResourceGroupName</span></span>
<span data-ttu-id="66e77-128">Nazwa grupy zasobów grupy ipgroup.</span><span class="sxs-lookup"><span data-stu-id="66e77-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e77-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66e77-129">-ResourceId</span></span>
<span data-ttu-id="66e77-130">Identyfikator zasobu ipgroup.</span><span class="sxs-lookup"><span data-stu-id="66e77-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e77-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66e77-131">-Confirm</span></span>
<span data-ttu-id="66e77-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="66e77-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e77-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e77-133">-WhatIf</span></span>
<span data-ttu-id="66e77-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66e77-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e77-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="66e77-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e77-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e77-136">CommonParameters</span></span>
<span data-ttu-id="66e77-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e77-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e77-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66e77-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e77-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66e77-139">INPUTS</span></span>

### <span data-ttu-id="66e77-140">System.String</span><span class="sxs-lookup"><span data-stu-id="66e77-140">System.String</span></span>

### <span data-ttu-id="66e77-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="66e77-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="66e77-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66e77-142">OUTPUTS</span></span>

### <span data-ttu-id="66e77-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66e77-143">System.Boolean</span></span>

## <span data-ttu-id="66e77-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66e77-144">NOTES</span></span>

## <span data-ttu-id="66e77-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66e77-145">RELATED LINKS</span></span>
