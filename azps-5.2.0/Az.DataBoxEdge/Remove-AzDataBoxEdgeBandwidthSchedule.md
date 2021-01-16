---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355054"
---
# <span data-ttu-id="8aeeb-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8aeeb-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="8aeeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="8aeeb-103">Usuwa harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="8aeeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aeeb-104">SYNTAX</span></span>

### <span data-ttu-id="8aeeb-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8aeeb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aeeb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aeeb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aeeb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aeeb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aeeb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8aeeb-108">DESCRIPTION</span></span>
<span data-ttu-id="8aeeb-109">Polecenie cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** usuwa harmonogram przepustowości dla urządzenia z polem danych Edge.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="8aeeb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aeeb-110">EXAMPLES</span></span>

### <span data-ttu-id="8aeeb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8aeeb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="8aeeb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aeeb-112">PARAMETERS</span></span>

### <span data-ttu-id="8aeeb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aeeb-113">-AsJob</span></span>
<span data-ttu-id="8aeeb-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8aeeb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8aeeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aeeb-115">-DefaultProfile</span></span>
<span data-ttu-id="8aeeb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aeeb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8aeeb-117">-DeviceName</span></span>
<span data-ttu-id="8aeeb-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="8aeeb-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aeeb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8aeeb-119">-InputObject</span></span>
<span data-ttu-id="8aeeb-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="8aeeb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aeeb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8aeeb-121">-Name</span></span>
<span data-ttu-id="8aeeb-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="8aeeb-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aeeb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8aeeb-123">-PassThru</span></span>
<span data-ttu-id="8aeeb-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="8aeeb-124">returns true if successful</span></span>

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

### <span data-ttu-id="8aeeb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aeeb-125">-ResourceGroupName</span></span>
<span data-ttu-id="8aeeb-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8aeeb-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aeeb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8aeeb-127">-ResourceId</span></span>
<span data-ttu-id="8aeeb-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8aeeb-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8aeeb-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8aeeb-129">-Confirm</span></span>
<span data-ttu-id="8aeeb-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aeeb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aeeb-131">-WhatIf</span></span>
<span data-ttu-id="8aeeb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aeeb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aeeb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aeeb-134">CommonParameters</span></span>
<span data-ttu-id="8aeeb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aeeb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aeeb-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aeeb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aeeb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aeeb-137">INPUTS</span></span>

### <span data-ttu-id="8aeeb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8aeeb-138">System.String</span></span>

### <span data-ttu-id="8aeeb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8aeeb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="8aeeb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aeeb-140">OUTPUTS</span></span>

### <span data-ttu-id="8aeeb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8aeeb-141">System.Boolean</span></span>

## <span data-ttu-id="8aeeb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aeeb-142">NOTES</span></span>

## <span data-ttu-id="8aeeb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aeeb-143">RELATED LINKS</span></span>
