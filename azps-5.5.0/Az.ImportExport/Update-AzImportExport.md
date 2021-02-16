---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203932"
---
# <span data-ttu-id="95ab3-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="95ab3-101">Update-AzImportExport</span></span>

## <span data-ttu-id="95ab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="95ab3-103">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="95ab3-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="95ab3-104">Tę operację można wywołać w celu powiadomienia usługi importowania/eksportowania, że dyski twarde wywchiwują zadanie importu lub eksportu do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="95ab3-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="95ab3-105">Za jego pomocą można także anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="95ab3-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95ab3-106">SYNTAX</span></span>

### <span data-ttu-id="95ab3-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="95ab3-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95ab3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="95ab3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95ab3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="95ab3-109">DESCRIPTION</span></span>
<span data-ttu-id="95ab3-110">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="95ab3-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="95ab3-111">Tę operację można wywołać w celu powiadomienia usługi importowania/eksportowania, że dyski twarde wywchiwują zadanie importu lub eksportu do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="95ab3-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="95ab3-112">Za jego pomocą można także anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="95ab3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95ab3-113">EXAMPLES</span></span>

### <span data-ttu-id="95ab3-114">Przykład 1. Aktualizowanie zadania ImportExport według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="95ab3-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="95ab3-115">To polecenie cmdlet aktualizuje zadanie ImportExport według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="95ab3-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="95ab3-116">Przykład 2. Aktualizowanie zadania ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="95ab3-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="95ab3-117">To polecenie cmdlet aktualizuje zadanie ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="95ab3-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="95ab3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95ab3-118">PARAMETERS</span></span>

### <span data-ttu-id="95ab3-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="95ab3-119">-AcceptLanguage</span></span>
<span data-ttu-id="95ab3-120">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="95ab3-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="95ab3-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="95ab3-121">-BackupDriveManifest</span></span>
<span data-ttu-id="95ab3-122">Wskazuje, czy pliki manifestu na dyskach powinny zostać skopiowane w celu zablokowania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="95ab3-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="95ab3-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="95ab3-123">-CancelRequested</span></span>
<span data-ttu-id="95ab3-124">Jeśli zostanie określona, wartość musi być prawdziwa.</span><span class="sxs-lookup"><span data-stu-id="95ab3-124">If specified, the value must be true.</span></span>
<span data-ttu-id="95ab3-125">Usługa spróbuje anulować zadanie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="95ab3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ab3-126">-DefaultProfile</span></span>
<span data-ttu-id="95ab3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95ab3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ab3-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="95ab3-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="95ab3-129">Nazwa operatora używanego do wysyłki dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="95ab3-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="95ab3-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="95ab3-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="95ab3-131">Liczba dysków dołączonych do pakietu.</span><span class="sxs-lookup"><span data-stu-id="95ab3-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="95ab3-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="95ab3-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="95ab3-133">Data wysyłki paczki.</span><span class="sxs-lookup"><span data-stu-id="95ab3-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="95ab3-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="95ab3-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="95ab3-135">Numer śledzenia przesyłki.</span><span class="sxs-lookup"><span data-stu-id="95ab3-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="95ab3-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="95ab3-136">-DriveList</span></span>
<span data-ttu-id="95ab3-137">Lista dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="95ab3-138">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach listy dysków i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="95ab3-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="95ab3-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ab3-139">-InputObject</span></span>
<span data-ttu-id="95ab3-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="95ab3-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab3-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="95ab3-141">-LogLevel</span></span>
<span data-ttu-id="95ab3-142">Wskazuje, czy funkcja rejestrowania błędów, czy rejestrowania szczegółowego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="95ab3-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="95ab3-143">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="95ab3-143">-Name</span></span>
<span data-ttu-id="95ab3-144">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="95ab3-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ab3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ab3-145">-ResourceGroupName</span></span>
<span data-ttu-id="95ab3-146">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="95ab3-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ab3-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="95ab3-147">-ReturnAddressCity</span></span>
<span data-ttu-id="95ab3-148">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="95ab3-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="95ab3-150">Kraj lub region, z których należy korzystać podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="95ab3-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="95ab3-152">Adres e-mail adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="95ab3-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="95ab3-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="95ab3-154">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="95ab3-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="95ab3-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="95ab3-156">Kod pocztowy do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="95ab3-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="95ab3-158">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="95ab3-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="95ab3-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="95ab3-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="95ab3-160">Stan lub prowincja do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="95ab3-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="95ab3-162">Pierwszy wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="95ab3-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="95ab3-164">Drugi wiersz ulicy, który ma być podany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="95ab3-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="95ab3-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="95ab3-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="95ab3-166">Numer konta klienta u operatora.</span><span class="sxs-lookup"><span data-stu-id="95ab3-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="95ab3-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="95ab3-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="95ab3-168">Imię i nazwisko operatora.</span><span class="sxs-lookup"><span data-stu-id="95ab3-168">The carrier's name.</span></span>

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

