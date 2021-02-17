---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189354"
---
# <span data-ttu-id="4a112-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a112-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a112-102">SYNOPSIS</span></span>
<span data-ttu-id="4a112-103">Wznawia wystąpienie osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4a112-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4a112-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a112-104">SYNTAX</span></span>

### <span data-ttu-id="4a112-105">ByNameAndResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4a112-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a112-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a112-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a112-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a112-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a112-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a112-108">DESCRIPTION</span></span>
<span data-ttu-id="4a112-109">Polecenie Resume-AzPowerBIEmbeddedCapacity cmdlet wznawia wystąpienie osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="4a112-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4a112-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a112-110">EXAMPLES</span></span>

### <span data-ttu-id="4a112-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a112-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="4a112-112">To polecenie spowoduje wznowienie wstrzymanej wydajności o nazwie testcapacity w testRG grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4a112-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="4a112-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a112-113">PARAMETERS</span></span>

### <span data-ttu-id="4a112-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a112-114">-DefaultProfile</span></span>
<span data-ttu-id="4a112-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a112-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a112-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a112-116">-InputObject</span></span>
<span data-ttu-id="4a112-117">Obiekt wejściowy dla funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="4a112-117">Input object for Piping</span></span>

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

### <span data-ttu-id="4a112-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a112-118">-Name</span></span>
<span data-ttu-id="4a112-119">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="4a112-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4a112-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a112-120">-PassThru</span></span>
<span data-ttu-id="4a112-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4a112-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4a112-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a112-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a112-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="4a112-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4a112-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a112-124">-ResourceId</span></span>
<span data-ttu-id="4a112-125">Identyfikator zasobu Azure</span><span class="sxs-lookup"><span data-stu-id="4a112-125">Azure resource ID</span></span>

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

### <span data-ttu-id="4a112-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a112-126">-Confirm</span></span>
<span data-ttu-id="4a112-127">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="4a112-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4a112-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a112-128">-WhatIf</span></span>
<span data-ttu-id="4a112-129">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="4a112-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4a112-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a112-130">CommonParameters</span></span>
<span data-ttu-id="4a112-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a112-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a112-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a112-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a112-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a112-133">INPUTS</span></span>

### <span data-ttu-id="4a112-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4a112-134">System.String</span></span>

### <span data-ttu-id="4a112-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a112-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a112-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a112-136">OUTPUTS</span></span>

### <span data-ttu-id="4a112-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a112-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a112-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a112-138">NOTES</span></span>

## <span data-ttu-id="4a112-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a112-139">RELATED LINKS</span></span>

[<span data-ttu-id="4a112-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a112-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4a112-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a112-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
