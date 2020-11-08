---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221317"
---
# <span data-ttu-id="a78c4-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a78c4-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a78c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a78c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a78c4-103">Usuwa kolejność urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a78c4-103">Removes the order for a device.</span></span>

## <span data-ttu-id="a78c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a78c4-104">SYNTAX</span></span>

### <span data-ttu-id="a78c4-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a78c4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a78c4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a78c4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a78c4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a78c4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78c4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a78c4-108">DESCRIPTION</span></span>
<span data-ttu-id="a78c4-109">Polecenie cmdlet **Remove-AzDataBoxEdgeOrder** usuwa istniejące zamówienie na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="a78c4-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="a78c4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a78c4-110">EXAMPLES</span></span>

### <span data-ttu-id="a78c4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a78c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="a78c4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a78c4-112">PARAMETERS</span></span>

### <span data-ttu-id="a78c4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a78c4-113">-AsJob</span></span>
<span data-ttu-id="a78c4-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a78c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a78c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78c4-115">-DefaultProfile</span></span>
<span data-ttu-id="a78c4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a78c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a78c4-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a78c4-117">-DeviceName</span></span>
<span data-ttu-id="a78c4-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a78c4-118">Device Name</span></span>

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

### <span data-ttu-id="a78c4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a78c4-119">-InputObject</span></span>
<span data-ttu-id="a78c4-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="a78c4-120">Input Object</span></span>

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

### <span data-ttu-id="a78c4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a78c4-121">-PassThru</span></span>
<span data-ttu-id="a78c4-122">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="a78c4-122">returns true if successful</span></span>

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

### <span data-ttu-id="a78c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a78c4-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a78c4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a78c4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a78c4-125">-ResourceId</span></span>
<span data-ttu-id="a78c4-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a78c4-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a78c4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a78c4-127">-Confirm</span></span>
<span data-ttu-id="a78c4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78c4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78c4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78c4-129">-WhatIf</span></span>
<span data-ttu-id="a78c4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78c4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a78c4-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a78c4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78c4-132">CommonParameters</span></span>
<span data-ttu-id="a78c4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78c4-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a78c4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78c4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a78c4-135">INPUTS</span></span>

### <span data-ttu-id="a78c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a78c4-136">System.String</span></span>

### <span data-ttu-id="a78c4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a78c4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a78c4-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a78c4-138">OUTPUTS</span></span>

### <span data-ttu-id="a78c4-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a78c4-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a78c4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a78c4-140">NOTES</span></span>

## <span data-ttu-id="a78c4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a78c4-141">RELATED LINKS</span></span>
