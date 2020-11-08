---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062886"
---
# <span data-ttu-id="29c91-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="29c91-101">Get-AzVMSize</span></span>

## <span data-ttu-id="29c91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29c91-102">SYNOPSIS</span></span>
<span data-ttu-id="29c91-103">Pobiera dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="29c91-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="29c91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29c91-104">SYNTAX</span></span>

### <span data-ttu-id="29c91-105">ListVirtualMachineSizeParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29c91-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c91-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="29c91-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c91-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="29c91-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29c91-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29c91-108">DESCRIPTION</span></span>
<span data-ttu-id="29c91-109">Polecenie cmdlet **Get-AzVMSize** Pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29c91-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="29c91-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29c91-110">EXAMPLES</span></span>

### <span data-ttu-id="29c91-111">Przykład 1: pobieranie rozmiaru maszyny wirtualnej dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="29c91-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="29c91-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="29c91-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="29c91-113">Przykład 2: uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="29c91-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="29c91-114">To polecenie pobiera dostępne rozmiary maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="29c91-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="29c91-115">Przykład 3: uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="29c91-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="29c91-116">To polecenie pobiera dostępne rozmiary dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="29c91-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="29c91-117">Możesz zmienić rozmiar maszyny wirtualnej na rozmiar, jaki to polecenie pobiera.</span><span class="sxs-lookup"><span data-stu-id="29c91-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="29c91-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29c91-118">PARAMETERS</span></span>

### <span data-ttu-id="29c91-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="29c91-119">-AvailabilitySetName</span></span>
<span data-ttu-id="29c91-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29c91-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="29c91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c91-121">-DefaultProfile</span></span>
<span data-ttu-id="29c91-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29c91-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c91-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29c91-123">-Location</span></span>
<span data-ttu-id="29c91-124">Określa lokalizację, w której to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29c91-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="29c91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c91-125">-ResourceGroupName</span></span>
<span data-ttu-id="29c91-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29c91-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="29c91-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="29c91-127">-VMName</span></span>
<span data-ttu-id="29c91-128">Określa nazwę maszyny wirtualnej, którą to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej w celu zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="29c91-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="29c91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c91-129">CommonParameters</span></span>
<span data-ttu-id="29c91-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c91-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29c91-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c91-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29c91-132">INPUTS</span></span>

### <span data-ttu-id="29c91-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29c91-133">System.String</span></span>

## <span data-ttu-id="29c91-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29c91-134">OUTPUTS</span></span>

### <span data-ttu-id="29c91-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="29c91-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="29c91-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29c91-136">NOTES</span></span>

## <span data-ttu-id="29c91-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29c91-137">RELATED LINKS</span></span>

[<span data-ttu-id="29c91-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="29c91-138">Get-AzVM</span></span>](./Get-AzVM.md)


