---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503530"
---
# <span data-ttu-id="da969-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="da969-101">New-AzImportExport</span></span>

## <span data-ttu-id="da969-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da969-102">SYNOPSIS</span></span>
<span data-ttu-id="da969-103">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da969-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="da969-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da969-104">SYNTAX</span></span>

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

## <span data-ttu-id="da969-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da969-105">DESCRIPTION</span></span>
<span data-ttu-id="da969-106">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da969-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="da969-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da969-107">EXAMPLES</span></span>

### <span data-ttu-id="da969-108">Przykład 1. Utwórz nowe zadanie ImportExport</span><span class="sxs-lookup"><span data-stu-id="da969-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="da969-109">Te polecenia cmdlet tworzą nowe zadanie ImportExport.</span><span class="sxs-lookup"><span data-stu-id="da969-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="da969-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da969-110">PARAMETERS</span></span>

### <span data-ttu-id="da969-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="da969-111">-AcceptLanguage</span></span>
<span data-ttu-id="da969-112">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="da969-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="da969-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="da969-113">-BackupDriveManifest</span></span>
<span data-ttu-id="da969-114">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="da969-114">Default value is false.</span></span>
<span data-ttu-id="da969-115">Wskazuje, czy pliki manifestu na dyskach powinny być kopiowane w celu zablokowania obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="da969-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="da969-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="da969-116">-BlobListBlobPath</span></span>
<span data-ttu-id="da969-117">Kolekcja ciągów ścieżek obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="da969-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="da969-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="da969-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="da969-119">Kolekcja ciągów prefiksu obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="da969-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="da969-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="da969-120">-CancelRequested</span></span>
<span data-ttu-id="da969-121">Wskazuje, czy przesłano żądanie anulowania zadania.</span><span class="sxs-lookup"><span data-stu-id="da969-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="da969-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="da969-122">-ClientTenantId</span></span>
<span data-ttu-id="da969-123">Identyfikator dzierżawy klienta składającego żądanie.</span><span class="sxs-lookup"><span data-stu-id="da969-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="da969-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da969-124">-DefaultProfile</span></span>
<span data-ttu-id="da969-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da969-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da969-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="da969-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="da969-127">Nazwa operatora, który jest używany do wysyłania dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="da969-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="da969-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="da969-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="da969-129">Liczba dysków uwzględnionych w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="da969-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="da969-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="da969-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="da969-131">Data wydania paczki.</span><span class="sxs-lookup"><span data-stu-id="da969-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="da969-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="da969-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="da969-133">Numer śledzenia pakietu.</span><span class="sxs-lookup"><span data-stu-id="da969-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="da969-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="da969-134">-DiagnosticsPath</span></span>
<span data-ttu-id="da969-135">Katalog wirtualnego obiektu BLOB, do którego będą przechowywane dzienniki kopii i kopie zapasowe plików manifestu dysków (jeśli są włączone).</span><span class="sxs-lookup"><span data-stu-id="da969-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="da969-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="da969-136">-DriveList</span></span>
<span data-ttu-id="da969-137">Lista składająca się z maksymalnie dziesięciu dysków, które składają się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="da969-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="da969-138">Lista dysków to element wymagany dla zadania importu; nie określono jej w zadaniach eksportowania.</span><span class="sxs-lookup"><span data-stu-id="da969-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="da969-139">Aby skonstruować, zobacz sekcję notatki dla właściwości DRIVELIST i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="da969-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="da969-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="da969-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="da969-141">Względny identyfikator URI względem obiektu BLOB bloku, który zawiera listę ścieżek obiektu BLOB lub prefiksów ścieżek obiektu BLOB zdefiniowanych powyżej, rozpoczynając od nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="da969-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="da969-142">Jeśli obiekt BLOB znajduje się w kontenerze głównym, identyfikator URI musi zaczynać się od $root.</span><span class="sxs-lookup"><span data-stu-id="da969-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="da969-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="da969-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="da969-144">Ścieżka obiektu BLOB wskazująca element BLOB bloku zawierający listę nazw obiektów blob, które nie zostały wyeksportowane ze względu na niewystarczającą ilość miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="da969-145">Jeśli wszystkie obiekty blob zostały pomyślnie wyeksportowane, ten element nie jest uwzględniony w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="da969-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="da969-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="da969-146">-JobType</span></span>
<span data-ttu-id="da969-147">Typ zadania</span><span class="sxs-lookup"><span data-stu-id="da969-147">The type of job</span></span>

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

