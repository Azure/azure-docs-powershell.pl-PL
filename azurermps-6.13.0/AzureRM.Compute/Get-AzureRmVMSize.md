---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 9aca04a3b8bbccccd2950be30f0f13287997bcfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548860"
---
# <span data-ttu-id="384f4-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="384f4-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="384f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="384f4-102">SYNOPSIS</span></span>
<span data-ttu-id="384f4-103">Pobiera dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="384f4-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="384f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="384f4-104">SYNTAX</span></span>

### <span data-ttu-id="384f4-105">ListVirtualMachineSizeParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="384f4-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384f4-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="384f4-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384f4-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="384f4-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="384f4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="384f4-108">DESCRIPTION</span></span>
<span data-ttu-id="384f4-109">Polecenie cmdlet **Get-AzureRmVMSize** Pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="384f4-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="384f4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="384f4-110">EXAMPLES</span></span>

### <span data-ttu-id="384f4-111">Przykład 1: pobieranie rozmiaru maszyny wirtualnej dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="384f4-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="384f4-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="384f4-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="384f4-113">Przykład 2: uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="384f4-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="384f4-114">To polecenie pobiera dostępne rozmiary maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="384f4-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="384f4-115">Przykład 3: uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="384f4-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="384f4-116">To polecenie pobiera dostępne rozmiary dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="384f4-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="384f4-117">Możesz zmienić rozmiar maszyny wirtualnej na rozmiar, jaki to polecenie pobiera.</span><span class="sxs-lookup"><span data-stu-id="384f4-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="384f4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="384f4-118">PARAMETERS</span></span>

### <span data-ttu-id="384f4-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="384f4-119">-AvailabilitySetName</span></span>
<span data-ttu-id="384f4-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="384f4-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="384f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384f4-121">-DefaultProfile</span></span>
<span data-ttu-id="384f4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="384f4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384f4-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="384f4-123">-Location</span></span>
<span data-ttu-id="384f4-124">Określa lokalizację, w której to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="384f4-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="384f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="384f4-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="384f4-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="384f4-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="384f4-127">-VMName</span></span>
<span data-ttu-id="384f4-128">Określa nazwę maszyny wirtualnej, którą to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej w celu zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="384f4-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="384f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384f4-129">CommonParameters</span></span>
<span data-ttu-id="384f4-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384f4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384f4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384f4-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="384f4-132">INPUTS</span></span>

### <span data-ttu-id="384f4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="384f4-133">System.String</span></span>

## <span data-ttu-id="384f4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="384f4-134">OUTPUTS</span></span>

### <span data-ttu-id="384f4-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="384f4-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="384f4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="384f4-136">NOTES</span></span>

## <span data-ttu-id="384f4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="384f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="384f4-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="384f4-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


