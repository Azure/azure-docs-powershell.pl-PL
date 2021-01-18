---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501904"
---
# <span data-ttu-id="17732-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="17732-101">Get-AzVMSize</span></span>

## <span data-ttu-id="17732-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17732-102">SYNOPSIS</span></span>
<span data-ttu-id="17732-103">Pobiera dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="17732-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="17732-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17732-104">SYNTAX</span></span>

### <span data-ttu-id="17732-105">ListVirtualMachineSizeParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17732-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17732-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17732-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17732-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="17732-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17732-108">Opis</span><span class="sxs-lookup"><span data-stu-id="17732-108">DESCRIPTION</span></span>
<span data-ttu-id="17732-109">Polecenie cmdlet **Get-AzVMSize** Pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17732-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="17732-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17732-110">EXAMPLES</span></span>

### <span data-ttu-id="17732-111">Przykład 1: pobieranie rozmiaru maszyny wirtualnej dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="17732-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="17732-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="17732-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="17732-113">Przykład 2: uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="17732-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="17732-114">To polecenie pobiera dostępne rozmiary maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="17732-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="17732-115">Przykład 3: uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="17732-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="17732-116">To polecenie pobiera dostępne rozmiary dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="17732-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="17732-117">Możesz zmienić rozmiar maszyny wirtualnej na rozmiar, jaki to polecenie pobiera.</span><span class="sxs-lookup"><span data-stu-id="17732-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="17732-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17732-118">PARAMETERS</span></span>

### <span data-ttu-id="17732-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="17732-119">-AvailabilitySetName</span></span>
<span data-ttu-id="17732-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17732-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="17732-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17732-121">-DefaultProfile</span></span>
<span data-ttu-id="17732-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17732-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17732-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="17732-123">-Location</span></span>
<span data-ttu-id="17732-124">Określa lokalizację, w której to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17732-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="17732-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17732-125">-ResourceGroupName</span></span>
<span data-ttu-id="17732-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17732-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="17732-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="17732-127">-VMName</span></span>
<span data-ttu-id="17732-128">Określa nazwę maszyny wirtualnej, którą to polecenie cmdlet pobiera dostępne rozmiary maszyny wirtualnej w celu zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="17732-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="17732-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17732-129">CommonParameters</span></span>
<span data-ttu-id="17732-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17732-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17732-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17732-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17732-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17732-132">INPUTS</span></span>

### <span data-ttu-id="17732-133">System. String</span><span class="sxs-lookup"><span data-stu-id="17732-133">System.String</span></span>

## <span data-ttu-id="17732-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17732-134">OUTPUTS</span></span>

### <span data-ttu-id="17732-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="17732-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="17732-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17732-136">NOTES</span></span>

## <span data-ttu-id="17732-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17732-137">RELATED LINKS</span></span>

[<span data-ttu-id="17732-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="17732-138">Get-AzVM</span></span>](./Get-AzVM.md)


