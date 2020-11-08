---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233647"
---
# <span data-ttu-id="21032-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="21032-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="21032-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21032-102">SYNOPSIS</span></span>
<span data-ttu-id="21032-103">Wstrzymuje działanie wystąpienia osadzonych możliwości usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="21032-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="21032-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21032-104">SYNTAX</span></span>

### <span data-ttu-id="21032-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21032-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21032-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21032-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21032-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21032-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21032-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21032-108">DESCRIPTION</span></span>
<span data-ttu-id="21032-109">Polecenie cmdlet Suspend-AzPowerBIEmbeddedCapacity wstrzymuje wystąpienie z osadzoną pojemnością usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="21032-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="21032-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21032-110">EXAMPLES</span></span>

### <span data-ttu-id="21032-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21032-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="21032-112">To polecenie zawiesić aktywną pojemność o nazwie testcapacity w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="21032-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="21032-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21032-113">PARAMETERS</span></span>

### <span data-ttu-id="21032-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21032-114">-DefaultProfile</span></span>
<span data-ttu-id="21032-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21032-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21032-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21032-116">-InputObject</span></span>
<span data-ttu-id="21032-117">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="21032-117">Input object for Piping</span></span>

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

### <span data-ttu-id="21032-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21032-118">-Name</span></span>
<span data-ttu-id="21032-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="21032-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="21032-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21032-120">-PassThru</span></span>
<span data-ttu-id="21032-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="21032-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="21032-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21032-122">-ResourceGroupName</span></span>
<span data-ttu-id="21032-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="21032-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="21032-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21032-124">-ResourceId</span></span>
<span data-ttu-id="21032-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="21032-125">Azure resource ID</span></span>

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

### <span data-ttu-id="21032-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21032-126">-Confirm</span></span>
<span data-ttu-id="21032-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="21032-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="21032-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21032-128">-WhatIf</span></span>
<span data-ttu-id="21032-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="21032-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="21032-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21032-130">CommonParameters</span></span>
<span data-ttu-id="21032-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21032-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21032-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21032-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21032-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21032-133">INPUTS</span></span>

### <span data-ttu-id="21032-134">System. String</span><span class="sxs-lookup"><span data-stu-id="21032-134">System.String</span></span>

### <span data-ttu-id="21032-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="21032-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="21032-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21032-136">OUTPUTS</span></span>

### <span data-ttu-id="21032-137">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="21032-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="21032-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21032-138">NOTES</span></span>

## <span data-ttu-id="21032-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21032-139">RELATED LINKS</span></span>

[<span data-ttu-id="21032-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="21032-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="21032-141">Życiorys — AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="21032-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

