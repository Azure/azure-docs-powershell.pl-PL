---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 93c15d2675cc0e3e5fe0b37bc5af331ce97e7d8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953450"
---
# <span data-ttu-id="a6152-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a6152-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a6152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6152-102">SYNOPSIS</span></span>
<span data-ttu-id="a6152-103">Usuwa wystąpienie osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a6152-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="a6152-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6152-104">SYNTAX</span></span>

### <span data-ttu-id="a6152-105">ByNameAndResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a6152-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6152-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6152-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6152-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6152-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6152-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6152-108">DESCRIPTION</span></span>
<span data-ttu-id="a6152-109">Polecenie Remove-AzPowerBIEmbeddedCapacity cmdlet usuwa wystąpienie osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="a6152-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a6152-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6152-110">EXAMPLES</span></span>

### <span data-ttu-id="a6152-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6152-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="a6152-112">To polecenie usunie wydajność o nazwie testcapacity w teścieRG grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a6152-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a6152-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6152-113">PARAMETERS</span></span>

### <span data-ttu-id="a6152-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6152-114">-DefaultProfile</span></span>
<span data-ttu-id="a6152-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6152-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6152-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6152-116">-InputObject</span></span>
<span data-ttu-id="a6152-117">Obiekt wejściowy dla funkcji Piping</span><span class="sxs-lookup"><span data-stu-id="a6152-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6152-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6152-118">-Name</span></span>
<span data-ttu-id="a6152-119">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="a6152-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6152-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6152-120">-PassThru</span></span>
<span data-ttu-id="a6152-121">Jeśli operacja zostanie pomyślnie ukończona, zostaną zwrócone szczegółowe informacje o usuniętej pojemności.</span><span class="sxs-lookup"><span data-stu-id="a6152-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="a6152-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6152-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6152-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="a6152-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6152-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6152-124">-ResourceId</span></span>
<span data-ttu-id="a6152-125">Identyfikator zasobu Azure</span><span class="sxs-lookup"><span data-stu-id="a6152-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6152-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6152-126">-Confirm</span></span>
<span data-ttu-id="a6152-127">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="a6152-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a6152-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6152-128">-WhatIf</span></span>
<span data-ttu-id="a6152-129">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="a6152-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a6152-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6152-130">CommonParameters</span></span>
<span data-ttu-id="a6152-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6152-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6152-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6152-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6152-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6152-133">INPUTS</span></span>

### <span data-ttu-id="a6152-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a6152-134">System.String</span></span>

### <span data-ttu-id="a6152-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a6152-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a6152-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6152-136">OUTPUTS</span></span>

### <span data-ttu-id="a6152-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a6152-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a6152-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6152-138">NOTES</span></span>

## <span data-ttu-id="a6152-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6152-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6152-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a6152-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a6152-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a6152-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
