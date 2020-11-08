---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055657"
---
# <span data-ttu-id="7576f-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7576f-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="7576f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7576f-102">SYNOPSIS</span></span>
<span data-ttu-id="7576f-103">Uzyskaj istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="7576f-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="7576f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7576f-104">SYNTAX</span></span>

### <span data-ttu-id="7576f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7576f-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7576f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7576f-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7576f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7576f-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7576f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7576f-108">DESCRIPTION</span></span>
<span data-ttu-id="7576f-109">Uzyskaj istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="7576f-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="7576f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7576f-110">EXAMPLES</span></span>

### <span data-ttu-id="7576f-111">Przykład 1. pobieranie wszystkich przydziałów obliczania</span><span class="sxs-lookup"><span data-stu-id="7576f-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="7576f-112">Uruchom `Get-AzsComputeQuota` bez parametrów, aby uzyskać listę wszystkich przydziałów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="7576f-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="7576f-113">Przykład 2: Uzyskaj przydział obliczeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="7576f-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

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

<span data-ttu-id="7576f-114">Określ nazwę przydziału w wierszu polecenia w celu pobrania określonego przydziału.</span><span class="sxs-lookup"><span data-stu-id="7576f-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="7576f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7576f-115">PARAMETERS</span></span>

### <span data-ttu-id="7576f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7576f-116">-DefaultProfile</span></span>
<span data-ttu-id="7576f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7576f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7576f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7576f-118">-InputObject</span></span>
<span data-ttu-id="7576f-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7576f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7576f-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7576f-120">-Location</span></span>
<span data-ttu-id="7576f-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7576f-121">Location of the resource.</span></span>

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

### <span data-ttu-id="7576f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7576f-122">-Name</span></span>
<span data-ttu-id="7576f-123">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="7576f-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7576f-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7576f-124">-SubscriptionId</span></span>
<span data-ttu-id="7576f-125">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7576f-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7576f-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7576f-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7576f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7576f-127">CommonParameters</span></span>
<span data-ttu-id="7576f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7576f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7576f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7576f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7576f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7576f-130">INPUTS</span></span>

### <span data-ttu-id="7576f-131">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7576f-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="7576f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7576f-132">OUTPUTS</span></span>

### <span data-ttu-id="7576f-133">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="7576f-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="7576f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7576f-134">NOTES</span></span>

<span data-ttu-id="7576f-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7576f-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7576f-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7576f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7576f-137">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7576f-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7576f-138">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="7576f-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="7576f-139">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7576f-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7576f-140">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7576f-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7576f-141">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="7576f-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="7576f-142">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="7576f-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="7576f-143">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="7576f-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="7576f-144">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="7576f-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7576f-145">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="7576f-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="7576f-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7576f-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7576f-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7576f-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7576f-148">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="7576f-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="7576f-149">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7576f-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="7576f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7576f-150">RELATED LINKS</span></span>

