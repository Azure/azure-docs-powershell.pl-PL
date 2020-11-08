---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054308"
---
# <span data-ttu-id="ffddf-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ffddf-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="ffddf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffddf-102">SYNOPSIS</span></span>
<span data-ttu-id="ffddf-103">Tworzy nowy obraz platformy z danym wydawcą, ofertą, wersjami SKU i wersją.</span><span class="sxs-lookup"><span data-stu-id="ffddf-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="ffddf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffddf-104">SYNTAX</span></span>

### <span data-ttu-id="ffddf-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ffddf-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ffddf-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="ffddf-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ffddf-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ffddf-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ffddf-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ffddf-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffddf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ffddf-109">DESCRIPTION</span></span>
<span data-ttu-id="ffddf-110">Tworzy nowy obraz platformy z danym wydawcą, ofertą, wersjami SKU i wersją.</span><span class="sxs-lookup"><span data-stu-id="ffddf-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="ffddf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffddf-111">EXAMPLES</span></span>

### <span data-ttu-id="ffddf-112">Przykład 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ffddf-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="ffddf-113">Dodawanie obrazu platformy z magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="ffddf-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="ffddf-114">Użyj SasUri, aby określić lokalizację PlatformImage, lub użyj publicznie dostępnego adresu URL.</span><span class="sxs-lookup"><span data-stu-id="ffddf-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="ffddf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffddf-115">PARAMETERS</span></span>

### <span data-ttu-id="ffddf-116">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="ffddf-116">Exception.Message</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="ffddf-117">-BillingPartNumber</span></span>
<span data-ttu-id="ffddf-118">Numer części jest wykorzystywany do naliczania kosztów oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="ffddf-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-119">-Datadyski</span><span class="sxs-lookup"><span data-stu-id="ffddf-119">-DataDisks</span></span>
<span data-ttu-id="ffddf-120">Dyski danych używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="ffddf-121">Aby skonstruować, zobacz sekcję Uwagi dla właściwości dysków datadysks i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ffddf-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffddf-122">-DefaultProfile</span></span>
<span data-ttu-id="ffddf-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffddf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffddf-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ffddf-124">-InputObject</span></span>
<span data-ttu-id="ffddf-125">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ffddf-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ffddf-126">-Location</span></span>
<span data-ttu-id="ffddf-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffddf-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="ffddf-128">-NewImage</span></span>
<span data-ttu-id="ffddf-129">Parametry używane do tworzenia nowego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="ffddf-130">Aby skonstruować, zobacz sekcję notatki dla właściwości NEWIMAGE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ffddf-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ffddf-131">-NoWait</span></span>
<span data-ttu-id="ffddf-132">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ffddf-132">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-133">-Offer</span><span class="sxs-lookup"><span data-stu-id="ffddf-133">-Offer</span></span>
<span data-ttu-id="ffddf-134">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="ffddf-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="ffddf-135">-OsType</span></span>
<span data-ttu-id="ffddf-136">Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ffddf-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="ffddf-137">-OsUri</span></span>
<span data-ttu-id="ffddf-138">Lokalizacja dysku.</span><span class="sxs-lookup"><span data-stu-id="ffddf-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="ffddf-139">-ProvisioningState</span></span>
<span data-ttu-id="ffddf-140">Stan inicjowania obsługi obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-141">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="ffddf-141">-Publisher</span></span>
<span data-ttu-id="ffddf-142">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="ffddf-143">-Sku</span></span>
<span data-ttu-id="ffddf-144">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="ffddf-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ffddf-145">-SubscriptionId</span></span>
<span data-ttu-id="ffddf-146">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ffddf-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ffddf-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ffddf-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-148">-Version</span><span class="sxs-lookup"><span data-stu-id="ffddf-148">-Version</span></span>
<span data-ttu-id="ffddf-149">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffddf-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffddf-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffddf-150">-Confirm</span></span>
<span data-ttu-id="ffddf-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffddf-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffddf-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffddf-152">-WhatIf</span></span>
<span data-ttu-id="ffddf-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffddf-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffddf-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffddf-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="ffddf-155">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="ffddf-155">Exception.Message</span></span>

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

### <span data-ttu-id="ffddf-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffddf-156">CommonParameters</span></span>
<span data-ttu-id="ffddf-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffddf-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffddf-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffddf-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffddf-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffddf-159">INPUTS</span></span>

### <span data-ttu-id="ffddf-160">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="ffddf-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="ffddf-161">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ffddf-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="ffddf-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffddf-162">OUTPUTS</span></span>

### <span data-ttu-id="ffddf-163">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ffddf-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="ffddf-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffddf-164">NOTES</span></span>

<span data-ttu-id="ffddf-165">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ffddf-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ffddf-166">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ffddf-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ffddf-167">Datadysks <IDataDisk [] >: dyski z danymi używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="ffddf-168">`[Lun <Int32?>]`: Numer jednostki logicznej.</span><span class="sxs-lookup"><span data-stu-id="ffddf-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="ffddf-169">`[Uri <String>]`: Lokalizacja szablonu dysku.</span><span class="sxs-lookup"><span data-stu-id="ffddf-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="ffddf-170">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ffddf-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ffddf-171">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="ffddf-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="ffddf-172">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ffddf-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ffddf-173">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffddf-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ffddf-174">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="ffddf-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="ffddf-175">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="ffddf-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="ffddf-176">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="ffddf-177">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="ffddf-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="ffddf-178">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="ffddf-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="ffddf-179">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ffddf-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ffddf-180">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ffddf-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ffddf-181">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ffddf-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="ffddf-182">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffddf-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="ffddf-183">NEWIMAGE <IPlatformImageParameters> : parametry używane do tworzenia nowego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="ffddf-184">`[DataDisk <IDataDisk[]>]`: Dyski danych używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="ffddf-185">`[Lun <Int32?>]`: Numer jednostki logicznej.</span><span class="sxs-lookup"><span data-stu-id="ffddf-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="ffddf-186">`[Uri <String>]`: Lokalizacja szablonu dysku.</span><span class="sxs-lookup"><span data-stu-id="ffddf-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="ffddf-187">`[DetailBillingPartNumber <String>]`: Numer części jest wykorzystywany do naliczania kosztów oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="ffddf-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="ffddf-188">`[OSDiskOstype <OSType?>]`: Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ffddf-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="ffddf-189">`[OSDiskUri <String>]`: Lokalizacja dysku.</span><span class="sxs-lookup"><span data-stu-id="ffddf-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="ffddf-190">`[ProvisioningState <ProvisioningState?>]`: Stan inicjowania obsługi obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="ffddf-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="ffddf-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffddf-191">RELATED LINKS</span></span>

