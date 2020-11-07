---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716628"
---
# <span data-ttu-id="cc53a-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="cc53a-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="cc53a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc53a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc53a-103">Umożliwia ustawienie informacji dotyczących planu rynkowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc53a-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc53a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc53a-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc53a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc53a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc53a-106">Polecenie cmdlet **Set-AzureRmVMPlan** ustawia informacje dotyczące planu Azure Marketplace dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc53a-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="cc53a-107">Przed rozpoczęciem wdrażania obrazu witryny Marketplace za pośrednictwem wiersza polecenia program dostęp programistyczny musi być włączony lub wdrożenie maszyny wirtualnej za pomocą portalu Azure.</span><span class="sxs-lookup"><span data-stu-id="cc53a-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="cc53a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc53a-108">EXAMPLES</span></span>

## <span data-ttu-id="cc53a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc53a-109">PARAMETERS</span></span>

### <span data-ttu-id="cc53a-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc53a-110">-Name</span></span>
<span data-ttu-id="cc53a-111">Określa nazwę obrazu na podstawie witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="cc53a-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="cc53a-112">Jest to ta sama wartość, która jest zwracana przez polecenie cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="cc53a-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="cc53a-113">Aby uzyskać więcej informacji na temat znajdowania informacji o obrazach, zobacz [nawigowanie i wybieranie obrazów maszyny wirtualnej platformy Azure za pomocą programu PowerShell i usługi Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) w dokumentacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc53a-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53a-114">-Product</span><span class="sxs-lookup"><span data-stu-id="cc53a-114">-Product</span></span>
<span data-ttu-id="cc53a-115">Określa iloczyn obrazu z witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="cc53a-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="cc53a-116">Jest to ta sama informacja, co wartość **oferty** elementu **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="cc53a-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53a-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="cc53a-117">-PromotionCode</span></span>
<span data-ttu-id="cc53a-118">Określa kod promocyjny.</span><span class="sxs-lookup"><span data-stu-id="cc53a-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53a-119">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="cc53a-119">-Publisher</span></span>
<span data-ttu-id="cc53a-120">Umożliwia określenie wydawcy obrazu.</span><span class="sxs-lookup"><span data-stu-id="cc53a-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="cc53a-121">Te informacje można znaleźć przy użyciu Get-AzureRmVMImagePublisher polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc53a-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53a-122">-VM</span><span class="sxs-lookup"><span data-stu-id="cc53a-122">-VM</span></span>
<span data-ttu-id="cc53a-123">Określa obiekt maszyny wirtualnej, dla którego ma zostać ustawiony plan rynku.</span><span class="sxs-lookup"><span data-stu-id="cc53a-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="cc53a-124">Możesz użyć polecenia cmdlet Get-AzureRmVM, aby uzyskać obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc53a-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="cc53a-125">Możesz użyć polecenia cmdlet New-AzureRmVMConfig, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc53a-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc53a-126">CommonParameters</span></span>
<span data-ttu-id="cc53a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc53a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc53a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc53a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc53a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc53a-129">INPUTS</span></span>

### <span data-ttu-id="cc53a-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc53a-130">None</span></span>
<span data-ttu-id="cc53a-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cc53a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc53a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc53a-132">OUTPUTS</span></span>

## <span data-ttu-id="cc53a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc53a-133">NOTES</span></span>

## <span data-ttu-id="cc53a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc53a-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc53a-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc53a-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cc53a-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cc53a-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="cc53a-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cc53a-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="cc53a-138">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="cc53a-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
