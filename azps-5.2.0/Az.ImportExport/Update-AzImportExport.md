---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364483"
---
# <span data-ttu-id="4e024-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4e024-101">Update-AzImportExport</span></span>

## <span data-ttu-id="4e024-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e024-102">SYNOPSIS</span></span>
<span data-ttu-id="4e024-103">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="4e024-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="4e024-104">Możesz zadzwonić do tej operacji, aby powiadomić usługę importu/eksportu, że dyski twarde zawierające zadanie importu lub eksportu zostały wysłane do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e024-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="4e024-105">Można go również użyć, aby anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="4e024-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="4e024-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e024-106">SYNTAX</span></span>

### <span data-ttu-id="4e024-107">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e024-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="4e024-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e024-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="4e024-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4e024-109">DESCRIPTION</span></span>
<span data-ttu-id="4e024-110">Aktualizuje określone właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="4e024-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="4e024-111">Możesz zadzwonić do tej operacji, aby powiadomić usługę importu/eksportu, że dyski twarde zawierające zadanie importu lub eksportu zostały wysłane do centrum danych firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e024-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="4e024-112">Można go również użyć, aby anulować istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="4e024-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="4e024-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e024-113">EXAMPLES</span></span>

### <span data-ttu-id="4e024-114">Przykład 1: aktualizowanie zadania ImportExport według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="4e024-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="4e024-115">To polecenie cmdlet aktualizuje zadanie ImportExport według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="4e024-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="4e024-116">Przykład 2: aktualizowanie zadania ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4e024-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="4e024-117">To polecenie cmdlet aktualizuje zadanie ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4e024-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="4e024-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e024-118">PARAMETERS</span></span>

### <span data-ttu-id="4e024-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4e024-119">-AcceptLanguage</span></span>
<span data-ttu-id="4e024-120">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="4e024-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4e024-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="4e024-121">-BackupDriveManifest</span></span>
<span data-ttu-id="4e024-122">Wskazuje, czy pliki manifestu na dyskach powinny być kopiowane w celu zablokowania obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="4e024-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="4e024-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="4e024-123">-CancelRequested</span></span>
<span data-ttu-id="4e024-124">Jeśli jest określona, musi być wartością prawda.</span><span class="sxs-lookup"><span data-stu-id="4e024-124">If specified, the value must be true.</span></span>
<span data-ttu-id="4e024-125">Usługa podejmie próbę anulowania zadania.</span><span class="sxs-lookup"><span data-stu-id="4e024-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="4e024-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e024-126">-DefaultProfile</span></span>
<span data-ttu-id="4e024-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e024-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e024-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4e024-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="4e024-129">Nazwa operatora, który jest używany do wysyłania dysków importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="4e024-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="4e024-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4e024-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="4e024-131">Liczba dysków uwzględnionych w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="4e024-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="4e024-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4e024-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="4e024-133">Data wydania paczki.</span><span class="sxs-lookup"><span data-stu-id="4e024-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="4e024-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4e024-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="4e024-135">Numer śledzenia pakietu.</span><span class="sxs-lookup"><span data-stu-id="4e024-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="4e024-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="4e024-136">-DriveList</span></span>
<span data-ttu-id="4e024-137">Lista dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="4e024-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="4e024-138">Aby skonstruować, zobacz sekcję notatki dla właściwości DRIVELIST i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4e024-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e024-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e024-139">-InputObject</span></span>
<span data-ttu-id="4e024-140">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4e024-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e024-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4e024-141">-LogLevel</span></span>
<span data-ttu-id="4e024-142">Wskazuje, czy jest włączone rejestrowanie błędów lub pełne rejestrowanie.</span><span class="sxs-lookup"><span data-stu-id="4e024-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="4e024-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e024-143">-Name</span></span>
<span data-ttu-id="4e024-144">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="4e024-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="4e024-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e024-145">-ResourceGroupName</span></span>
<span data-ttu-id="4e024-146">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4e024-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="4e024-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="4e024-147">-ReturnAddressCity</span></span>
<span data-ttu-id="4e024-148">Nazwa miasta do użycia podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4e024-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="4e024-150">Kraj lub region, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="4e024-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="4e024-152">Adres e-mail adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4e024-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="4e024-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="4e024-154">Numer telefonu adresata zwróconych dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="4e024-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="4e024-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="4e024-156">Kod pocztowy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="4e024-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="4e024-158">Nazwa adresata, który otrzyma dyski twarde po ich zwróceniu.</span><span class="sxs-lookup"><span data-stu-id="4e024-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="4e024-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4e024-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="4e024-160">Stan lub Prowincja, które mają być używane podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4e024-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="4e024-162">Pierwszy wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4e024-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="4e024-164">Drugi wiersz adresu ulicy, który ma być używany podczas zwracania dysków.</span><span class="sxs-lookup"><span data-stu-id="4e024-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="4e024-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="4e024-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="4e024-166">Numer konta klienta z przewoźnikiem.</span><span class="sxs-lookup"><span data-stu-id="4e024-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="4e024-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="4e024-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="4e024-168">Imię i nazwisko operatora.</span><span class="sxs-lookup"><span data-stu-id="4e024-168">The carrier's name.</span></span>

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

