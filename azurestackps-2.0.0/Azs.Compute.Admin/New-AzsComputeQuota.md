---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894022"
---
# <span data-ttu-id="5223e-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5223e-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="5223e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5223e-102">SYNOPSIS</span></span>
<span data-ttu-id="5223e-103">Umożliwia utworzenie lub zaktualizowanie przydziału obliczanego przy użyciu podanych parametrów przydziałów.</span><span class="sxs-lookup"><span data-stu-id="5223e-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="5223e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5223e-104">SYNTAX</span></span>

### <span data-ttu-id="5223e-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5223e-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5223e-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="5223e-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5223e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5223e-107">DESCRIPTION</span></span>
<span data-ttu-id="5223e-108">Umożliwia utworzenie lub zaktualizowanie przydziału obliczanego przy użyciu podanych parametrów przydziałów.</span><span class="sxs-lookup"><span data-stu-id="5223e-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="5223e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5223e-109">EXAMPLES</span></span>

### <span data-ttu-id="5223e-110">Przykład 1. Tworzenie przydziału obliczanego z parametrami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="5223e-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="5223e-111">Wszystkie parametry, które nie zostały określone, zostaną ustawione na ich domyślny parametr, pokazane powyżej.</span><span class="sxs-lookup"><span data-stu-id="5223e-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="5223e-112">Przykład 2: Tworzenie przydziału obliczanego z parametrami niestandardowymi</span><span class="sxs-lookup"><span data-stu-id="5223e-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="5223e-113">Dostosowywanie przydziału za pomocą parametrów.</span><span class="sxs-lookup"><span data-stu-id="5223e-113">Customize Quota with parameters.</span></span> <span data-ttu-id="5223e-114">Wszystkie parametry, które nie zostały określone, będą miały wartość domyślną.</span><span class="sxs-lookup"><span data-stu-id="5223e-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="5223e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5223e-115">PARAMETERS</span></span>

### <span data-ttu-id="5223e-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="5223e-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="5223e-117">Maksymalna dozwolona liczba zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="5223e-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="5223e-118">-CoresCount</span></span>
<span data-ttu-id="5223e-119">Maksymalna dozwolona liczba rdzeni.</span><span class="sxs-lookup"><span data-stu-id="5223e-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5223e-120">-DefaultProfile</span></span>
<span data-ttu-id="5223e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5223e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5223e-122">-Location</span></span>
<span data-ttu-id="5223e-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5223e-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="5223e-124">-Location1</span></span>
<span data-ttu-id="5223e-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5223e-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5223e-126">-Name</span></span>
<span data-ttu-id="5223e-127">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="5223e-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="5223e-128">-NewQuota</span></span>
<span data-ttu-id="5223e-129">Przechowuje informacje o przydziałach obliczeniowych używane do kontroli alokacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="5223e-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="5223e-130">Aby skonstruować, zobacz sekcję notatki dla właściwości NEWQUOTA i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="5223e-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="5223e-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="5223e-132">Maksymalna dozwolona liczba zarządzanych dysków i migawek typu Premium.</span><span class="sxs-lookup"><span data-stu-id="5223e-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="5223e-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="5223e-134">Maksymalna liczba zarządzanych dysków i migawek dozwolone typy Standard.</span><span class="sxs-lookup"><span data-stu-id="5223e-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5223e-135">-SubscriptionId</span></span>
<span data-ttu-id="5223e-136">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5223e-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5223e-137">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5223e-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="5223e-138">-VirtualMachineCount</span></span>
<span data-ttu-id="5223e-139">Maksymalna dozwolona liczba maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5223e-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="5223e-140">-VMScaleSetCount</span></span>
<span data-ttu-id="5223e-141">Maksymalna dozwolona liczba zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="5223e-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5223e-142">-Confirm</span></span>
<span data-ttu-id="5223e-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5223e-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5223e-144">-WhatIf</span></span>
<span data-ttu-id="5223e-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5223e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5223e-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5223e-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5223e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5223e-147">CommonParameters</span></span>
<span data-ttu-id="5223e-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5223e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5223e-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5223e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5223e-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5223e-150">INPUTS</span></span>

### <span data-ttu-id="5223e-151">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="5223e-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="5223e-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5223e-152">OUTPUTS</span></span>

### <span data-ttu-id="5223e-153">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="5223e-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="5223e-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5223e-154">NOTES</span></span>

<span data-ttu-id="5223e-155">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5223e-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5223e-156">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5223e-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5223e-157">NEWQUOTA <IQuota> : przechowuje informacje o przydziałach obliczeniowych używane do kontroli alokacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="5223e-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="5223e-158">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5223e-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5223e-159">`[AvailabilitySetCount <Int32?>]`: Maksymalna dozwolona liczba zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="5223e-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="5223e-160">`[CoresLimit <Int32?>]`: Maksymalna dozwolona liczba rdzeni.</span><span class="sxs-lookup"><span data-stu-id="5223e-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="5223e-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maksymalna dozwolona liczba zarządzanych dysków i migawek typu Premium.</span><span class="sxs-lookup"><span data-stu-id="5223e-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="5223e-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maksymalna liczba zarządzanych dysków i migawek typu Standard jest dozwolona.</span><span class="sxs-lookup"><span data-stu-id="5223e-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="5223e-163">`[VMScaleSetCount <Int32?>]`: Dozwolone jest określenie maksymalnej liczby zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="5223e-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="5223e-164">`[VirtualMachineCount <Int32?>]`: Maksymalna dozwolona liczba maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5223e-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="5223e-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5223e-165">RELATED LINKS</span></span>

