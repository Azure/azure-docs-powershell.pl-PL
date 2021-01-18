---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503734"
---
# <span data-ttu-id="2a31a-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2a31a-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="2a31a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a31a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a31a-103">Wywołuje określone akcje w udziale.</span><span class="sxs-lookup"><span data-stu-id="2a31a-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="2a31a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a31a-104">SYNTAX</span></span>

### <span data-ttu-id="2a31a-105">InvokeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a31a-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a31a-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a31a-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a31a-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a31a-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a31a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2a31a-108">DESCRIPTION</span></span>
<span data-ttu-id="2a31a-109">Polecenie cmdlet **Invoke-AzDataBoxEdgeShare** umożliwia wywołanie akcji dotyczącej odświeżania danych w udziale na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="2a31a-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="2a31a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a31a-110">EXAMPLES</span></span>

### <span data-ttu-id="2a31a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a31a-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="2a31a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2a31a-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="2a31a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a31a-113">PARAMETERS</span></span>

### <span data-ttu-id="2a31a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a31a-114">-AsJob</span></span>
<span data-ttu-id="2a31a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2a31a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a31a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a31a-116">-DefaultProfile</span></span>
<span data-ttu-id="2a31a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a31a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a31a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2a31a-118">-DeviceName</span></span>
<span data-ttu-id="2a31a-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="2a31a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a31a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a31a-120">-InputObject</span></span>
<span data-ttu-id="2a31a-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="2a31a-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a31a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a31a-122">-Name</span></span>
<span data-ttu-id="2a31a-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="2a31a-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a31a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a31a-124">-PassThru</span></span>
<span data-ttu-id="2a31a-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="2a31a-125">returns true if successful</span></span>

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

### <span data-ttu-id="2a31a-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="2a31a-126">-RefreshData</span></span>
<span data-ttu-id="2a31a-127">Odświeżanie metadanych udziału przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="2a31a-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="2a31a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a31a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a31a-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2a31a-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a31a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a31a-130">-ResourceId</span></span>
<span data-ttu-id="2a31a-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2a31a-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a31a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a31a-132">-Confirm</span></span>
<span data-ttu-id="2a31a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a31a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a31a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a31a-134">-WhatIf</span></span>
<span data-ttu-id="2a31a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a31a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a31a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a31a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a31a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a31a-137">CommonParameters</span></span>
<span data-ttu-id="2a31a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a31a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a31a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a31a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a31a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a31a-140">INPUTS</span></span>

### <span data-ttu-id="2a31a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2a31a-141">System.String</span></span>

### <span data-ttu-id="2a31a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2a31a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="2a31a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a31a-143">OUTPUTS</span></span>

### <span data-ttu-id="2a31a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a31a-144">System.Boolean</span></span>

## <span data-ttu-id="2a31a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a31a-145">NOTES</span></span>

## <span data-ttu-id="2a31a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a31a-146">RELATED LINKS</span></span>
