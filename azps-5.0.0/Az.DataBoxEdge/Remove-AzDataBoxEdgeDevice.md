---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306480"
---
# <span data-ttu-id="cb7ba-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cb7ba-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cb7ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7ba-103">Usuwa urządzenie z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="cb7ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb7ba-104">SYNTAX</span></span>

### <span data-ttu-id="cb7ba-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb7ba-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7ba-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7ba-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7ba-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7ba-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb7ba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cb7ba-108">DESCRIPTION</span></span>
<span data-ttu-id="cb7ba-109">Polecenie cmdlet **Remove-AzDataBoxEdgeDevice** usuwa konfigurację urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="cb7ba-110">Pamiętaj, że urządzenie można usunąć tylko po złożeniu zamówienia i przed przygotowaniem urządzenia przez firmę Microsoft w celu wysyłki.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="cb7ba-111">Zapoznaj się z dokumentacją dotyczącą usuwania zasobu przed użyciem tego [polecenia cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) .</span><span class="sxs-lookup"><span data-stu-id="cb7ba-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="cb7ba-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb7ba-112">EXAMPLES</span></span>

### <span data-ttu-id="cb7ba-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb7ba-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="cb7ba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb7ba-114">PARAMETERS</span></span>

### <span data-ttu-id="cb7ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb7ba-115">-AsJob</span></span>
<span data-ttu-id="cb7ba-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cb7ba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb7ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7ba-117">-DefaultProfile</span></span>
<span data-ttu-id="cb7ba-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb7ba-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cb7ba-119">-InputObject</span></span>
<span data-ttu-id="cb7ba-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="cb7ba-120">Input Object</span></span>

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

### <span data-ttu-id="cb7ba-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb7ba-121">-Name</span></span>
<span data-ttu-id="cb7ba-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="cb7ba-122">Resource Name</span></span>

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

### <span data-ttu-id="cb7ba-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb7ba-123">-PassThru</span></span>
<span data-ttu-id="cb7ba-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="cb7ba-124">returns true if successful</span></span>

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

### <span data-ttu-id="cb7ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb7ba-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cb7ba-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cb7ba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb7ba-127">-ResourceId</span></span>
<span data-ttu-id="cb7ba-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cb7ba-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="cb7ba-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb7ba-129">-Confirm</span></span>
<span data-ttu-id="cb7ba-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7ba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb7ba-131">-WhatIf</span></span>
<span data-ttu-id="cb7ba-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb7ba-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ba-134">CommonParameters</span></span>
<span data-ttu-id="cb7ba-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ba-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb7ba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ba-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb7ba-137">INPUTS</span></span>

### <span data-ttu-id="cb7ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cb7ba-138">System.String</span></span>

### <span data-ttu-id="cb7ba-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cb7ba-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cb7ba-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb7ba-140">OUTPUTS</span></span>

### <span data-ttu-id="cb7ba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb7ba-141">System.Boolean</span></span>

## <span data-ttu-id="cb7ba-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb7ba-142">NOTES</span></span>

## <span data-ttu-id="cb7ba-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb7ba-143">RELATED LINKS</span></span>
