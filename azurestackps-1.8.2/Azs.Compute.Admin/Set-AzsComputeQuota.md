---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055750"
---
# <span data-ttu-id="196e4-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="196e4-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="196e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="196e4-102">SYNOPSIS</span></span>
<span data-ttu-id="196e4-103">Zaktualizuj istniejący przydział obliczeń przy użyciu podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="196e4-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="196e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="196e4-104">SYNTAX</span></span>

### <span data-ttu-id="196e4-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="196e4-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196e4-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="196e4-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="196e4-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="196e4-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196e4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="196e4-108">DESCRIPTION</span></span>
<span data-ttu-id="196e4-109">Zaktualizuj istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="196e4-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="196e4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="196e4-110">EXAMPLES</span></span>

### <span data-ttu-id="196e4-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="196e4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="196e4-112">Zaktualizuj przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="196e4-112">Update a compute quota.</span></span>

## <span data-ttu-id="196e4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="196e4-113">PARAMETERS</span></span>

### <span data-ttu-id="196e4-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="196e4-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="196e4-115">Liczba dozwolonych zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="196e4-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="196e4-116">-CoresCount</span></span>
<span data-ttu-id="196e4-117">Liczba dozwolonych rdzeni.</span><span class="sxs-lookup"><span data-stu-id="196e4-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="196e4-118">-InputObject</span></span>
<span data-ttu-id="196e4-119">Prawdopodobnie zmodyfikowano przydział obliczeń zwróconych przez formularz Get-AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="196e4-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="196e4-120">-Location</span></span>
<span data-ttu-id="196e4-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="196e4-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="196e4-122">-Name</span></span>
<span data-ttu-id="196e4-123">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="196e4-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="196e4-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="196e4-125">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="196e4-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="196e4-126">-ResourceId</span></span>
<span data-ttu-id="196e4-127">Identyfikator przydziału dla ARM.</span><span class="sxs-lookup"><span data-stu-id="196e4-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="196e4-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="196e4-129">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="196e4-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="196e4-130">-VirtualMachineCount</span></span>
<span data-ttu-id="196e4-131">Liczba dozwolonych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="196e4-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="196e4-132">-VmScaleSetCount</span></span>
<span data-ttu-id="196e4-133">Liczba dozwolonych zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="196e4-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e4-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="196e4-134">-Confirm</span></span>
<span data-ttu-id="196e4-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196e4-136">-WhatIf</span></span>
<span data-ttu-id="196e4-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196e4-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="196e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196e4-139">CommonParameters</span></span>
<span data-ttu-id="196e4-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196e4-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196e4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196e4-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="196e4-142">INPUTS</span></span>

## <span data-ttu-id="196e4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="196e4-143">OUTPUTS</span></span>

### <span data-ttu-id="196e4-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="196e4-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="196e4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="196e4-145">NOTES</span></span>

## <span data-ttu-id="196e4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="196e4-146">RELATED LINKS</span></span>

