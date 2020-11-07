---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fff76d83c3cb80c620414d07808e473ac3892e99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708771"
---
# <span data-ttu-id="657e5-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="657e5-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="657e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="657e5-102">SYNOPSIS</span></span>
<span data-ttu-id="657e5-103">Umożliwia usunięcie wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="657e5-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="657e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="657e5-104">SYNTAX</span></span>

### <span data-ttu-id="657e5-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="657e5-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="657e5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="657e5-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="657e5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="657e5-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="657e5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="657e5-108">DESCRIPTION</span></span>
<span data-ttu-id="657e5-109">Polecenie cmdlet Remove-AzPowerBIEmbeddedCapacity powoduje usunięcie wystąpienia zaosadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="657e5-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="657e5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="657e5-110">EXAMPLES</span></span>

### <span data-ttu-id="657e5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="657e5-111">Example 1</span></span>
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

<span data-ttu-id="657e5-112">To polecenie usunie pojemność o nazwie testcapacity w oknie resourceName testRG</span><span class="sxs-lookup"><span data-stu-id="657e5-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="657e5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="657e5-113">PARAMETERS</span></span>

### <span data-ttu-id="657e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657e5-114">-DefaultProfile</span></span>
<span data-ttu-id="657e5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="657e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="657e5-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="657e5-116">-InputObject</span></span>
<span data-ttu-id="657e5-117">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="657e5-117">Input object for Piping</span></span>

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

### <span data-ttu-id="657e5-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="657e5-118">-Name</span></span>
<span data-ttu-id="657e5-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="657e5-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="657e5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="657e5-120">-PassThru</span></span>
<span data-ttu-id="657e5-121">Zwraca szczegóły usuniętej pojemności, jeśli operacja zostanie ukończona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="657e5-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="657e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="657e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="657e5-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="657e5-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="657e5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="657e5-124">-ResourceId</span></span>
<span data-ttu-id="657e5-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="657e5-125">Azure resource ID</span></span>

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

### <span data-ttu-id="657e5-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="657e5-126">-Confirm</span></span>
<span data-ttu-id="657e5-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="657e5-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="657e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657e5-128">-WhatIf</span></span>
<span data-ttu-id="657e5-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="657e5-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="657e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657e5-130">CommonParameters</span></span>
<span data-ttu-id="657e5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657e5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657e5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657e5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="657e5-133">INPUTS</span></span>

### <span data-ttu-id="657e5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="657e5-134">System.String</span></span>

### <span data-ttu-id="657e5-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="657e5-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="657e5-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="657e5-136">OUTPUTS</span></span>

### <span data-ttu-id="657e5-137">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="657e5-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="657e5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="657e5-138">NOTES</span></span>

## <span data-ttu-id="657e5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="657e5-139">RELATED LINKS</span></span>

[<span data-ttu-id="657e5-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="657e5-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="657e5-141">Nowe — AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="657e5-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
