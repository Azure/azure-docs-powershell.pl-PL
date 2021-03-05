---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1f2c2e2bf02718053d3656b084f845f40215aceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988303"
---
# <span data-ttu-id="e6380-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e6380-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e6380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6380-102">SYNOPSIS</span></span>
<span data-ttu-id="e6380-103">Usuwa urządzenie z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="e6380-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="e6380-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6380-104">SYNTAX</span></span>

### <span data-ttu-id="e6380-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e6380-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6380-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6380-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6380-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6380-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6380-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6380-108">DESCRIPTION</span></span>
<span data-ttu-id="e6380-109">Polecenie **cmdlet Remove-AzDataBoxEdgeDevice** usuwa konfigurację urządzenia z przeglądarką Edge pola danych.</span><span class="sxs-lookup"><span data-stu-id="e6380-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="e6380-110">Pamiętaj, że urządzenie można usunąć dopiero po zmieściu się w zamówieniu i zanim urządzenie będzie przygotowane do wysyłki przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6380-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="e6380-111">Przed użyciem tego [polecenia cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource) zapoznaj się z dokumentacją dotyczącą usuwania zasobu</span><span class="sxs-lookup"><span data-stu-id="e6380-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="e6380-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6380-112">EXAMPLES</span></span>

### <span data-ttu-id="e6380-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6380-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="e6380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6380-114">PARAMETERS</span></span>

### <span data-ttu-id="e6380-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e6380-115">-AsJob</span></span>
<span data-ttu-id="e6380-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e6380-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6380-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6380-117">-DefaultProfile</span></span>
<span data-ttu-id="e6380-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6380-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6380-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6380-119">-InputObject</span></span>
<span data-ttu-id="e6380-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="e6380-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6380-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6380-121">-Name</span></span>
<span data-ttu-id="e6380-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="e6380-122">Resource Name</span></span>

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

### <span data-ttu-id="e6380-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6380-123">-PassThru</span></span>
<span data-ttu-id="e6380-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="e6380-124">returns true if successful</span></span>

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

### <span data-ttu-id="e6380-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6380-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6380-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e6380-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e6380-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6380-127">-ResourceId</span></span>
<span data-ttu-id="e6380-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6380-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e6380-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6380-129">-Confirm</span></span>
<span data-ttu-id="e6380-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6380-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6380-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6380-131">-WhatIf</span></span>
<span data-ttu-id="e6380-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6380-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6380-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6380-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6380-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6380-134">CommonParameters</span></span>
<span data-ttu-id="e6380-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6380-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6380-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6380-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6380-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6380-137">INPUTS</span></span>

### <span data-ttu-id="e6380-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e6380-138">System.String</span></span>

### <span data-ttu-id="e6380-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e6380-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e6380-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6380-140">OUTPUTS</span></span>

### <span data-ttu-id="e6380-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6380-141">System.Boolean</span></span>

## <span data-ttu-id="e6380-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6380-142">NOTES</span></span>

## <span data-ttu-id="e6380-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6380-143">RELATED LINKS</span></span>
