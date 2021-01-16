---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364511"
---
# <span data-ttu-id="4d60a-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4d60a-101">New-AzImportExport</span></span>

## <span data-ttu-id="4d60a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d60a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d60a-103">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4d60a-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4d60a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d60a-104">SYNTAX</span></span>

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

## <span data-ttu-id="4d60a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d60a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d60a-106">Tworzy nowe zadanie lub aktualizuje istniejące zadanie w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4d60a-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4d60a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d60a-107">EXAMPLES</span></span>

### <span data-ttu-id="4d60a-108">Przykład 1. Utwórz nowe zadanie ImportExport</span><span class="sxs-lookup"><span data-stu-id="4d60a-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="4d60a-109">Te polecenia cmdlet tworzą nowe zadanie ImportExport.</span><span class="sxs-lookup"><span data-stu-id="4d60a-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="4d60a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d60a-110">PARAMETERS</span></span>

### <span data-ttu-id="4d60a-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4d60a-111">-AcceptLanguage</span></span>
<span data-ttu-id="4d60a-112">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="4d60a-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4d60a-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="4d60a-113">-BackupDriveManifest</span></span>
<span data-ttu-id="4d60a-114">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="4d60a-114">Default value is false.</span></span>
<span data-ttu-id="4d60a-115">Wskazuje, czy pliki manifestu na dyskach powinny być kopiowane w celu zablokowania obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="4d60a-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="4d60a-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="4d60a-116">-BlobListBlobPath</span></span>
<span data-ttu-id="4d60a-117">Kolekcja ciągów ścieżek obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="4d60a-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="4d60a-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="4d60a-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="4d60a-119">Kolekcja ciągów prefiksu obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="4d60a-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="4d60a-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="4d60a-120">-CancelRequested</span></span>
<span data-ttu-id="4d60a-121">Wskazuje, czy przesłano żądanie anulowania zadania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="4d60a-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="4d60a-122">-ClientTenantId</span></span>
<span data-ttu-id="4d60a-123">Identyfikator dzierżawy klienta składającego żądanie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="4d60a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d60a-124">-DefaultProfile</span></span>
<span data-ttu-id="4d60a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d60a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d60a-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4d60a-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="4d60a-127">Nazwa operatora, który jest używany do wysyłania dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="4d60a-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4d60a-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="4d60a-129">Liczba dysków uwzględnionych w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="4d60a-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4d60a-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="4d60a-131">Data wydania paczki.</span><span class="sxs-lookup"><span data-stu-id="4d60a-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="4d60a-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4d60a-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="4d60a-133">Numer śledzenia pakietu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="4d60a-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="4d60a-134">-DiagnosticsPath</span></span>
<span data-ttu-id="4d60a-135">Katalog wirtualnego obiektu BLOB, do którego będą przechowywane dzienniki kopii i kopie zapasowe plików manifestu dysków (jeśli są włączone).</span><span class="sxs-lookup"><span data-stu-id="4d60a-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="4d60a-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="4d60a-136">-DriveList</span></span>
<span data-ttu-id="4d60a-137">Lista składająca się z maksymalnie dziesięciu dysków, które składają się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="4d60a-138">Lista dysków to element wymagany dla zadania importu; nie określono jej w zadaniach eksportowania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="4d60a-139">Aby skonstruować, zobacz sekcję notatki dla właściwości DRIVELIST i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4d60a-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d60a-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="4d60a-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="4d60a-141">Względny identyfikator URI względem obiektu BLOB bloku, który zawiera listę ścieżek obiektu BLOB lub prefiksów ścieżek obiektu BLOB zdefiniowanych powyżej, rozpoczynając od nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="4d60a-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="4d60a-142">Jeśli obiekt BLOB znajduje się w kontenerze głównym, identyfikator URI musi zaczynać się od $root.</span><span class="sxs-lookup"><span data-stu-id="4d60a-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="4d60a-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="4d60a-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="4d60a-144">Ścieżka obiektu BLOB wskazująca element BLOB bloku zawierający listę nazw obiektów blob, które nie zostały wyeksportowane ze względu na niewystarczającą ilość miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="4d60a-145">Jeśli wszystkie obiekty blob zostały pomyślnie wyeksportowane, ten element nie jest uwzględniony w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="4d60a-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="4d60a-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="4d60a-146">-JobType</span></span>
<span data-ttu-id="4d60a-147">Typ zadania</span><span class="sxs-lookup"><span data-stu-id="4d60a-147">The type of job</span></span>

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

