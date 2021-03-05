---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: e38402359a3bccebc33d92211ed10d8032a0dd4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977098"
---
# <span data-ttu-id="225e7-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="225e7-101">New-AzImportExport</span></span>

## <span data-ttu-id="225e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="225e7-102">SYNOPSIS</span></span>
<span data-ttu-id="225e7-103">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="225e7-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="225e7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="225e7-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="225e7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="225e7-105">DESCRIPTION</span></span>
<span data-ttu-id="225e7-106">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="225e7-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="225e7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="225e7-107">EXAMPLES</span></span>

### <span data-ttu-id="225e7-108">Przykład 1. Tworzenie nowego zadania ImportExport</span><span class="sxs-lookup"><span data-stu-id="225e7-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="225e7-109">Te polecenia cmdlet tworzą nowe zadanie ImportExport.</span><span class="sxs-lookup"><span data-stu-id="225e7-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="225e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="225e7-110">PARAMETERS</span></span>

### <span data-ttu-id="225e7-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="225e7-111">-AcceptLanguage</span></span>
<span data-ttu-id="225e7-112">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="225e7-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="225e7-113">-BackupDriveManifest</span></span>
<span data-ttu-id="225e7-114">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="225e7-114">Default value is false.</span></span>
<span data-ttu-id="225e7-115">Wskazuje, czy pliki manifestu na dyskach powinny zostać skopiowane w celu zablokowania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="225e7-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="225e7-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="225e7-116">-BlobListBlobPath</span></span>
<span data-ttu-id="225e7-117">Zbiór ciągów ścieżki obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="225e7-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="225e7-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="225e7-119">Zbiór ciągów prefiksów obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="225e7-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="225e7-120">-CancelRequested</span></span>
<span data-ttu-id="225e7-121">Wskazuje, czy żądanie anulowania zadania zostało przesłane.</span><span class="sxs-lookup"><span data-stu-id="225e7-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="225e7-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="225e7-122">-ClientTenantId</span></span>
<span data-ttu-id="225e7-123">Identyfikator dzierżawy klienta, który złożyć żądanie.</span><span class="sxs-lookup"><span data-stu-id="225e7-123">The tenant ID of the client making the request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225e7-124">-DefaultProfile</span></span>
<span data-ttu-id="225e7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="225e7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225e7-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="225e7-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="225e7-127">Nazwa operatora używanego do wysyłki dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="225e7-127">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="225e7-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="225e7-129">Liczba dysków dołączonych do pakietu.</span><span class="sxs-lookup"><span data-stu-id="225e7-129">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="225e7-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="225e7-131">Data wysyłki paczki.</span><span class="sxs-lookup"><span data-stu-id="225e7-131">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="225e7-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="225e7-133">Numer śledzenia przesyłki.</span><span class="sxs-lookup"><span data-stu-id="225e7-133">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-134">- DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="225e7-134">-DiagnosticsPath</span></span>
<span data-ttu-id="225e7-135">Katalog wirtualnych obiektów blob, w którym będą przechowywane dzienniki kopii i kopie zapasowe plików manifestu dysku (jeśli ta funkcja jest włączona).</span><span class="sxs-lookup"><span data-stu-id="225e7-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="225e7-136">-DriveList</span></span>
<span data-ttu-id="225e7-137">Lista maksymalnie dziesięciu dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="225e7-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="225e7-138">Lista dysków jest wymaganym elementem dla zadania importu. nie jest określony dla zadań eksportu.</span><span class="sxs-lookup"><span data-stu-id="225e7-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="225e7-139">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach listy dysków i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="225e7-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="225e7-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="225e7-141">Względny URI do bloku obiektu blob zawierającego listę ścieżek obiektów blob lub prefiksów ścieżek obiektów blob zdefiniowanych powyżej, począwszy od nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="225e7-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="225e7-142">Jeśli obiekt blob znajduje się w kontenerze głównym, musi zaczynać się od $root.</span><span class="sxs-lookup"><span data-stu-id="225e7-142">If the blob is in root container, the URI must begin with $root.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="225e7-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="225e7-144">Ścieżka obiektu blob, która wskazuje blokowy obiekt blob zawierający listę nazw obiektów blob, które nie zostały wyeksportowane z powodu niewystarczającej ilości miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="225e7-145">Jeśli wszystkie obiekty blob zostały pomyślnie wyeksportowane, ten element nie jest uwzględniany w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="225e7-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-146">- JobType</span><span class="sxs-lookup"><span data-stu-id="225e7-146">-JobType</span></span>
<span data-ttu-id="225e7-147">Typ zadania</span><span class="sxs-lookup"><span data-stu-id="225e7-147">The type of job</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="225e7-148">-Location</span></span>
<span data-ttu-id="225e7-149">Określa obsługiwaną lokalizację platformy Azure, w której należy utworzyć zadanie.</span><span class="sxs-lookup"><span data-stu-id="225e7-149">Specifies the supported Azure location where the job should be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="225e7-150">-LogLevel</span></span>
<span data-ttu-id="225e7-151">Wartość domyślna to Błąd.</span><span class="sxs-lookup"><span data-stu-id="225e7-151">Default value is Error.</span></span>
<span data-ttu-id="225e7-152">Wskazuje, czy funkcja rejestrowania błędów, czy rejestrowania szczegółowego zostanie włączona.</span><span class="sxs-lookup"><span data-stu-id="225e7-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-153">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="225e7-153">-Name</span></span>
<span data-ttu-id="225e7-154">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="225e7-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="225e7-155">-PercentComplete</span></span>
<span data-ttu-id="225e7-156">Ogólna wartość procentowa ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="225e7-156">Overall percentage completed for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="225e7-157">-ProvisioningState</span></span>
<span data-ttu-id="225e7-158">Określa stan inicjowania obsługi administracyjnej zadania.</span><span class="sxs-lookup"><span data-stu-id="225e7-158">Specifies the provisioning state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225e7-159">-ResourceGroupName</span></span>
<span data-ttu-id="225e7-160">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="225e7-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="225e7-161">-ReturnAddressCity</span></span>
<span data-ttu-id="225e7-162">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-162">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="225e7-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="225e7-164">Kraj lub region, z których należy korzystać podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-164">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="225e7-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="225e7-166">Adres e-mail adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-166">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="225e7-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="225e7-168">Numer telefonu odbiorcy zwracanych dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-168">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="225e7-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="225e7-170">Kod pocztowy do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-170">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="225e7-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="225e7-172">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="225e7-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="225e7-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="225e7-174">Stan lub prowincja do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-174">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="225e7-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="225e7-176">Pierwszy wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-176">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="225e7-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="225e7-178">Drugi wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-178">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="225e7-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="225e7-180">Nazwa operatora używanego do wysyłki dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="225e7-180">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="225e7-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="225e7-182">Liczba dysków dołączonych do pakietu.</span><span class="sxs-lookup"><span data-stu-id="225e7-182">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="225e7-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="225e7-184">Data wysyłki paczki.</span><span class="sxs-lookup"><span data-stu-id="225e7-184">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="225e7-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="225e7-186">Numer śledzenia przesyłki.</span><span class="sxs-lookup"><span data-stu-id="225e7-186">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="225e7-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="225e7-188">Numer konta klienta u operatora.</span><span class="sxs-lookup"><span data-stu-id="225e7-188">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="225e7-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="225e7-190">Imię i nazwisko operatora.</span><span class="sxs-lookup"><span data-stu-id="225e7-190">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="225e7-191">-ShippingInformationCity</span></span>
<span data-ttu-id="225e7-192">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-192">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="225e7-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="225e7-194">Kraj lub region, z których należy korzystać podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-194">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="225e7-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="225e7-196">Numer telefonu odbiorcy zwracanych dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-196">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="225e7-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="225e7-198">Kod pocztowy do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-198">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="225e7-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="225e7-200">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="225e7-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="225e7-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="225e7-202">Stan lub prowincja do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-202">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="225e7-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="225e7-204">Pierwszy wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-204">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="225e7-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="225e7-206">Drugi wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="225e7-206">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-207">— województwo</span><span class="sxs-lookup"><span data-stu-id="225e7-207">-State</span></span>
<span data-ttu-id="225e7-208">Bieżący stan zadania.</span><span class="sxs-lookup"><span data-stu-id="225e7-208">Current state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-209">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="225e7-209">-StorageAccountId</span></span>
<span data-ttu-id="225e7-210">Identyfikator zasobu konta magazynu, z którego będą importowane lub eksportowane dane.</span><span class="sxs-lookup"><span data-stu-id="225e7-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-211">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="225e7-211">-SubscriptionId</span></span>
<span data-ttu-id="225e7-212">Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="225e7-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="225e7-213">— Tag</span><span class="sxs-lookup"><span data-stu-id="225e7-213">-Tag</span></span>
<span data-ttu-id="225e7-214">Określa tagi, które zostaną przypisane do zadania.</span><span class="sxs-lookup"><span data-stu-id="225e7-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e7-215">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="225e7-215">-Confirm</span></span>
<span data-ttu-id="225e7-216">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="225e7-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225e7-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225e7-217">-WhatIf</span></span>
<span data-ttu-id="225e7-218">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="225e7-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225e7-219">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="225e7-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225e7-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225e7-220">CommonParameters</span></span>
<span data-ttu-id="225e7-221">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225e7-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225e7-222">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="225e7-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225e7-223">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="225e7-223">INPUTS</span></span>

