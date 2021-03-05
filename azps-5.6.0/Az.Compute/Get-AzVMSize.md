---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: b669d415e88c16f7ddfe532f05bc754561b7ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980954"
---
# <span data-ttu-id="c4f45-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="c4f45-101">Get-AzVMSize</span></span>

## <span data-ttu-id="c4f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4f45-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f45-103">Uzyskuje dostęp do rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c4f45-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="c4f45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c4f45-104">SYNTAX</span></span>

### <span data-ttu-id="c4f45-105">ListVirtualMachineSizeParamSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c4f45-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f45-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c4f45-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f45-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c4f45-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f45-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c4f45-108">DESCRIPTION</span></span>
<span data-ttu-id="c4f45-109">Polecenie **cmdlet Get-AzVMSize** uzyskuje dostęp do rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c4f45-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="c4f45-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c4f45-110">EXAMPLES</span></span>

### <span data-ttu-id="c4f45-111">Przykład 1. Uzyskiwanie rozmiarów maszyn wirtualnych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="c4f45-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="c4f45-112">To polecenie pobiera dostępne rozmiary maszyn wirtualnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c4f45-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="c4f45-113">Przykład 2. Uzyskiwanie rozmiarów zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="c4f45-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="c4f45-114">To polecenie uzyskuje dostęp do rozmiarów maszyn wirtualnych, które można wdrożyć w zestawie dostępności o nazwie AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="c4f45-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="c4f45-115">Przykład 3. Uzyskiwanie rozmiarów istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c4f45-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="c4f45-116">To polecenie jest dostępne dla istniejącej maszyny wirtualnej o nazwie VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="c4f45-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="c4f45-117">Możesz zmienić rozmiar tej maszyny wirtualnej na rozmiary, do których otrzymuje to polecenie.</span><span class="sxs-lookup"><span data-stu-id="c4f45-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="c4f45-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4f45-118">PARAMETERS</span></span>

### <span data-ttu-id="c4f45-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="c4f45-119">-AvailabilitySetName</span></span>
<span data-ttu-id="c4f45-120">Określa nazwę zestawu dostępności, dla którego to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c4f45-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="c4f45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f45-121">-DefaultProfile</span></span>
<span data-ttu-id="c4f45-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4f45-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4f45-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c4f45-123">-Location</span></span>
<span data-ttu-id="c4f45-124">Określa lokalizację, dla której to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c4f45-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="c4f45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f45-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4f45-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4f45-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c4f45-127">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="c4f45-127">-VMName</span></span>
<span data-ttu-id="c4f45-128">Określa nazwę maszyny wirtualnej, dla których to polecenie cmdlet uzyskuje dostępne rozmiary maszyn wirtualnych do zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="c4f45-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="c4f45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f45-129">CommonParameters</span></span>
<span data-ttu-id="c4f45-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f45-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4f45-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f45-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4f45-132">INPUTS</span></span>

### <span data-ttu-id="c4f45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4f45-133">System.String</span></span>

## <span data-ttu-id="c4f45-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4f45-134">OUTPUTS</span></span>

### <span data-ttu-id="c4f45-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="c4f45-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="c4f45-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c4f45-136">NOTES</span></span>

## <span data-ttu-id="c4f45-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4f45-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4f45-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c4f45-138">Get-AzVM</span></span>](./Get-AzVM.md)


