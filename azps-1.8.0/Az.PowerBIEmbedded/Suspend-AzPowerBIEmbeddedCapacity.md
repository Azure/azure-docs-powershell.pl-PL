---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708766"
---
# <span data-ttu-id="d1b9e-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1b9e-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1b9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b9e-103">Wstrzymuje działanie wystąpienia osadzonych możliwości usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d1b9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1b9e-104">SYNTAX</span></span>

### <span data-ttu-id="d1b9e-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1b9e-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1b9e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1b9e-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1b9e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1b9e-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1b9e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d1b9e-108">DESCRIPTION</span></span>
<span data-ttu-id="d1b9e-109">Polecenie cmdlet Suspend-AzPowerBIEmbeddedCapacity wstrzymuje wystąpienie z osadzoną pojemnością usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1b9e-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d1b9e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1b9e-110">EXAMPLES</span></span>

### <span data-ttu-id="d1b9e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1b9e-111">Example 1</span></span>
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

<span data-ttu-id="d1b9e-112">To polecenie zawiesić aktywną pojemność o nazwie testcapacity w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d1b9e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1b9e-113">PARAMETERS</span></span>

### <span data-ttu-id="d1b9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b9e-114">-DefaultProfile</span></span>
<span data-ttu-id="d1b9e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1b9e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1b9e-116">-InputObject</span></span>
<span data-ttu-id="d1b9e-117">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="d1b9e-117">Input object for Piping</span></span>

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

### <span data-ttu-id="d1b9e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1b9e-118">-Name</span></span>
<span data-ttu-id="d1b9e-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1b9e-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d1b9e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1b9e-120">-PassThru</span></span>
<span data-ttu-id="d1b9e-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d1b9e-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d1b9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1b9e-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="d1b9e-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="d1b9e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1b9e-124">-ResourceId</span></span>
<span data-ttu-id="d1b9e-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d1b9e-125">Azure resource ID</span></span>

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

### <span data-ttu-id="d1b9e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1b9e-126">-Confirm</span></span>
<span data-ttu-id="d1b9e-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d1b9e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b9e-128">-WhatIf</span></span>
<span data-ttu-id="d1b9e-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d1b9e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b9e-130">CommonParameters</span></span>
<span data-ttu-id="d1b9e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b9e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b9e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b9e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1b9e-133">INPUTS</span></span>

### <span data-ttu-id="d1b9e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d1b9e-134">System.String</span></span>

### <span data-ttu-id="d1b9e-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1b9e-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1b9e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1b9e-136">OUTPUTS</span></span>

### <span data-ttu-id="d1b9e-137">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1b9e-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1b9e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1b9e-138">NOTES</span></span>

## <span data-ttu-id="d1b9e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1b9e-139">RELATED LINKS</span></span>

[<span data-ttu-id="d1b9e-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1b9e-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d1b9e-141">Życiorys — AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1b9e-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

