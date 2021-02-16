---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199282"
---
# <span data-ttu-id="0fd12-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="0fd12-101">Get-AzVMSize</span></span>

## <span data-ttu-id="0fd12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd12-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd12-103">Uzyskuje dostęp do rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0fd12-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="0fd12-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0fd12-104">SYNTAX</span></span>

### <span data-ttu-id="0fd12-105">ListVirtualMachineSizeParamSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0fd12-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd12-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0fd12-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd12-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0fd12-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fd12-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0fd12-108">DESCRIPTION</span></span>
<span data-ttu-id="0fd12-109">Polecenie **cmdlet Get-AzVMSize** uzyskuje dostęp do rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0fd12-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="0fd12-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0fd12-110">EXAMPLES</span></span>

### <span data-ttu-id="0fd12-111">Przykład 1. Uzyskiwanie rozmiarów maszyn wirtualnych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="0fd12-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="0fd12-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0fd12-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="0fd12-113">Przykład 2. Uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="0fd12-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="0fd12-114">To polecenie uzyskuje dostęp do rozmiarów maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="0fd12-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="0fd12-115">Przykład 3. Uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0fd12-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="0fd12-116">To polecenie jest dostępne dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="0fd12-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="0fd12-117">Możesz zmienić rozmiar tej maszyny wirtualnej na rozmiary, do których otrzymuje to polecenie.</span><span class="sxs-lookup"><span data-stu-id="0fd12-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="0fd12-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fd12-118">PARAMETERS</span></span>

### <span data-ttu-id="0fd12-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="0fd12-119">-AvailabilitySetName</span></span>
<span data-ttu-id="0fd12-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0fd12-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="0fd12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd12-121">-DefaultProfile</span></span>
<span data-ttu-id="0fd12-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd12-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd12-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0fd12-123">-Location</span></span>
<span data-ttu-id="0fd12-124">Określa lokalizację, dla której to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0fd12-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="0fd12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd12-125">-ResourceGroupName</span></span>
<span data-ttu-id="0fd12-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0fd12-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0fd12-127">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="0fd12-127">-VMName</span></span>
<span data-ttu-id="0fd12-128">Określa nazwę maszyny wirtualnej, dla których to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych do zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="0fd12-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="0fd12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd12-129">CommonParameters</span></span>
<span data-ttu-id="0fd12-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd12-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fd12-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd12-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fd12-132">INPUTS</span></span>

### <span data-ttu-id="0fd12-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0fd12-133">System.String</span></span>

## <span data-ttu-id="0fd12-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fd12-134">OUTPUTS</span></span>

### <span data-ttu-id="0fd12-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="0fd12-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="0fd12-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0fd12-136">NOTES</span></span>

## <span data-ttu-id="0fd12-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fd12-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fd12-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fd12-138">Get-AzVM</span></span>](./Get-AzVM.md)


