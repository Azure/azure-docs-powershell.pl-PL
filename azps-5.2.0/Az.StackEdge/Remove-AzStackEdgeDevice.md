---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352273"
---
# <span data-ttu-id="c4595-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c4595-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c4595-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4595-102">SYNOPSIS</span></span>
<span data-ttu-id="c4595-103">Usuwa urządzenie stosujące stos.</span><span class="sxs-lookup"><span data-stu-id="c4595-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="c4595-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4595-104">SYNTAX</span></span>

### <span data-ttu-id="c4595-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4595-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4595-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4595-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4595-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4595-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4595-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4595-108">DESCRIPTION</span></span>
<span data-ttu-id="c4595-109">Polecenie cmdlet **Remove-AzStackEdgeDevice** usuwa konfigurację urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="c4595-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="c4595-110">Pamiętaj, że urządzenie można usunąć tylko po złożeniu zamówienia i przed przygotowaniem urządzenia przez firmę Microsoft w celu wysyłki.</span><span class="sxs-lookup"><span data-stu-id="c4595-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="c4595-111">Zapoznaj się z dokumentacją dotyczącą usuwania zasobu przed użyciem tego [polecenia cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) .</span><span class="sxs-lookup"><span data-stu-id="c4595-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="c4595-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4595-112">EXAMPLES</span></span>

### <span data-ttu-id="c4595-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4595-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="c4595-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4595-114">PARAMETERS</span></span>

### <span data-ttu-id="c4595-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4595-115">-AsJob</span></span>
<span data-ttu-id="c4595-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c4595-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4595-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4595-117">-DefaultProfile</span></span>
<span data-ttu-id="c4595-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4595-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4595-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c4595-119">-DeviceObject</span></span>
<span data-ttu-id="c4595-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="c4595-120">Input Object</span></span>

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

### <span data-ttu-id="c4595-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4595-121">-Name</span></span>
<span data-ttu-id="c4595-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="c4595-122">Resource Name</span></span>

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

### <span data-ttu-id="c4595-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4595-123">-PassThru</span></span>
<span data-ttu-id="c4595-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="c4595-124">returns true if successful</span></span>

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

### <span data-ttu-id="c4595-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4595-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4595-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c4595-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c4595-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4595-127">-ResourceId</span></span>
<span data-ttu-id="c4595-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c4595-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="c4595-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4595-129">-Confirm</span></span>
<span data-ttu-id="c4595-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4595-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4595-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4595-131">-WhatIf</span></span>
<span data-ttu-id="c4595-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4595-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4595-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4595-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4595-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4595-134">CommonParameters</span></span>
<span data-ttu-id="c4595-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4595-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4595-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4595-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4595-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4595-137">INPUTS</span></span>

### <span data-ttu-id="c4595-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c4595-138">System.String</span></span>

### <span data-ttu-id="c4595-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c4595-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c4595-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4595-140">OUTPUTS</span></span>

### <span data-ttu-id="c4595-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4595-141">System.Boolean</span></span>

## <span data-ttu-id="c4595-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4595-142">NOTES</span></span>

## <span data-ttu-id="c4595-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4595-143">RELATED LINKS</span></span>