### <span data-ttu-id="95ab3-169">— województwo</span><span class="sxs-lookup"><span data-stu-id="95ab3-169">-State</span></span>
<span data-ttu-id="95ab3-170">Jeśli ta wartość jest określona, musi to być wartość Wysyłka, co informuje usługę importu/eksportu o wysłaniu paczki dla zadania.</span><span class="sxs-lookup"><span data-stu-id="95ab3-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="95ab3-171">Właściwości ReturnAddress i DeliveryPackage muszą zostać ustawione w tym żądaniu lub w poprzednim żądaniu, w przeciwnym razie żądanie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="95ab3-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="95ab3-172">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95ab3-172">-SubscriptionId</span></span>
<span data-ttu-id="95ab3-173">Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95ab3-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ab3-174">— Tag</span><span class="sxs-lookup"><span data-stu-id="95ab3-174">-Tag</span></span>
<span data-ttu-id="95ab3-175">Określa tagi, które zostaną przypisane do zadania.</span><span class="sxs-lookup"><span data-stu-id="95ab3-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ab3-176">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95ab3-176">-Confirm</span></span>
<span data-ttu-id="95ab3-177">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ab3-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ab3-178">-WhatIf</span></span>
<span data-ttu-id="95ab3-179">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95ab3-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ab3-180">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95ab3-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ab3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ab3-181">CommonParameters</span></span>
<span data-ttu-id="95ab3-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ab3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ab3-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95ab3-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ab3-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95ab3-184">INPUTS</span></span>

### <span data-ttu-id="95ab3-185">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="95ab3-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="95ab3-186">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95ab3-186">OUTPUTS</span></span>

### <span data-ttu-id="95ab3-187">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="95ab3-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="95ab3-188">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95ab3-188">NOTES</span></span>

<span data-ttu-id="95ab3-189">ALIASY</span><span class="sxs-lookup"><span data-stu-id="95ab3-189">ALIASES</span></span>

<span data-ttu-id="95ab3-190">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="95ab3-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95ab3-191">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="95ab3-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95ab3-192">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95ab3-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95ab3-193">DRIVELIST <IDriveStatus[]>: Lista dysków składających się na to zadanie.</span><span class="sxs-lookup"><span data-stu-id="95ab3-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="95ab3-194">`[BitLockerKey <String>]`: klawisz BitLocker używany do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="95ab3-195">`[BytesSucceeded <Int64?>]`: Bajty zostały pomyślnie przeniesione dla dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="95ab3-196">`[CopyStatus <String>]`: szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="95ab3-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="95ab3-197">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie znajduje się w stanie Przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="95ab3-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="95ab3-198">`[DriveHeaderHash <String>]`: wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="95ab3-199">`[DriveId <String>]`: numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="95ab3-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="95ab3-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="95ab3-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="95ab3-201">`[ManifestFile <String>]`: względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="95ab3-202">`[ManifestHash <String>]`: Skrót MD5 zakodowany w bazie danych Base16 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="95ab3-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span><span class="sxs-lookup"><span data-stu-id="95ab3-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="95ab3-204">`[PercentComplete <Int32?>]`: Procent ukończenia dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="95ab3-205">`[State <DriveState?>]`: bieżący stan dysku.</span><span class="sxs-lookup"><span data-stu-id="95ab3-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="95ab3-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="95ab3-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="95ab3-207">INPUTOBJECT: <IImportExportIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="95ab3-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95ab3-208">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="95ab3-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95ab3-209">`[JobName <String>]`: nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="95ab3-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="95ab3-210">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="95ab3-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="95ab3-211">Na przykład Stany Zjednoczone Lub Zachód.</span><span class="sxs-lookup"><span data-stu-id="95ab3-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="95ab3-212">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="95ab3-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="95ab3-213">`[SubscriptionId <String>]`: Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95ab3-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="95ab3-214">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95ab3-214">RELATED LINKS</span></span>

