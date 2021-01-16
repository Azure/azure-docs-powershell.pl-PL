---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365491"
---
# <span data-ttu-id="edfbe-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="edfbe-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="edfbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="edfbe-103">Usuwa usługę Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="edfbe-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="edfbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edfbe-104">SYNTAX</span></span>

### <span data-ttu-id="edfbe-105">VirtualRouterNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="edfbe-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edfbe-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edfbe-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edfbe-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edfbe-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfbe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="edfbe-108">DESCRIPTION</span></span>
<span data-ttu-id="edfbe-109">Polecenie cmdlet **Remove-AzVirtualRouter** usuwa składnik Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="edfbe-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="edfbe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edfbe-110">EXAMPLES</span></span>

### <span data-ttu-id="edfbe-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="edfbe-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="edfbe-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="edfbe-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="edfbe-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="edfbe-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="edfbe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edfbe-114">PARAMETERS</span></span>

### <span data-ttu-id="edfbe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edfbe-115">-AsJob</span></span>
<span data-ttu-id="edfbe-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="edfbe-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfbe-117">-DefaultProfile</span></span>
<span data-ttu-id="edfbe-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edfbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfbe-119">-Force</span><span class="sxs-lookup"><span data-stu-id="edfbe-119">-Force</span></span>
<span data-ttu-id="edfbe-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="edfbe-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="edfbe-121">-InputObject</span></span>
<span data-ttu-id="edfbe-122">Obiekt wejściowy wirtualnego routera.</span><span class="sxs-lookup"><span data-stu-id="edfbe-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edfbe-123">-PassThru</span></span>
<span data-ttu-id="edfbe-124">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="edfbe-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edfbe-125">-ResourceGroupName</span></span>
<span data-ttu-id="edfbe-126">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="edfbe-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edfbe-127">-ResourceId</span></span>
<span data-ttu-id="edfbe-128">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="edfbe-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-129">-Routername</span><span class="sxs-lookup"><span data-stu-id="edfbe-129">-RouterName</span></span>
<span data-ttu-id="edfbe-130">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="edfbe-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edfbe-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edfbe-131">-Confirm</span></span>
<span data-ttu-id="edfbe-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edfbe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfbe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfbe-133">-WhatIf</span></span>
<span data-ttu-id="edfbe-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edfbe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edfbe-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edfbe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfbe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfbe-136">CommonParameters</span></span>
<span data-ttu-id="edfbe-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfbe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfbe-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edfbe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfbe-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edfbe-139">INPUTS</span></span>

### <span data-ttu-id="edfbe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="edfbe-140">System.String</span></span>

### <span data-ttu-id="edfbe-141">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="edfbe-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="edfbe-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edfbe-142">OUTPUTS</span></span>

### <span data-ttu-id="edfbe-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edfbe-143">System.Boolean</span></span>

## <span data-ttu-id="edfbe-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edfbe-144">NOTES</span></span>

## <span data-ttu-id="edfbe-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edfbe-145">RELATED LINKS</span></span>
