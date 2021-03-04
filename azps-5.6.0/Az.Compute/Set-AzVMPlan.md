---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 9d3897b52d59c85caac3f68b9904878f14014606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004554"
---
# <span data-ttu-id="4d508-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="4d508-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="4d508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d508-102">SYNOPSIS</span></span>
<span data-ttu-id="4d508-103">Ustawia informacje o planie usługi Marketplace na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="4d508-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="4d508-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d508-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d508-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d508-105">DESCRIPTION</span></span>
<span data-ttu-id="4d508-106">Polecenie **cmdlet Set-AzVMPlan** ustawia informacje o planie usługi Azure Marketplace dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d508-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="4d508-107">Aby można było wdrożyć obraz witryny Marketplace za pośrednictwem wiersza polecenia, należy włączyć dostęp programowy lub wdrożyć maszynę wirtualną za pomocą portalu Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="4d508-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="4d508-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d508-108">EXAMPLES</span></span>

## <span data-ttu-id="4d508-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d508-109">PARAMETERS</span></span>

### <span data-ttu-id="4d508-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d508-110">-DefaultProfile</span></span>
<span data-ttu-id="4d508-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d508-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d508-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d508-112">-Name</span></span>
<span data-ttu-id="4d508-113">Określa nazwę obrazu z witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4d508-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="4d508-114">Jest to ta sama wartość, która jest zwracana przez Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d508-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="4d508-115">Aby uzyskać więcej informacji o tym, jak znaleźć informacje o obrazach, zobacz Nawigowanie po obrazach maszyn wirtualnych platformy Azure i wybieranie ich za pomocą programu PowerShell i interfejsu cli platformy Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (w https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) dokumentacji platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="4d508-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d508-116">— Produkt</span><span class="sxs-lookup"><span data-stu-id="4d508-116">-Product</span></span>
<span data-ttu-id="4d508-117">Określa igiełę obrazu z witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4d508-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="4d508-118">Są to te same informacje co wartość **Offer** elementu **imageReference.**</span><span class="sxs-lookup"><span data-stu-id="4d508-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d508-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="4d508-119">-PromotionCode</span></span>
<span data-ttu-id="4d508-120">Określa kod promocyjny.</span><span class="sxs-lookup"><span data-stu-id="4d508-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d508-121">— Publisher</span><span class="sxs-lookup"><span data-stu-id="4d508-121">-Publisher</span></span>
<span data-ttu-id="4d508-122">Określa wydawcę obrazu.</span><span class="sxs-lookup"><span data-stu-id="4d508-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="4d508-123">Możesz znaleźć te informacje za pomocą polecenia cmdlet Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d508-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d508-124">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="4d508-124">-VM</span></span>
<span data-ttu-id="4d508-125">Określa obiekt maszyny wirtualnej, dla którego ma być ustawiany plan usługi Marketplace.</span><span class="sxs-lookup"><span data-stu-id="4d508-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="4d508-126">Możesz użyć tego Get-AzVM cmdlet, aby uzyskać obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d508-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="4d508-127">Możesz użyć polecenia cmdlet New-AzVMConfig, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d508-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d508-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d508-128">CommonParameters</span></span>
<span data-ttu-id="4d508-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d508-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d508-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d508-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d508-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d508-131">INPUTS</span></span>

### <span data-ttu-id="4d508-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4d508-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4d508-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d508-133">System.String</span></span>

## <span data-ttu-id="4d508-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d508-134">OUTPUTS</span></span>

### <span data-ttu-id="4d508-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4d508-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4d508-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d508-136">NOTES</span></span>

## <span data-ttu-id="4d508-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d508-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d508-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4d508-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4d508-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4d508-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="4d508-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4d508-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="4d508-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4d508-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