### <span data-ttu-id="4e024-169">-State</span><span class="sxs-lookup"><span data-stu-id="4e024-169">-State</span></span>
<span data-ttu-id="4e024-170">Jeśli jest określona, wartość musi być równa wysyłce, co informuje usługę importu/eksportu o tym, że pakiet dla zadania został wysłany.</span><span class="sxs-lookup"><span data-stu-id="4e024-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="4e024-171">Właściwości ReturnAddress i DeliveryPackage muszą być ustawione w tym żądaniu lub we wcześniejszych prośbach, w przeciwnym razie żądanie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="4e024-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="4e024-172">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4e024-172">-SubscriptionId</span></span>
<span data-ttu-id="4e024-173">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4e024-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="4e024-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e024-174">-Tag</span></span>
<span data-ttu-id="4e024-175">Określa Tagi, które zostaną przydzielone do zadania.</span><span class="sxs-lookup"><span data-stu-id="4e024-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="4e024-176">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e024-176">-Confirm</span></span>
<span data-ttu-id="4e024-177">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e024-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e024-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e024-178">-WhatIf</span></span>
<span data-ttu-id="4e024-179">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e024-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e024-180">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e024-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e024-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e024-181">CommonParameters</span></span>
<span data-ttu-id="4e024-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e024-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e024-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e024-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e024-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e024-184">INPUTS</span></span>

### <span data-ttu-id="4e024-185">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="4e024-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="4e024-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e024-186">OUTPUTS</span></span>

### <span data-ttu-id="4e024-187">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="4e024-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="4e024-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e024-188">NOTES</span></span>

<span data-ttu-id="4e024-189">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4e024-189">ALIASES</span></span>

<span data-ttu-id="4e024-190">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e024-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e024-191">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4e024-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e024-192">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e024-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e024-193">DRIVELIST <IDriveStatus [] >: Lista dysków składających się na zadanie.</span><span class="sxs-lookup"><span data-stu-id="4e024-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="4e024-194">`[BitLockerKey <String>]`: Klucz funkcji BitLocker służący do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="4e024-195">`[BytesSucceeded <Int64?>]`: Pomyślnie przeniesiono bajty dla dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="4e024-196">`[CopyStatus <String>]`: Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="4e024-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="4e024-197">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie będzie w stanie przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="4e024-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="4e024-198">`[DriveHeaderHash <String>]`: Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="4e024-199">`[DriveId <String>]`: Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="4e024-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="4e024-200">`[ErrorLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający dziennik błędów operacji transferu danych.</span><span class="sxs-lookup"><span data-stu-id="4e024-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="4e024-201">`[ManifestFile <String>]`: Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="4e024-202">`[ManifestHash <String>]`: Zakodowana na Base16 skrót MD5 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="4e024-203">`[ManifestUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający plik manifestu dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="4e024-204">`[PercentComplete <Int32?>]`: Procent ukończenia dla dysku.</span><span class="sxs-lookup"><span data-stu-id="4e024-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="4e024-205">`[State <DriveState?>]`: Obecny stan stacji.</span><span class="sxs-lookup"><span data-stu-id="4e024-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="4e024-206">`[VerboseLogUri <String>]`: Identyfikator URI wskazujący obiekt BLOB zawierający pełny dziennik w operacji przesyłania danych.</span><span class="sxs-lookup"><span data-stu-id="4e024-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="4e024-207">INPUTobject <IImportExportIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4e024-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e024-208">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4e024-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e024-209">`[JobName <String>]`: Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="4e024-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="4e024-210">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4e024-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="4e024-211">Na przykład w przypadku zachodniego, USA lub zachodniego.</span><span class="sxs-lookup"><span data-stu-id="4e024-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="4e024-212">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4e024-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="4e024-213">`[SubscriptionId <String>]`: Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4e024-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="4e024-214">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e024-214">RELATED LINKS</span></span>

