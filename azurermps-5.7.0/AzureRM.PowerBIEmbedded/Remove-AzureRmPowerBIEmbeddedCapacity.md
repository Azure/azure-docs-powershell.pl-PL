---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717724"
---
# <span data-ttu-id="107fb-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="107fb-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="107fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="107fb-102">SYNOPSIS</span></span>
<span data-ttu-id="107fb-103">Umożliwia usunięcie wystąpienia z osadzonymi możliwościami usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="107fb-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="107fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="107fb-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="107fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="107fb-105">DESCRIPTION</span></span>
<span data-ttu-id="107fb-106">Polecenie cmdlet Remove-AzureRmPowerBIEmbeddedCapacity powoduje usunięcie wystąpienia zaosadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="107fb-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="107fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="107fb-107">EXAMPLES</span></span>

### <span data-ttu-id="107fb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="107fb-108">Example 1</span></span>
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

<span data-ttu-id="107fb-109">To polecenie usunie pojemność o nazwie testcapacity w oknie resourceName testRG</span><span class="sxs-lookup"><span data-stu-id="107fb-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="107fb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="107fb-110">PARAMETERS</span></span>

### <span data-ttu-id="107fb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107fb-111">-ResourceGroupName</span></span>
<span data-ttu-id="107fb-112">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="107fb-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="107fb-113">-Name</span></span>
<span data-ttu-id="107fb-114">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="107fb-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="107fb-115">-ResourceId</span></span>
<span data-ttu-id="107fb-116">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="107fb-116">Azure resource ID</span></span>

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

### <span data-ttu-id="107fb-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="107fb-117">-InputObject</span></span>
<span data-ttu-id="107fb-118">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="107fb-118">Input object for Piping</span></span>

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

### <span data-ttu-id="107fb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107fb-119">-PassThru</span></span>
<span data-ttu-id="107fb-120">Zwraca szczegóły usuniętej pojemności, jeśli operacja zostanie ukończona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="107fb-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="107fb-121">-Confirm</span></span>
<span data-ttu-id="107fb-122">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="107fb-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="107fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107fb-123">-WhatIf</span></span>
<span data-ttu-id="107fb-124">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="107fb-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="107fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107fb-125">CommonParameters</span></span>
<span data-ttu-id="107fb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107fb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107fb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="107fb-128">INPUTS</span></span>

### <span data-ttu-id="107fb-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="107fb-129">None</span></span>
<span data-ttu-id="107fb-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="107fb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="107fb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="107fb-131">OUTPUTS</span></span>

### <span data-ttu-id="107fb-132">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="107fb-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="107fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="107fb-133">NOTES</span></span>

## <span data-ttu-id="107fb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="107fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="107fb-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="107fb-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="107fb-136">Nowe — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="107fb-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