## <span data-ttu-id="225e7-224">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="225e7-224">OUTPUTS</span></span>

### <span data-ttu-id="225e7-225">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="225e7-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="225e7-226">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="225e7-226">NOTES</span></span>

<span data-ttu-id="225e7-227">ALIASY</span><span class="sxs-lookup"><span data-stu-id="225e7-227">ALIASES</span></span>

<span data-ttu-id="225e7-228">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="225e7-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="225e7-229">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="225e7-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="225e7-230">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="225e7-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="225e7-231">DRIVELIST <IDriveStatus[]>: lista maksymalnie dziesięciu dysków, które składają się na dane zadanie.</span><span class="sxs-lookup"><span data-stu-id="225e7-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="225e7-232">Lista dysków jest wymaganym elementem dla zadania importu. nie jest określony dla zadań eksportu.</span><span class="sxs-lookup"><span data-stu-id="225e7-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="225e7-233">`[BitLockerKey <String>]`: klawisz BitLocker używany do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="225e7-234">`[BytesSucceeded <Int64?>]`: Bajty zostały pomyślnie przeniesione dla dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="225e7-235">`[CopyStatus <String>]`: szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="225e7-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="225e7-236">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie znajduje się w stanie Przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="225e7-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="225e7-237">`[DriveHeaderHash <String>]`: wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="225e7-238">`[DriveId <String>]`: numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="225e7-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="225e7-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="225e7-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="225e7-240">`[ManifestFile <String>]`: względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="225e7-241">`[ManifestHash <String>]`: Skrót MD5 zakodowany w bazie danych Base16 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="225e7-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span><span class="sxs-lookup"><span data-stu-id="225e7-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="225e7-243">`[PercentComplete <Int32?>]`: Procent ukończenia dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="225e7-244">`[State <DriveState?>]`: bieżący stan dysku.</span><span class="sxs-lookup"><span data-stu-id="225e7-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="225e7-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="225e7-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="225e7-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="225e7-246">RELATED LINKS</span></span>

