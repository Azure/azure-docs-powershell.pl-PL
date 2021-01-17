---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346570"
---
# <span data-ttu-id="d3f0b-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d3f0b-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="d3f0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f0b-103">Usuwa usługę Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="d3f0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3f0b-104">SYNTAX</span></span>

### <span data-ttu-id="d3f0b-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f0b-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f0b-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f0b-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f0b-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f0b-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f0b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d3f0b-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f0b-109">Polecenie cmdlet **Remove-AzIpGroup** usuwa składnik Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="d3f0b-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="d3f0b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f0b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3f0b-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="d3f0b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d3f0b-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="d3f0b-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d3f0b-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="d3f0b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3f0b-114">PARAMETERS</span></span>

### <span data-ttu-id="d3f0b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3f0b-115">-AsJob</span></span>
<span data-ttu-id="d3f0b-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d3f0b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3f0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f0b-117">-DefaultProfile</span></span>
<span data-ttu-id="d3f0b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f0b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f0b-119">-Force</span></span>
<span data-ttu-id="d3f0b-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d3f0b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3f0b-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="d3f0b-121">-IpGroup</span></span>
<span data-ttu-id="d3f0b-122">Obiekt wejściowy ipGroup.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="d3f0b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3f0b-123">-Name</span></span>
<span data-ttu-id="d3f0b-124">Nazwa ipgroup.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="d3f0b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3f0b-125">-PassThru</span></span>
<span data-ttu-id="d3f0b-126">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="d3f0b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f0b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3f0b-128">Nazwa grupy zasobów ipgroup.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="d3f0b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f0b-129">-ResourceId</span></span>
<span data-ttu-id="d3f0b-130">Identyfikator zasobu ipgroup.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="d3f0b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3f0b-131">-Confirm</span></span>
<span data-ttu-id="d3f0b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f0b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f0b-133">-WhatIf</span></span>
<span data-ttu-id="d3f0b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f0b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f0b-136">CommonParameters</span></span>
<span data-ttu-id="d3f0b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f0b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3f0b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f0b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3f0b-139">INPUTS</span></span>

### <span data-ttu-id="d3f0b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f0b-140">System.String</span></span>

### <span data-ttu-id="d3f0b-141">Microsoft. Azure. Commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d3f0b-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d3f0b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3f0b-142">OUTPUTS</span></span>

### <span data-ttu-id="d3f0b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3f0b-143">System.Boolean</span></span>

## <span data-ttu-id="d3f0b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3f0b-144">NOTES</span></span>

## <span data-ttu-id="d3f0b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3f0b-145">RELATED LINKS</span></span>
