---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054323"
---
# <span data-ttu-id="ef272-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ef272-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ef272-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef272-102">SYNOPSIS</span></span>
<span data-ttu-id="ef272-103">Anulowanie zadania migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="ef272-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="ef272-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef272-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef272-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef272-105">DESCRIPTION</span></span>
<span data-ttu-id="ef272-106">Anulowanie zadania migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="ef272-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="ef272-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef272-107">EXAMPLES</span></span>

### <span data-ttu-id="ef272-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="ef272-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="ef272-109">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="ef272-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="ef272-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef272-110">PARAMETERS</span></span>

### <span data-ttu-id="ef272-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef272-111">-DefaultProfile</span></span>
<span data-ttu-id="ef272-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef272-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef272-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ef272-113">-Location</span></span>
<span data-ttu-id="ef272-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef272-114">Location of the resource.</span></span>

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

### <span data-ttu-id="ef272-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef272-115">-Name</span></span>
<span data-ttu-id="ef272-116">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="ef272-116">The migration job guid name.</span></span>

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

### <span data-ttu-id="ef272-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ef272-117">-SubscriptionId</span></span>
<span data-ttu-id="ef272-118">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef272-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef272-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ef272-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef272-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef272-120">-Confirm</span></span>
<span data-ttu-id="ef272-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef272-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef272-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef272-122">-WhatIf</span></span>
<span data-ttu-id="ef272-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef272-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef272-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef272-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef272-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef272-125">CommonParameters</span></span>
<span data-ttu-id="ef272-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef272-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef272-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef272-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef272-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef272-128">INPUTS</span></span>

## <span data-ttu-id="ef272-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef272-129">OUTPUTS</span></span>

### <span data-ttu-id="ef272-130">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ef272-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="ef272-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef272-131">NOTES</span></span>

## <span data-ttu-id="ef272-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef272-132">RELATED LINKS</span></span>

