---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055697"
---
# <span data-ttu-id="9ad10-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="9ad10-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="9ad10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ad10-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad10-103">Zwraca żądanego wydawcy dopasowania obrazu rozszerzenia maszyny wirtualnej. typ, wersja.</span><span class="sxs-lookup"><span data-stu-id="9ad10-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="9ad10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ad10-104">SYNTAX</span></span>

### <span data-ttu-id="9ad10-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9ad10-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad10-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9ad10-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ad10-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ad10-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9ad10-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ad10-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad10-109">Zwraca żądanego wydawcy dopasowania obrazu rozszerzenia maszyny wirtualnej. typ, wersja.</span><span class="sxs-lookup"><span data-stu-id="9ad10-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="9ad10-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ad10-110">EXAMPLES</span></span>

### <span data-ttu-id="9ad10-111">Przykład 1: pobieranie wszystkich rozszerzeń maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9ad10-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="9ad10-112">Zapoznaj się z listą wszystkich VMExtensions, pozostawiając wszystkie parametry puste.</span><span class="sxs-lookup"><span data-stu-id="9ad10-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="9ad10-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ad10-113">PARAMETERS</span></span>

### <span data-ttu-id="9ad10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad10-114">-DefaultProfile</span></span>
<span data-ttu-id="9ad10-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad10-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad10-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ad10-116">-InputObject</span></span>
<span data-ttu-id="9ad10-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9ad10-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ad10-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9ad10-118">-Location</span></span>
<span data-ttu-id="9ad10-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ad10-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9ad10-120">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="9ad10-120">-Publisher</span></span>
<span data-ttu-id="9ad10-121">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="9ad10-121">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ad10-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9ad10-122">-SubscriptionId</span></span>
<span data-ttu-id="9ad10-123">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad10-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ad10-124">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9ad10-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9ad10-125">-Type</span><span class="sxs-lookup"><span data-stu-id="9ad10-125">-Type</span></span>
<span data-ttu-id="9ad10-126">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9ad10-126">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ad10-127">-Version</span><span class="sxs-lookup"><span data-stu-id="9ad10-127">-Version</span></span>
<span data-ttu-id="9ad10-128">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ad10-128">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ad10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad10-129">CommonParameters</span></span>
<span data-ttu-id="9ad10-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad10-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ad10-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad10-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ad10-132">INPUTS</span></span>

### <span data-ttu-id="9ad10-133">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9ad10-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="9ad10-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ad10-134">OUTPUTS</span></span>

### <span data-ttu-id="9ad10-135">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="9ad10-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="9ad10-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ad10-136">NOTES</span></span>

<span data-ttu-id="9ad10-137">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9ad10-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ad10-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ad10-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9ad10-139">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9ad10-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ad10-140">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="9ad10-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="9ad10-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9ad10-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ad10-142">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ad10-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9ad10-143">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="9ad10-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="9ad10-144">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="9ad10-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="9ad10-145">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="9ad10-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="9ad10-146">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="9ad10-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9ad10-147">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="9ad10-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="9ad10-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad10-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9ad10-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9ad10-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9ad10-150">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9ad10-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="9ad10-151">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ad10-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="9ad10-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ad10-152">RELATED LINKS</span></span>

