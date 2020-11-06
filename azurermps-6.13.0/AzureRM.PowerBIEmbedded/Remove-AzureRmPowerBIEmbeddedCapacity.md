---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c2dc0333d2e991b21ac1a921465971f2131f5c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549311"
---
# <span data-ttu-id="0c97f-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0c97f-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0c97f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c97f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c97f-103">Umożliwia usunięcie wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="0c97f-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c97f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c97f-104">SYNTAX</span></span>

### <span data-ttu-id="0c97f-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c97f-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c97f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c97f-106">ByResourceId</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c97f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c97f-107">ByInputObject</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c97f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0c97f-108">DESCRIPTION</span></span>
<span data-ttu-id="0c97f-109">Polecenie cmdlet Remove-AzureRmPowerBIEmbeddedCapacity powoduje usunięcie wystąpienia zaosadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="0c97f-109">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="0c97f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c97f-110">EXAMPLES</span></span>

### <span data-ttu-id="0c97f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c97f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="0c97f-112">To polecenie usunie pojemność o nazwie testcapacity w oknie resourceName testRG</span><span class="sxs-lookup"><span data-stu-id="0c97f-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="0c97f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c97f-113">PARAMETERS</span></span>

### <span data-ttu-id="0c97f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c97f-114">-DefaultProfile</span></span>
<span data-ttu-id="0c97f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c97f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c97f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c97f-116">-InputObject</span></span>
<span data-ttu-id="0c97f-117">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="0c97f-117">Input object for Piping</span></span>

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

### <span data-ttu-id="0c97f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c97f-118">-Name</span></span>
<span data-ttu-id="0c97f-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="0c97f-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="0c97f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c97f-120">-PassThru</span></span>
<span data-ttu-id="0c97f-121">Zwraca szczegóły usuniętej pojemności, jeśli operacja zostanie ukończona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="0c97f-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0c97f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c97f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c97f-123">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="0c97f-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="0c97f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c97f-124">-ResourceId</span></span>
<span data-ttu-id="0c97f-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0c97f-125">Azure resource ID</span></span>

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

### <span data-ttu-id="0c97f-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c97f-126">-Confirm</span></span>
<span data-ttu-id="0c97f-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="0c97f-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0c97f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c97f-128">-WhatIf</span></span>
<span data-ttu-id="0c97f-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="0c97f-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0c97f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c97f-130">CommonParameters</span></span>
<span data-ttu-id="0c97f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c97f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c97f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c97f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c97f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c97f-133">INPUTS</span></span>

### <span data-ttu-id="0c97f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0c97f-134">System.String</span></span>

### <span data-ttu-id="0c97f-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0c97f-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="0c97f-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c97f-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0c97f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c97f-137">OUTPUTS</span></span>

### <span data-ttu-id="0c97f-138">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0c97f-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0c97f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c97f-139">NOTES</span></span>

## <span data-ttu-id="0c97f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c97f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c97f-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0c97f-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="0c97f-142">Nowe — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0c97f-142">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
