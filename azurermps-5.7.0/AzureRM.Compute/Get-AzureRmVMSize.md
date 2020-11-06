---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546876"
---
# <span data-ttu-id="5fbca-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="5fbca-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="5fbca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fbca-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbca-103">Pobiera dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5fbca-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fbca-104">SYNTAX</span></span>

### <span data-ttu-id="5fbca-105">ListVirtualMachineSizeParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fbca-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="5fbca-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5fbca-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="5fbca-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5fbca-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="5fbca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5fbca-108">DESCRIPTION</span></span>
<span data-ttu-id="5fbca-109">Polecenie cmdlet **Get-AzureRmVMSize** Pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5fbca-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="5fbca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fbca-110">EXAMPLES</span></span>

### <span data-ttu-id="5fbca-111">Przykład 1: pobieranie rozmiaru maszyny wirtualnej dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="5fbca-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="5fbca-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5fbca-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="5fbca-113">Przykład 2: uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="5fbca-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="5fbca-114">To polecenie pobiera dostępne rozmiary maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="5fbca-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="5fbca-115">Przykład 3: uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5fbca-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="5fbca-116">To polecenie pobiera dostępne rozmiary dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="5fbca-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="5fbca-117">Możesz zmienić rozmiar maszyny wirtualnej na rozmiar, jaki to polecenie pobiera.</span><span class="sxs-lookup"><span data-stu-id="5fbca-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="5fbca-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fbca-118">PARAMETERS</span></span>

### <span data-ttu-id="5fbca-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="5fbca-119">-AvailabilitySetName</span></span>
<span data-ttu-id="5fbca-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5fbca-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbca-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5fbca-121">-Location</span></span>
<span data-ttu-id="5fbca-122">Określa lokalizację, w której to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5fbca-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbca-123">-ResourceGroupName</span></span>
<span data-ttu-id="5fbca-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5fbca-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbca-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="5fbca-125">-VMName</span></span>
<span data-ttu-id="5fbca-126">Określa nazwę maszyny wirtualnej, którą to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej w celu zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="5fbca-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbca-127">CommonParameters</span></span>
<span data-ttu-id="5fbca-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbca-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbca-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbca-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fbca-130">INPUTS</span></span>

### <span data-ttu-id="5fbca-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5fbca-131">None</span></span>
<span data-ttu-id="5fbca-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5fbca-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fbca-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fbca-133">OUTPUTS</span></span>

## <span data-ttu-id="5fbca-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fbca-134">NOTES</span></span>

## <span data-ttu-id="5fbca-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fbca-135">RELATED LINKS</span></span>

[<span data-ttu-id="5fbca-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5fbca-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


