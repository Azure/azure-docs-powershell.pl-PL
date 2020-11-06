---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525046"
---
# <span data-ttu-id="90206-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="90206-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="90206-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90206-102">SYNOPSIS</span></span>
<span data-ttu-id="90206-103">Wstrzymuje działanie wystąpienia osadzonych możliwości usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="90206-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90206-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90206-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="90206-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90206-105">DESCRIPTION</span></span>
<span data-ttu-id="90206-106">Polecenie cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity wstrzymuje wystąpienie z osadzoną pojemnością usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="90206-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="90206-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90206-107">EXAMPLES</span></span>

### <span data-ttu-id="90206-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90206-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="90206-109">To polecenie zawiesić aktywną pojemność o nazwie testcapacity w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="90206-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="90206-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90206-110">PARAMETERS</span></span>

### <span data-ttu-id="90206-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90206-111">-Name</span></span>
<span data-ttu-id="90206-112">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="90206-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="90206-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90206-113">-ResourceGroupName</span></span>
<span data-ttu-id="90206-114">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="90206-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="90206-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90206-115">-ResourceId</span></span>
<span data-ttu-id="90206-116">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="90206-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90206-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90206-117">-InputObject</span></span>
<span data-ttu-id="90206-118">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="90206-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90206-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90206-119">-Confirm</span></span>
<span data-ttu-id="90206-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="90206-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90206-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90206-121">-WhatIf</span></span>
<span data-ttu-id="90206-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="90206-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90206-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90206-123">CommonParameters</span></span>
<span data-ttu-id="90206-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90206-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90206-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90206-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90206-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90206-126">INPUTS</span></span>

### <span data-ttu-id="90206-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90206-127">None</span></span>
<span data-ttu-id="90206-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="90206-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90206-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90206-129">OUTPUTS</span></span>

### <span data-ttu-id="90206-130">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="90206-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="90206-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90206-131">NOTES</span></span>

## <span data-ttu-id="90206-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90206-132">RELATED LINKS</span></span>

[<span data-ttu-id="90206-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="90206-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="90206-134">Życiorys — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="90206-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

