---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894017"
---
# <span data-ttu-id="ecd0c-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ecd0c-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ecd0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecd0c-102">SYNOPSIS</span></span>


## <span data-ttu-id="ecd0c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecd0c-103">SYNTAX</span></span>

### <span data-ttu-id="ecd0c-104">Wolumin (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ecd0c-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd0c-105">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="ecd0c-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecd0c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="ecd0c-106">DESCRIPTION</span></span>


## <span data-ttu-id="ecd0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecd0c-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd0c-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="ecd0c-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="ecd0c-109">Utwórz zadanie migracji dysku w celu migrowania dysków do docelowej jednostki skali i woluminu.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="ecd0c-110">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="ecd0c-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="ecd0c-111">Utwórz zadanie migracji dysku w celu migrowania dysków do udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="ecd0c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecd0c-112">PARAMETERS</span></span>

### <span data-ttu-id="ecd0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd0c-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="ecd0c-114">-Dyski</span><span class="sxs-lookup"><span data-stu-id="ecd0c-114">-Disks</span></span>
<span data-ttu-id="ecd0c-115">Aby skonstruować, zobacz sekcję Uwagi dotyczącej właściwości dysków i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ecd0c-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ecd0c-116">-Location</span></span>


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

### <span data-ttu-id="ecd0c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ecd0c-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ecd0c-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ecd0c-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="ecd0c-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ecd0c-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ecd0c-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="ecd0c-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ecd0c-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="ecd0c-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ecd0c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecd0c-122">-Confirm</span></span>
<span data-ttu-id="ecd0c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd0c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd0c-124">-WhatIf</span></span>
<span data-ttu-id="ecd0c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd0c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd0c-127">CommonParameters</span></span>
<span data-ttu-id="ecd0c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd0c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecd0c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd0c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd0c-130">INPUTS</span></span>

### <span data-ttu-id="ecd0c-131">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180730Preview. IDisk []</span><span class="sxs-lookup"><span data-stu-id="ecd0c-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="ecd0c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecd0c-132">OUTPUTS</span></span>

### <span data-ttu-id="ecd0c-133">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ecd0c-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="ecd0c-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ecd0c-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ecd0c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecd0c-135">NOTES</span></span>

<span data-ttu-id="ecd0c-136">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecd0c-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ecd0c-138">DYSKI <IDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="ecd0c-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="ecd0c-139">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ecd0c-140">`[DiskId <String>]`: Identyfikator dysku.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="ecd0c-141">`[SharePath <String>]`: Ścieżka udziału dysku.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="ecd0c-142">`[Status <DiskState?>]`: Stan dysku.</span><span class="sxs-lookup"><span data-stu-id="ecd0c-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="ecd0c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecd0c-143">RELATED LINKS</span></span>

