---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525061"
---
# <span data-ttu-id="64058-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64058-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64058-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64058-102">SYNOPSIS</span></span>
<span data-ttu-id="64058-103">Wznawia działanie wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="64058-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64058-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64058-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="64058-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64058-105">DESCRIPTION</span></span>
<span data-ttu-id="64058-106">Polecenie cmdlet Resume-AzureRmPowerBIEmbeddedCapacity wznawia działanie wystąpienia z zaimportowaną pojemnością usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="64058-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="64058-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64058-107">EXAMPLES</span></span>

### <span data-ttu-id="64058-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64058-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="64058-109">To polecenie spowoduje wznowienie wstrzymanej pojemności o nazwie testcapacity w oknie Resources testRG</span><span class="sxs-lookup"><span data-stu-id="64058-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="64058-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64058-110">PARAMETERS</span></span>

### <span data-ttu-id="64058-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64058-111">-Name</span></span>
<span data-ttu-id="64058-112">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="64058-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64058-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64058-113">-ResourceGroupName</span></span>
<span data-ttu-id="64058-114">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="64058-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64058-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64058-115">-ResourceId</span></span>
<span data-ttu-id="64058-116">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="64058-116">Azure resource ID</span></span>

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

### <span data-ttu-id="64058-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64058-117">-InputObject</span></span>
<span data-ttu-id="64058-118">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="64058-118">Input object for Piping</span></span>

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

### <span data-ttu-id="64058-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64058-119">-Confirm</span></span>
<span data-ttu-id="64058-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="64058-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="64058-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64058-121">-WhatIf</span></span>
<span data-ttu-id="64058-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="64058-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="64058-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64058-123">CommonParameters</span></span>
<span data-ttu-id="64058-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64058-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64058-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64058-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64058-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64058-126">INPUTS</span></span>

### <span data-ttu-id="64058-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64058-127">None</span></span>
<span data-ttu-id="64058-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="64058-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64058-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64058-129">OUTPUTS</span></span>

### <span data-ttu-id="64058-130">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64058-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64058-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64058-131">NOTES</span></span>

## <span data-ttu-id="64058-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64058-132">RELATED LINKS</span></span>

[<span data-ttu-id="64058-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64058-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="64058-134">Suspend — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64058-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
