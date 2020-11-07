---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894002"
---
# <span data-ttu-id="89ae3-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="89ae3-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="89ae3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89ae3-102">SYNOPSIS</span></span>


## <span data-ttu-id="89ae3-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89ae3-103">SYNTAX</span></span>

### <span data-ttu-id="89ae3-104">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="89ae3-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89ae3-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="89ae3-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89ae3-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="89ae3-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="89ae3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89ae3-107">DESCRIPTION</span></span>
<span data-ttu-id="89ae3-108">Aktualizowanie przydziału obliczeń</span><span class="sxs-lookup"><span data-stu-id="89ae3-108">Update a Compute Quota</span></span>

## <span data-ttu-id="89ae3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89ae3-109">EXAMPLES</span></span>

### <span data-ttu-id="89ae3-110">Przykład 1. Ustawianie właściwości w istniejącym kontyngencie obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="89ae3-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="89ae3-111">Ustaw parametry określone w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="89ae3-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="89ae3-112">Wszystkie parametry, których nie ustawiono, domyślnie mają wartość 0</span><span class="sxs-lookup"><span data-stu-id="89ae3-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="89ae3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89ae3-113">PARAMETERS</span></span>

### <span data-ttu-id="89ae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ae3-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="89ae3-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="89ae3-115">-NewQuota</span></span>
<span data-ttu-id="89ae3-116">Aby skonstruować, zobacz sekcję notatki dla właściwości NEWQUOTA i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="89ae3-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="89ae3-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="89ae3-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="89ae3-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89ae3-118">-Confirm</span></span>
<span data-ttu-id="89ae3-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89ae3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ae3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ae3-120">-WhatIf</span></span>
<span data-ttu-id="89ae3-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89ae3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ae3-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89ae3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ae3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ae3-123">CommonParameters</span></span>
<span data-ttu-id="89ae3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ae3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ae3-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89ae3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ae3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89ae3-126">INPUTS</span></span>

### <span data-ttu-id="89ae3-127">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="89ae3-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="89ae3-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89ae3-128">OUTPUTS</span></span>

### <span data-ttu-id="89ae3-129">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="89ae3-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="89ae3-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89ae3-130">NOTES</span></span>

<span data-ttu-id="89ae3-131">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="89ae3-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89ae3-132">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89ae3-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="89ae3-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="89ae3-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="89ae3-134">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="89ae3-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="89ae3-135">`[AvailabilitySetCount <Int32?>]`: Maksymalna dozwolona liczba zestawów dostępności.</span><span class="sxs-lookup"><span data-stu-id="89ae3-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="89ae3-136">`[CoresLimit <Int32?>]`: Maksymalna dozwolona liczba rdzeni.</span><span class="sxs-lookup"><span data-stu-id="89ae3-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="89ae3-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maksymalna dozwolona liczba zarządzanych dysków i migawek typu Premium.</span><span class="sxs-lookup"><span data-stu-id="89ae3-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="89ae3-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maksymalna liczba zarządzanych dysków i migawek typu Standard jest dozwolona.</span><span class="sxs-lookup"><span data-stu-id="89ae3-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="89ae3-139">`[VMScaleSetCount <Int32?>]`: Dozwolone jest określenie maksymalnej liczby zestawów skali.</span><span class="sxs-lookup"><span data-stu-id="89ae3-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="89ae3-140">`[VirtualMachineCount <Int32?>]`: Maksymalna dozwolona liczba maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="89ae3-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="89ae3-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89ae3-141">RELATED LINKS</span></span>

