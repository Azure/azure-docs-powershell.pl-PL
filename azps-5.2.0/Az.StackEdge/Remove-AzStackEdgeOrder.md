---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358743"
---
# <span data-ttu-id="cd360-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cd360-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="cd360-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd360-102">SYNOPSIS</span></span>
<span data-ttu-id="cd360-103">Usuwa kolejność urządzenia.</span><span class="sxs-lookup"><span data-stu-id="cd360-103">Removes the order for a device.</span></span>

## <span data-ttu-id="cd360-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd360-104">SYNTAX</span></span>

### <span data-ttu-id="cd360-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd360-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd360-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd360-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd360-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd360-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd360-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd360-108">DESCRIPTION</span></span>
<span data-ttu-id="cd360-109">Polecenie cmdlet **Remove-AzStackEdgeOrder** usuwa istniejące zamówienie na urządzeniu z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="cd360-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="cd360-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd360-110">EXAMPLES</span></span>

### <span data-ttu-id="cd360-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd360-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="cd360-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd360-112">PARAMETERS</span></span>

### <span data-ttu-id="cd360-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd360-113">-AsJob</span></span>
<span data-ttu-id="cd360-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cd360-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd360-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd360-115">-DefaultProfile</span></span>
<span data-ttu-id="cd360-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd360-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd360-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cd360-117">-DeviceName</span></span>
<span data-ttu-id="cd360-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="cd360-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd360-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd360-119">-InputObject</span></span>
<span data-ttu-id="cd360-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="cd360-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd360-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd360-121">-PassThru</span></span>
<span data-ttu-id="cd360-122">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="cd360-122">returns true if successful</span></span>

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

### <span data-ttu-id="cd360-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd360-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd360-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd360-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd360-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd360-125">-ResourceId</span></span>
<span data-ttu-id="cd360-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd360-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd360-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd360-127">-Confirm</span></span>
<span data-ttu-id="cd360-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd360-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd360-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd360-129">-WhatIf</span></span>
<span data-ttu-id="cd360-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd360-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd360-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd360-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd360-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd360-132">CommonParameters</span></span>
<span data-ttu-id="cd360-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd360-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd360-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd360-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd360-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd360-135">INPUTS</span></span>

### <span data-ttu-id="cd360-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cd360-136">System.String</span></span>

### <span data-ttu-id="cd360-137">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cd360-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="cd360-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd360-138">OUTPUTS</span></span>

### <span data-ttu-id="cd360-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cd360-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="cd360-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd360-140">NOTES</span></span>

## <span data-ttu-id="cd360-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd360-141">RELATED LINKS</span></span>
