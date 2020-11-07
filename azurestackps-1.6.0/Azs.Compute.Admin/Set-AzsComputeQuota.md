---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4caf955c25cd29c9cc9c09f1182454ee3a4d56df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522966"
---
# <span data-ttu-id="aab2c-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="aab2c-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="aab2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aab2c-102">SYNOPSIS</span></span>
<span data-ttu-id="aab2c-103">Zaktualizuj istniejący przydział obliczeń przy użyciu podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="aab2c-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="aab2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aab2c-104">SYNTAX</span></span>

### <span data-ttu-id="aab2c-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="aab2c-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab2c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="aab2c-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aab2c-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="aab2c-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab2c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aab2c-108">DESCRIPTION</span></span>
<span data-ttu-id="aab2c-109">Zaktualizuj istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="aab2c-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="aab2c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aab2c-110">EXAMPLES</span></span>

### <span data-ttu-id="aab2c-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aab2c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="aab2c-112">Zaktualizuj przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="aab2c-112">Update a compute quota.</span></span>

## <span data-ttu-id="aab2c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aab2c-113">PARAMETERS</span></span>

### <span data-ttu-id="aab2c-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="aab2c-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="aab2c-115">Liczba dozwolonych zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="aab2c-115">Number of availability sets allowed.</span></span>

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

### <span data-ttu-id="aab2c-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="aab2c-116">-CoresCount</span></span>
<span data-ttu-id="aab2c-117">Liczba dozwolonych rdzeni.</span><span class="sxs-lookup"><span data-stu-id="aab2c-117">Number of cores allowed.</span></span>

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

### <span data-ttu-id="aab2c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aab2c-118">-InputObject</span></span>
<span data-ttu-id="aab2c-119">Prawdopodobnie zmodyfikowano przydział obliczeń zwróconych przez formularz Get-AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="aab2c-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

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

### <span data-ttu-id="aab2c-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aab2c-120">-Location</span></span>
<span data-ttu-id="aab2c-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="aab2c-121">Location of the resource.</span></span>

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

### <span data-ttu-id="aab2c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aab2c-122">-Name</span></span>
<span data-ttu-id="aab2c-123">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="aab2c-123">The name of the quota.</span></span>

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

### <span data-ttu-id="aab2c-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="aab2c-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="aab2c-125">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="aab2c-125">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="aab2c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aab2c-126">-ResourceId</span></span>
<span data-ttu-id="aab2c-127">Identyfikator przydziału dla ARM.</span><span class="sxs-lookup"><span data-stu-id="aab2c-127">The ARM compute quota id.</span></span>

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

### <span data-ttu-id="aab2c-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="aab2c-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="aab2c-129">Rozmiar dozwolonych standardowych dysków zarządzanych i migawek.</span><span class="sxs-lookup"><span data-stu-id="aab2c-129">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="aab2c-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="aab2c-130">-VirtualMachineCount</span></span>
<span data-ttu-id="aab2c-131">Liczba dozwolonych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="aab2c-131">Number of virtual machines allowed.</span></span>

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

### <span data-ttu-id="aab2c-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="aab2c-132">-VmScaleSetCount</span></span>
<span data-ttu-id="aab2c-133">Liczba dozwolonych zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="aab2c-133">Number of scale sets allowed.</span></span>

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

### <span data-ttu-id="aab2c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aab2c-134">-Confirm</span></span>
<span data-ttu-id="aab2c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aab2c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab2c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab2c-136">-WhatIf</span></span>
<span data-ttu-id="aab2c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aab2c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab2c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aab2c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab2c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab2c-139">CommonParameters</span></span>
<span data-ttu-id="aab2c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab2c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab2c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab2c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab2c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aab2c-142">INPUTS</span></span>

## <span data-ttu-id="aab2c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aab2c-143">OUTPUTS</span></span>

### <span data-ttu-id="aab2c-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="aab2c-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="aab2c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aab2c-145">NOTES</span></span>

## <span data-ttu-id="aab2c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aab2c-146">RELATED LINKS</span></span>
