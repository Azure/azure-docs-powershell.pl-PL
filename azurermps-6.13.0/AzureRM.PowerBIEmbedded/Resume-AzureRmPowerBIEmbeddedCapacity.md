---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 29113eecc02443fe2fbc8f57ada1fcfa8e7a2d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541580"
---
# <span data-ttu-id="a5a0c-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a0c-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a5a0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a0c-103">Wznawia działanie wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a5a0c-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5a0c-104">SYNTAX</span></span>

### <span data-ttu-id="a5a0c-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5a0c-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a0c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a0c-106">ByResourceId</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a0c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5a0c-107">ByInputObject</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a0c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="a5a0c-109">Polecenie cmdlet Resume-AzureRmPowerBIEmbeddedCapacity wznawia działanie wystąpienia z zaimportowaną pojemnością usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="a5a0c-109">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a5a0c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="a5a0c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5a0c-111">Example 1</span></span>
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

<span data-ttu-id="a5a0c-112">To polecenie spowoduje wznowienie wstrzymanej pojemności o nazwie testcapacity w oknie Resources testRG</span><span class="sxs-lookup"><span data-stu-id="a5a0c-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a5a0c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5a0c-113">PARAMETERS</span></span>

### <span data-ttu-id="a5a0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a0c-114">-DefaultProfile</span></span>
<span data-ttu-id="a5a0c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a0c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5a0c-116">-InputObject</span></span>
<span data-ttu-id="a5a0c-117">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a5a0c-117">Input object for Piping</span></span>

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

### <span data-ttu-id="a5a0c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5a0c-118">-Name</span></span>
<span data-ttu-id="a5a0c-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="a5a0c-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a5a0c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a0c-120">-PassThru</span></span>
<span data-ttu-id="a5a0c-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a5a0c-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a5a0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5a0c-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="a5a0c-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a5a0c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a0c-124">-ResourceId</span></span>
<span data-ttu-id="a5a0c-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a5a0c-125">Azure resource ID</span></span>

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

### <span data-ttu-id="a5a0c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5a0c-126">-Confirm</span></span>
<span data-ttu-id="a5a0c-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="a5a0c-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a5a0c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a0c-128">-WhatIf</span></span>
<span data-ttu-id="a5a0c-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="a5a0c-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a5a0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a0c-130">CommonParameters</span></span>
<span data-ttu-id="a5a0c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a0c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a0c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5a0c-133">INPUTS</span></span>

### <span data-ttu-id="a5a0c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a0c-134">System.String</span></span>

### <span data-ttu-id="a5a0c-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a0c-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="a5a0c-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5a0c-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5a0c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5a0c-137">OUTPUTS</span></span>

### <span data-ttu-id="a5a0c-138">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a0c-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a5a0c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5a0c-139">NOTES</span></span>

## <span data-ttu-id="a5a0c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5a0c-140">RELATED LINKS</span></span>

[<span data-ttu-id="a5a0c-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a0c-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a5a0c-142">Suspend — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a0c-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
