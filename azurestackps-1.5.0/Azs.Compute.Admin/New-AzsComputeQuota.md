---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523485"
---
# <span data-ttu-id="a49e6-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="a49e6-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="a49e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a49e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a49e6-103">Utwórz nowy przydział obliczania, który jest wykorzystywany do ograniczania zasobów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="a49e6-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="a49e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a49e6-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a49e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a49e6-105">DESCRIPTION</span></span>
<span data-ttu-id="a49e6-106">Utwórz nowy przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="a49e6-106">Create a new compute quota.</span></span>

## <span data-ttu-id="a49e6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a49e6-107">EXAMPLES</span></span>

### <span data-ttu-id="a49e6-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a49e6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="a49e6-109">Utwórz nowy przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="a49e6-109">Create a new compute quota.</span></span>

## <span data-ttu-id="a49e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a49e6-110">PARAMETERS</span></span>

### <span data-ttu-id="a49e6-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="a49e6-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="a49e6-112">Liczba dozwolonych zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="a49e6-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="a49e6-113">-CoresCount</span></span>
<span data-ttu-id="a49e6-114">Liczba dozwolonych rdzeni.</span><span class="sxs-lookup"><span data-stu-id="a49e6-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a49e6-115">-Location</span></span>
<span data-ttu-id="a49e6-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a49e6-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a49e6-117">-Name</span></span>
<span data-ttu-id="a49e6-118">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="a49e6-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a49e6-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a49e6-120">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="a49e6-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a49e6-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a49e6-122">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="a49e6-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="a49e6-123">-VirtualMachineCount</span></span>
<span data-ttu-id="a49e6-124">Liczba dozwolonych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="a49e6-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="a49e6-125">-VmScaleSetCount</span></span>
<span data-ttu-id="a49e6-126">Liczba dozwolonych zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="a49e6-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a49e6-127">-Confirm</span></span>
<span data-ttu-id="a49e6-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a49e6-129">-WhatIf</span></span>
<span data-ttu-id="a49e6-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a49e6-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a49e6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49e6-132">CommonParameters</span></span>
<span data-ttu-id="a49e6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49e6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a49e6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49e6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a49e6-135">INPUTS</span></span>

## <span data-ttu-id="a49e6-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a49e6-136">OUTPUTS</span></span>

### <span data-ttu-id="a49e6-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="a49e6-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="a49e6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a49e6-138">NOTES</span></span>

## <span data-ttu-id="a49e6-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a49e6-139">RELATED LINKS</span></span>