### <span data-ttu-id="4d60a-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4d60a-148">-Location</span></span>
<span data-ttu-id="4d60a-149">Określa obsługiwaną lokalizację platformy Azure, w której ma zostać utworzone zadanie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="4d60a-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4d60a-150">-LogLevel</span></span>
<span data-ttu-id="4d60a-151">Wartość domyślna to Error.</span><span class="sxs-lookup"><span data-stu-id="4d60a-151">Default value is Error.</span></span>
<span data-ttu-id="4d60a-152">Wskazuje, czy jest włączone rejestrowanie błędów lub pełne rejestrowanie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="4d60a-153">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d60a-153">-Name</span></span>
<span data-ttu-id="4d60a-154">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="4d60a-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="4d60a-155">-PercentComplete</span></span>
<span data-ttu-id="4d60a-156">Całkowity procent ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="4d60a-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="4d60a-157">-ProvisioningState</span></span>
<span data-ttu-id="4d60a-158">Określa stan aprowizacji zadania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="4d60a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d60a-159">-ResourceGroupName</span></span>
<span data-ttu-id="4d60a-160">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4d60a-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="4d60a-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="4d60a-161">-ReturnAddressCity</span></span>
<span data-ttu-id="4d60a-162">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4d60a-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="4d60a-164">Kraj lub region, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="4d60a-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="4d60a-166">Adres e-mail adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4d60a-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="4d60a-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="4d60a-168">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4d60a-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="4d60a-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="4d60a-170">Kod pocztowy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="4d60a-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="4d60a-172">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="4d60a-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4d60a-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="4d60a-174">Stan lub Prowincja, które mają być używane podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4d60a-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="4d60a-176">Pierwszy wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4d60a-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="4d60a-178">Drugi wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4d60a-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="4d60a-180">Nazwa operatora, który jest używany do wysyłania dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="4d60a-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4d60a-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="4d60a-182">Liczba dysków uwzględnionych w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="4d60a-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4d60a-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="4d60a-184">Data wydania paczki.</span><span class="sxs-lookup"><span data-stu-id="4d60a-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="4d60a-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4d60a-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="4d60a-186">Numer śledzenia pakietu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="4d60a-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="4d60a-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="4d60a-188">Numer konta klienta z przewoźnikiem.</span><span class="sxs-lookup"><span data-stu-id="4d60a-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="4d60a-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="4d60a-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="4d60a-190">Imię i nazwisko operatora.</span><span class="sxs-lookup"><span data-stu-id="4d60a-190">The carrier's name.</span></span>

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

### <span data-ttu-id="4d60a-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="4d60a-191">-ShippingInformationCity</span></span>
<span data-ttu-id="4d60a-192">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4d60a-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="4d60a-194">Kraj lub region, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="4d60a-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="4d60a-196">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4d60a-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="4d60a-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="4d60a-198">Kod pocztowy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="4d60a-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="4d60a-200">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="4d60a-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="4d60a-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4d60a-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="4d60a-202">Stan lub Prowincja, które mają być używane podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4d60a-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="4d60a-204">Pierwszy wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4d60a-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="4d60a-206">Drugi wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4d60a-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4d60a-207">-State</span><span class="sxs-lookup"><span data-stu-id="4d60a-207">-State</span></span>
<span data-ttu-id="4d60a-208">Bieżący stan zadania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-208">Current state of the job.</span></span>

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

### <span data-ttu-id="4d60a-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d60a-209">-StorageAccountId</span></span>
<span data-ttu-id="4d60a-210">Identyfikator zasobu konta magazynu, z którego będą importowane dane lub do których zostaną one wyeksportowane.</span><span class="sxs-lookup"><span data-stu-id="4d60a-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="4d60a-211">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4d60a-211">-SubscriptionId</span></span>
<span data-ttu-id="4d60a-212">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4d60a-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="4d60a-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d60a-213">-Tag</span></span>
<span data-ttu-id="4d60a-214">Określa Tagi, które zostaną przydzielone do zadania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="4d60a-215">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d60a-215">-Confirm</span></span>
<span data-ttu-id="4d60a-216">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d60a-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d60a-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d60a-217">-WhatIf</span></span>
<span data-ttu-id="4d60a-218">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d60a-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d60a-219">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d60a-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d60a-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d60a-220">CommonParameters</span></span>
<span data-ttu-id="4d60a-221">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d60a-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d60a-222">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d60a-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d60a-223">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d60a-223">INPUTS</span></span>

## <span data-ttu-id="4d60a-224">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d60a-224">OUTPUTS</span></span>

### <span data-ttu-id="4d60a-225">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="4d60a-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="4d60a-226">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d60a-226">NOTES</span></span>

<span data-ttu-id="4d60a-227">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4d60a-227">ALIASES</span></span>

<span data-ttu-id="4d60a-228">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d60a-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d60a-229">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4d60a-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d60a-230">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d60a-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d60a-231">DRIVELIST <IDriveStatus [] >: Lista składająca się z maksymalnie dziesięciu dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="4d60a-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="4d60a-232">Lista dysków to element wymagany dla zadania importu; nie określono jej w zadaniach eksportowania.</span><span class="sxs-lookup"><span data-stu-id="4d60a-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="4d60a-233">`[BitLockerKey <String>]`: Klucz funkcji BitLocker służący do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="4d60a-234">`[BytesSucceeded <Int64?>]`: Pomyślnie przeniesiono bajty dla dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="4d60a-235">`[CopyStatus <String>]`: Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="4d60a-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="4d60a-236">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie będzie w stanie przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="4d60a-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="4d60a-237">`[DriveHeaderHash <String>]`: Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="4d60a-238">`[DriveId <String>]`: Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="4d60a-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="4d60a-239">`[ErrorLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający dziennik błędów operacji transferu danych.</span><span class="sxs-lookup"><span data-stu-id="4d60a-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="4d60a-240">`[ManifestFile <String>]`: Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="4d60a-241">`[ManifestHash <String>]`: Zakodowana na Base16 skrót MD5 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="4d60a-242">`[ManifestUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający plik manifestu dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="4d60a-243">`[PercentComplete <Int32?>]`: Procent ukończenia dla dysku.</span><span class="sxs-lookup"><span data-stu-id="4d60a-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="4d60a-244">`[State <DriveState?>]`: Obecny stan stacji.</span><span class="sxs-lookup"><span data-stu-id="4d60a-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="4d60a-245">`[VerboseLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający pełny dziennik w operacji przesyłania danych.</span><span class="sxs-lookup"><span data-stu-id="4d60a-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="4d60a-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d60a-246">RELATED LINKS</span></span>

