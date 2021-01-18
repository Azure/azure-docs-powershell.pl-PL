---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503720"
---
# <span data-ttu-id="bd0c2-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bd0c2-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bd0c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0c2-103">Usuwa kolejność urządzenia.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-103">Removes the order for a device.</span></span>

## <span data-ttu-id="bd0c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd0c2-104">SYNTAX</span></span>

### <span data-ttu-id="bd0c2-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd0c2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd0c2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0c2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd0c2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0c2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0c2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bd0c2-108">DESCRIPTION</span></span>
<span data-ttu-id="bd0c2-109">Polecenie cmdlet **Remove-AzDataBoxEdgeOrder** usuwa istniejące zamówienie na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="bd0c2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="bd0c2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd0c2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="bd0c2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd0c2-112">PARAMETERS</span></span>

### <span data-ttu-id="bd0c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd0c2-113">-AsJob</span></span>
<span data-ttu-id="bd0c2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bd0c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd0c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0c2-115">-DefaultProfile</span></span>
<span data-ttu-id="bd0c2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0c2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bd0c2-117">-DeviceName</span></span>
<span data-ttu-id="bd0c2-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="bd0c2-118">Device Name</span></span>

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

### <span data-ttu-id="bd0c2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd0c2-119">-InputObject</span></span>
<span data-ttu-id="bd0c2-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="bd0c2-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd0c2-121">-PassThru</span></span>
<span data-ttu-id="bd0c2-122">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="bd0c2-122">returns true if successful</span></span>

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

### <span data-ttu-id="bd0c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd0c2-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bd0c2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bd0c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd0c2-125">-ResourceId</span></span>
<span data-ttu-id="bd0c2-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bd0c2-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bd0c2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd0c2-127">-Confirm</span></span>
<span data-ttu-id="bd0c2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd0c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0c2-129">-WhatIf</span></span>
<span data-ttu-id="bd0c2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd0c2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd0c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0c2-132">CommonParameters</span></span>
<span data-ttu-id="bd0c2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0c2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd0c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0c2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd0c2-135">INPUTS</span></span>

### <span data-ttu-id="bd0c2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0c2-136">System.String</span></span>

### <span data-ttu-id="bd0c2-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bd0c2-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bd0c2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd0c2-138">OUTPUTS</span></span>

### <span data-ttu-id="bd0c2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bd0c2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bd0c2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd0c2-140">NOTES</span></span>

## <span data-ttu-id="bd0c2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd0c2-141">RELATED LINKS</span></span>
