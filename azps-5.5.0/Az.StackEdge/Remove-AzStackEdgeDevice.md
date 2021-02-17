---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243186"
---
# <span data-ttu-id="60172-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="60172-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="60172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60172-102">SYNOPSIS</span></span>
<span data-ttu-id="60172-103">Usuwa urządzenie Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="60172-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="60172-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60172-104">SYNTAX</span></span>

### <span data-ttu-id="60172-105">DeleteByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="60172-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60172-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60172-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60172-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60172-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60172-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="60172-108">DESCRIPTION</span></span>
<span data-ttu-id="60172-109">Polecenie **cmdlet Remove-AzStackEdgeDevice** usuwa konfigurację urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="60172-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="60172-110">Pamiętaj, że urządzenie można usunąć dopiero po zmieściu się w zamówieniu i zanim urządzenie będzie przygotowane do wysyłki przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60172-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="60172-111">Przed użyciem tego [polecenia cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) zapoznaj się z dokumentacją dotyczącą usuwania zasobu</span><span class="sxs-lookup"><span data-stu-id="60172-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="60172-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60172-112">EXAMPLES</span></span>

### <span data-ttu-id="60172-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60172-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="60172-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60172-114">PARAMETERS</span></span>

### <span data-ttu-id="60172-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="60172-115">-AsJob</span></span>
<span data-ttu-id="60172-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60172-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60172-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60172-117">-DefaultProfile</span></span>
<span data-ttu-id="60172-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60172-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60172-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="60172-119">-DeviceObject</span></span>
<span data-ttu-id="60172-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="60172-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60172-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="60172-121">-Name</span></span>
<span data-ttu-id="60172-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="60172-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60172-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60172-123">-PassThru</span></span>
<span data-ttu-id="60172-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="60172-124">returns true if successful</span></span>

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

### <span data-ttu-id="60172-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60172-125">-ResourceGroupName</span></span>
<span data-ttu-id="60172-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="60172-126">Resource Group Name</span></span>

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

### <span data-ttu-id="60172-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60172-127">-ResourceId</span></span>
<span data-ttu-id="60172-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="60172-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="60172-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60172-129">-Confirm</span></span>
<span data-ttu-id="60172-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60172-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60172-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60172-131">-WhatIf</span></span>
<span data-ttu-id="60172-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60172-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60172-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="60172-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60172-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60172-134">CommonParameters</span></span>
<span data-ttu-id="60172-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60172-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60172-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60172-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60172-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60172-137">INPUTS</span></span>

### <span data-ttu-id="60172-138">System.String</span><span class="sxs-lookup"><span data-stu-id="60172-138">System.String</span></span>

### <span data-ttu-id="60172-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="60172-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="60172-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60172-140">OUTPUTS</span></span>

### <span data-ttu-id="60172-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60172-141">System.Boolean</span></span>

## <span data-ttu-id="60172-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60172-142">NOTES</span></span>

## <span data-ttu-id="60172-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60172-143">RELATED LINKS</span></span>
