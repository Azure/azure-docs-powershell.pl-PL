---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222789"
---
# <span data-ttu-id="60dcd-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="60dcd-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="60dcd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="60dcd-103">Usuwa urządzenie stosujące stos.</span><span class="sxs-lookup"><span data-stu-id="60dcd-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="60dcd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60dcd-104">SYNTAX</span></span>

### <span data-ttu-id="60dcd-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60dcd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dcd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dcd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dcd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dcd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60dcd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="60dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="60dcd-109">Polecenie cmdlet **Remove-AzStackEdgeDevice** usuwa konfigurację urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="60dcd-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="60dcd-110">Pamiętaj, że urządzenie można usunąć tylko po złożeniu zamówienia i przed przygotowaniem urządzenia przez firmę Microsoft w celu wysyłki.</span><span class="sxs-lookup"><span data-stu-id="60dcd-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="60dcd-111">Zapoznaj się z dokumentacją dotyczącą usuwania zasobu przed użyciem tego [polecenia cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) .</span><span class="sxs-lookup"><span data-stu-id="60dcd-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="60dcd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60dcd-112">EXAMPLES</span></span>

### <span data-ttu-id="60dcd-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60dcd-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="60dcd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60dcd-114">PARAMETERS</span></span>

### <span data-ttu-id="60dcd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60dcd-115">-AsJob</span></span>
<span data-ttu-id="60dcd-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60dcd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60dcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dcd-117">-DefaultProfile</span></span>
<span data-ttu-id="60dcd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60dcd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60dcd-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="60dcd-119">-DeviceObject</span></span>
<span data-ttu-id="60dcd-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="60dcd-120">Input Object</span></span>

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

### <span data-ttu-id="60dcd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60dcd-121">-Name</span></span>
<span data-ttu-id="60dcd-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="60dcd-122">Resource Name</span></span>

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

### <span data-ttu-id="60dcd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60dcd-123">-PassThru</span></span>
<span data-ttu-id="60dcd-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="60dcd-124">returns true if successful</span></span>

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

### <span data-ttu-id="60dcd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60dcd-125">-ResourceGroupName</span></span>
<span data-ttu-id="60dcd-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="60dcd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="60dcd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60dcd-127">-ResourceId</span></span>
<span data-ttu-id="60dcd-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="60dcd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="60dcd-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60dcd-129">-Confirm</span></span>
<span data-ttu-id="60dcd-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60dcd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60dcd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60dcd-131">-WhatIf</span></span>
<span data-ttu-id="60dcd-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60dcd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60dcd-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60dcd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60dcd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dcd-134">CommonParameters</span></span>
<span data-ttu-id="60dcd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dcd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dcd-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60dcd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dcd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60dcd-137">INPUTS</span></span>

### <span data-ttu-id="60dcd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60dcd-138">System.String</span></span>

### <span data-ttu-id="60dcd-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="60dcd-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="60dcd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60dcd-140">OUTPUTS</span></span>

### <span data-ttu-id="60dcd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60dcd-141">System.Boolean</span></span>

## <span data-ttu-id="60dcd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60dcd-142">NOTES</span></span>

## <span data-ttu-id="60dcd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60dcd-143">RELATED LINKS</span></span>