### <span data-ttu-id="da969-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="da969-148">-Location</span></span>
<span data-ttu-id="da969-149">Określa obsługiwaną lokalizację platformy Azure, w której ma zostać utworzone zadanie.</span><span class="sxs-lookup"><span data-stu-id="da969-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="da969-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="da969-150">-LogLevel</span></span>
<span data-ttu-id="da969-151">Wartość domyślna to Error.</span><span class="sxs-lookup"><span data-stu-id="da969-151">Default value is Error.</span></span>
<span data-ttu-id="da969-152">Wskazuje, czy jest włączone rejestrowanie błędów lub pełne rejestrowanie.</span><span class="sxs-lookup"><span data-stu-id="da969-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="da969-153">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da969-153">-Name</span></span>
<span data-ttu-id="da969-154">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="da969-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="da969-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="da969-155">-PercentComplete</span></span>
<span data-ttu-id="da969-156">Całkowity procent ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="da969-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="da969-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="da969-157">-ProvisioningState</span></span>
<span data-ttu-id="da969-158">Określa stan aprowizacji zadania.</span><span class="sxs-lookup"><span data-stu-id="da969-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="da969-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da969-159">-ResourceGroupName</span></span>
<span data-ttu-id="da969-160">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="da969-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="da969-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="da969-161">-ReturnAddressCity</span></span>
<span data-ttu-id="da969-162">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="da969-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="da969-164">Kraj lub region, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="da969-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="da969-166">Adres e-mail adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="da969-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="da969-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="da969-168">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="da969-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="da969-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="da969-170">Kod pocztowy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="da969-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="da969-172">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="da969-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="da969-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="da969-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="da969-174">Stan lub Prowincja, które mają być używane podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="da969-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="da969-176">Pierwszy wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="da969-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="da969-178">Drugi wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="da969-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="da969-180">Nazwa operatora, który jest używany do wysyłania dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="da969-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="da969-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="da969-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="da969-182">Liczba dysków uwzględnionych w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="da969-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="da969-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="da969-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="da969-184">Data wydania paczki.</span><span class="sxs-lookup"><span data-stu-id="da969-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="da969-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="da969-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="da969-186">Numer śledzenia pakietu.</span><span class="sxs-lookup"><span data-stu-id="da969-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="da969-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="da969-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="da969-188">Numer konta klienta z przewoźnikiem.</span><span class="sxs-lookup"><span data-stu-id="da969-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="da969-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="da969-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="da969-190">Imię i nazwisko operatora.</span><span class="sxs-lookup"><span data-stu-id="da969-190">The carrier's name.</span></span>

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

### <span data-ttu-id="da969-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="da969-191">-ShippingInformationCity</span></span>
<span data-ttu-id="da969-192">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="da969-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="da969-194">Kraj lub region, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="da969-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="da969-196">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="da969-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="da969-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="da969-198">Kod pocztowy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="da969-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="da969-200">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="da969-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="da969-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="da969-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="da969-202">Stan lub Prowincja, które mają być używane podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="da969-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="da969-204">Pierwszy wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="da969-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="da969-206">Drugi wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="da969-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="da969-207">-State</span><span class="sxs-lookup"><span data-stu-id="da969-207">-State</span></span>
<span data-ttu-id="da969-208">Bieżący stan zadania.</span><span class="sxs-lookup"><span data-stu-id="da969-208">Current state of the job.</span></span>

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

### <span data-ttu-id="da969-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="da969-209">-StorageAccountId</span></span>
<span data-ttu-id="da969-210">Identyfikator zasobu konta magazynu, z którego będą importowane dane lub do których zostaną one wyeksportowane.</span><span class="sxs-lookup"><span data-stu-id="da969-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="da969-211">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da969-211">-SubscriptionId</span></span>
<span data-ttu-id="da969-212">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da969-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="da969-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="da969-213">-Tag</span></span>
<span data-ttu-id="da969-214">Określa Tagi, które zostaną przydzielone do zadania.</span><span class="sxs-lookup"><span data-stu-id="da969-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="da969-215">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da969-215">-Confirm</span></span>
<span data-ttu-id="da969-216">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da969-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da969-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da969-217">-WhatIf</span></span>
<span data-ttu-id="da969-218">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da969-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da969-219">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da969-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da969-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da969-220">CommonParameters</span></span>
<span data-ttu-id="da969-221">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da969-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da969-222">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da969-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da969-223">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da969-223">INPUTS</span></span>

## <span data-ttu-id="da969-224">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da969-224">OUTPUTS</span></span>

### <span data-ttu-id="da969-225">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="da969-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="da969-226">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da969-226">NOTES</span></span>

<span data-ttu-id="da969-227">PISUJE</span><span class="sxs-lookup"><span data-stu-id="da969-227">ALIASES</span></span>

<span data-ttu-id="da969-228">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da969-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da969-229">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="da969-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da969-230">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da969-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da969-231">DRIVELIST <IDriveStatus [] >: Lista składająca się z maksymalnie dziesięciu dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="da969-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="da969-232">Lista dysków to element wymagany dla zadania importu; nie określono jej w zadaniach eksportowania.</span><span class="sxs-lookup"><span data-stu-id="da969-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="da969-233">`[BitLockerKey <String>]`: Klucz funkcji BitLocker służący do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="da969-234">`[BytesSucceeded <Int64?>]`: Pomyślnie przeniesiono bajty dla dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="da969-235">`[CopyStatus <String>]`: Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="da969-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="da969-236">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie będzie w stanie przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="da969-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="da969-237">`[DriveHeaderHash <String>]`: Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="da969-238">`[DriveId <String>]`: Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="da969-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="da969-239">`[ErrorLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający dziennik błędów operacji transferu danych.</span><span class="sxs-lookup"><span data-stu-id="da969-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="da969-240">`[ManifestFile <String>]`: Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="da969-241">`[ManifestHash <String>]`: Zakodowana na Base16 skrót MD5 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="da969-242">`[ManifestUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający plik manifestu dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="da969-243">`[PercentComplete <Int32?>]`: Procent ukończenia dla dysku.</span><span class="sxs-lookup"><span data-stu-id="da969-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="da969-244">`[State <DriveState?>]`: Obecny stan stacji.</span><span class="sxs-lookup"><span data-stu-id="da969-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="da969-245">`[VerboseLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający pełny dziennik w operacji przesyłania danych.</span><span class="sxs-lookup"><span data-stu-id="da969-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="da969-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da969-246">RELATED LINKS</span></span>

