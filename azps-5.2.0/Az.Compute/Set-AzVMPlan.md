---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362336"
---
# <span data-ttu-id="57b41-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="57b41-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="57b41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57b41-102">SYNOPSIS</span></span>
<span data-ttu-id="57b41-103">Umożliwia ustawienie informacji dotyczących planu rynkowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57b41-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="57b41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57b41-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57b41-105">DESCRIPTION</span></span>
<span data-ttu-id="57b41-106">Polecenie cmdlet **Set-AzVMPlan** ustawia informacje dotyczące planu Azure Marketplace dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57b41-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="57b41-107">Przed rozpoczęciem wdrażania obrazu witryny Marketplace za pośrednictwem wiersza polecenia program dostęp programistyczny musi być włączony lub wdrożenie maszyny wirtualnej za pomocą portalu Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="57b41-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57b41-108">EXAMPLES</span></span>

## <span data-ttu-id="57b41-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57b41-109">PARAMETERS</span></span>

### <span data-ttu-id="57b41-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b41-110">-DefaultProfile</span></span>
<span data-ttu-id="57b41-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57b41-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57b41-112">-Name</span></span>
<span data-ttu-id="57b41-113">Określa nazwę obrazu na podstawie witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="57b41-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="57b41-114">Jest to ta sama wartość, która jest zwracana przez polecenie cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="57b41-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="57b41-115">Aby uzyskać więcej informacji na temat znajdowania informacji o obrazach, zobacz Nawigowanie i wybieranie obrazów maszyny wirtualnej platformy Azure za pomocą programu PowerShell i usługi Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) w dokumentacji platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="57b41-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="57b41-116">-Product</span><span class="sxs-lookup"><span data-stu-id="57b41-116">-Product</span></span>
<span data-ttu-id="57b41-117">Określa iloczyn obrazu z witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="57b41-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="57b41-118">Jest to ta sama informacja, co wartość **oferty** elementu **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="57b41-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="57b41-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="57b41-119">-PromotionCode</span></span>
<span data-ttu-id="57b41-120">Określa kod promocyjny.</span><span class="sxs-lookup"><span data-stu-id="57b41-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="57b41-121">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="57b41-121">-Publisher</span></span>
<span data-ttu-id="57b41-122">Umożliwia określenie wydawcy obrazu.</span><span class="sxs-lookup"><span data-stu-id="57b41-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="57b41-123">Te informacje można znaleźć przy użyciu Get-AzVMImagePublisher polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b41-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="57b41-124">-VM</span><span class="sxs-lookup"><span data-stu-id="57b41-124">-VM</span></span>
<span data-ttu-id="57b41-125">Określa obiekt maszyny wirtualnej, dla którego ma zostać ustawiony plan rynku.</span><span class="sxs-lookup"><span data-stu-id="57b41-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="57b41-126">Możesz użyć polecenia cmdlet Get-AzVM, aby uzyskać obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57b41-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="57b41-127">Możesz użyć polecenia cmdlet New-AzVMConfig, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57b41-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="57b41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b41-128">CommonParameters</span></span>
<span data-ttu-id="57b41-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b41-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57b41-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b41-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57b41-131">INPUTS</span></span>

### <span data-ttu-id="57b41-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57b41-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="57b41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="57b41-133">System.String</span></span>

## <span data-ttu-id="57b41-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57b41-134">OUTPUTS</span></span>

### <span data-ttu-id="57b41-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57b41-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="57b41-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57b41-136">NOTES</span></span>

## <span data-ttu-id="57b41-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57b41-137">RELATED LINKS</span></span>

[<span data-ttu-id="57b41-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="57b41-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="57b41-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="57b41-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="57b41-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="57b41-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="57b41-141">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
