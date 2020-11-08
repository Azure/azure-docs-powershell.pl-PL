---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224021"
---
# <span data-ttu-id="d4741-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d4741-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="d4741-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4741-102">SYNOPSIS</span></span>
<span data-ttu-id="d4741-103">Usuwa harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="d4741-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="d4741-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4741-104">SYNTAX</span></span>

### <span data-ttu-id="d4741-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4741-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4741-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4741-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4741-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4741-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4741-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4741-108">DESCRIPTION</span></span>
<span data-ttu-id="d4741-109">Polecenie cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** usuwa harmonogram przepustowości dla urządzenia z polem danych Edge.</span><span class="sxs-lookup"><span data-stu-id="d4741-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="d4741-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4741-110">EXAMPLES</span></span>

### <span data-ttu-id="d4741-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4741-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="d4741-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4741-112">PARAMETERS</span></span>

### <span data-ttu-id="d4741-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4741-113">-AsJob</span></span>
<span data-ttu-id="d4741-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d4741-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4741-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4741-115">-DefaultProfile</span></span>
<span data-ttu-id="d4741-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4741-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4741-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d4741-117">-DeviceName</span></span>
<span data-ttu-id="d4741-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="d4741-118">Device Name</span></span>

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

### <span data-ttu-id="d4741-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4741-119">-InputObject</span></span>
<span data-ttu-id="d4741-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="d4741-120">Input Object</span></span>

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

### <span data-ttu-id="d4741-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4741-121">-Name</span></span>
<span data-ttu-id="d4741-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="d4741-122">Resource Name</span></span>

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

### <span data-ttu-id="d4741-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4741-123">-PassThru</span></span>
<span data-ttu-id="d4741-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="d4741-124">returns true if successful</span></span>

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

### <span data-ttu-id="d4741-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4741-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4741-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d4741-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d4741-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4741-127">-ResourceId</span></span>
<span data-ttu-id="d4741-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d4741-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="d4741-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4741-129">-Confirm</span></span>
<span data-ttu-id="d4741-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4741-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4741-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4741-131">-WhatIf</span></span>
<span data-ttu-id="d4741-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4741-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4741-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4741-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4741-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4741-134">CommonParameters</span></span>
<span data-ttu-id="d4741-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4741-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4741-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4741-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4741-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4741-137">INPUTS</span></span>

### <span data-ttu-id="d4741-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d4741-138">System.String</span></span>

### <span data-ttu-id="d4741-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d4741-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="d4741-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4741-140">OUTPUTS</span></span>

### <span data-ttu-id="d4741-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4741-141">System.Boolean</span></span>

## <span data-ttu-id="d4741-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4741-142">NOTES</span></span>

## <span data-ttu-id="d4741-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4741-143">RELATED LINKS</span></span>
