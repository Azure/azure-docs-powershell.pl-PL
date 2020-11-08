---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054241"
---
# <span data-ttu-id="b0e86-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b0e86-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="b0e86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0e86-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e86-103">Zwraca żądane zadanie migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="b0e86-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b0e86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0e86-104">SYNTAX</span></span>

### <span data-ttu-id="b0e86-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b0e86-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0e86-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b0e86-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0e86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0e86-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b0e86-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0e86-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e86-109">Zwraca żądane zadanie migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="b0e86-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b0e86-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0e86-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e86-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="b0e86-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="b0e86-112">Zwraca listę zadań zarządzanych migracji dysków w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="b0e86-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="b0e86-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="b0e86-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="b0e86-114">Uzyskiwanie określonego zadania dotyczącego migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="b0e86-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="b0e86-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0e86-115">PARAMETERS</span></span>

### <span data-ttu-id="b0e86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e86-116">-DefaultProfile</span></span>
<span data-ttu-id="b0e86-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e86-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0e86-118">-InputObject</span></span>
<span data-ttu-id="b0e86-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b0e86-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b0e86-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b0e86-120">-Location</span></span>
<span data-ttu-id="b0e86-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b0e86-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0e86-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0e86-122">-Name</span></span>
<span data-ttu-id="b0e86-123">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="b0e86-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0e86-124">-Status</span><span class="sxs-lookup"><span data-stu-id="b0e86-124">-Status</span></span>
<span data-ttu-id="b0e86-125">Parametry stanu zadania migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="b0e86-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0e86-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b0e86-126">-SubscriptionId</span></span>
<span data-ttu-id="b0e86-127">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e86-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0e86-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b0e86-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0e86-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e86-129">CommonParameters</span></span>
<span data-ttu-id="b0e86-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e86-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e86-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0e86-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e86-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0e86-132">INPUTS</span></span>

### <span data-ttu-id="b0e86-133">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b0e86-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="b0e86-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0e86-134">OUTPUTS</span></span>

### <span data-ttu-id="b0e86-135">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b0e86-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="b0e86-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0e86-136">NOTES</span></span>

<span data-ttu-id="b0e86-137">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0e86-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0e86-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0e86-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b0e86-139">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b0e86-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0e86-140">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="b0e86-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="b0e86-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b0e86-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0e86-142">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b0e86-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b0e86-143">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="b0e86-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="b0e86-144">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="b0e86-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b0e86-145">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="b0e86-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="b0e86-146">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="b0e86-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b0e86-147">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="b0e86-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="b0e86-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e86-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0e86-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b0e86-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0e86-150">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b0e86-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="b0e86-151">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b0e86-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="b0e86-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0e86-152">RELATED LINKS</span></span>

