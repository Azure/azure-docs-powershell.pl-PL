---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
ms.openlocfilehash: 77e4de344e3dd89eac09b1ebefb6ba49071dcbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899385"
---
# <span data-ttu-id="9536a-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="9536a-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="9536a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9536a-102">SYNOPSIS</span></span>
<span data-ttu-id="9536a-103">Pobiera dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="9536a-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9536a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9536a-104">SYNTAX</span></span>

### <span data-ttu-id="9536a-105">ListVirtualMachineSizeParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9536a-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9536a-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9536a-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9536a-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9536a-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9536a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9536a-108">DESCRIPTION</span></span>
<span data-ttu-id="9536a-109">Polecenie cmdlet **Get-AzureRmVMSize** Pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9536a-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="9536a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9536a-110">EXAMPLES</span></span>

### <span data-ttu-id="9536a-111">Przykład 1: pobieranie rozmiaru maszyny wirtualnej dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="9536a-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="9536a-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9536a-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="9536a-113">Przykład 2: uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="9536a-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="9536a-114">To polecenie pobiera dostępne rozmiary maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="9536a-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="9536a-115">Przykład 3: uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9536a-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="9536a-116">To polecenie pobiera dostępne rozmiary dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="9536a-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="9536a-117">Możesz zmienić rozmiar maszyny wirtualnej na rozmiar, jaki to polecenie pobiera.</span><span class="sxs-lookup"><span data-stu-id="9536a-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="9536a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9536a-118">PARAMETERS</span></span>

### <span data-ttu-id="9536a-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="9536a-119">-AvailabilitySetName</span></span>
<span data-ttu-id="9536a-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9536a-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="9536a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9536a-121">-DefaultProfile</span></span>
<span data-ttu-id="9536a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9536a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9536a-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9536a-123">-Location</span></span>
<span data-ttu-id="9536a-124">Określa lokalizację, w której to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9536a-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="9536a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9536a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9536a-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9536a-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9536a-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="9536a-127">-VMName</span></span>
<span data-ttu-id="9536a-128">Określa nazwę maszyny wirtualnej, którą to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej w celu zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="9536a-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="9536a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9536a-129">CommonParameters</span></span>
<span data-ttu-id="9536a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9536a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9536a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9536a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9536a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9536a-132">INPUTS</span></span>

### <span data-ttu-id="9536a-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9536a-133">None</span></span>
<span data-ttu-id="9536a-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9536a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9536a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9536a-135">OUTPUTS</span></span>

### <span data-ttu-id="9536a-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="9536a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="9536a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9536a-137">NOTES</span></span>

## <span data-ttu-id="9536a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9536a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9536a-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9536a-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


