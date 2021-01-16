---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352285"
---
# <span data-ttu-id="728fa-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="728fa-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="728fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="728fa-102">SYNOPSIS</span></span>
<span data-ttu-id="728fa-103">Usuwa harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="728fa-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="728fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="728fa-104">SYNTAX</span></span>

### <span data-ttu-id="728fa-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="728fa-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728fa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="728fa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728fa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="728fa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728fa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="728fa-108">DESCRIPTION</span></span>
<span data-ttu-id="728fa-109">Polecenie cmdlet **Remove-AzStackEdgeBandwidthSchedule** usuwa harmonogram przepustowości urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="728fa-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="728fa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="728fa-110">EXAMPLES</span></span>

### <span data-ttu-id="728fa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="728fa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="728fa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="728fa-112">PARAMETERS</span></span>

### <span data-ttu-id="728fa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="728fa-113">-AsJob</span></span>
<span data-ttu-id="728fa-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="728fa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="728fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728fa-115">-DefaultProfile</span></span>
<span data-ttu-id="728fa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="728fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="728fa-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="728fa-117">-DeviceName</span></span>
<span data-ttu-id="728fa-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="728fa-118">Device Name</span></span>

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

### <span data-ttu-id="728fa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="728fa-119">-InputObject</span></span>
<span data-ttu-id="728fa-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="728fa-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="728fa-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="728fa-121">-Name</span></span>
<span data-ttu-id="728fa-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="728fa-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728fa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="728fa-123">-PassThru</span></span>
<span data-ttu-id="728fa-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="728fa-124">returns true if successful</span></span>

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

### <span data-ttu-id="728fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="728fa-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="728fa-126">Resource Group Name</span></span>

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

### <span data-ttu-id="728fa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="728fa-127">-ResourceId</span></span>
<span data-ttu-id="728fa-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="728fa-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="728fa-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="728fa-129">-Confirm</span></span>
<span data-ttu-id="728fa-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728fa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728fa-131">-WhatIf</span></span>
<span data-ttu-id="728fa-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728fa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="728fa-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="728fa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728fa-134">CommonParameters</span></span>
<span data-ttu-id="728fa-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728fa-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="728fa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728fa-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="728fa-137">INPUTS</span></span>

### <span data-ttu-id="728fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="728fa-138">System.String</span></span>

### <span data-ttu-id="728fa-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="728fa-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="728fa-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="728fa-140">OUTPUTS</span></span>

### <span data-ttu-id="728fa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="728fa-141">System.Boolean</span></span>

## <span data-ttu-id="728fa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="728fa-142">NOTES</span></span>

## <span data-ttu-id="728fa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="728fa-143">RELATED LINKS</span></span>
