---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195683"
---
# <span data-ttu-id="02183-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="02183-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="02183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02183-102">SYNOPSIS</span></span>
<span data-ttu-id="02183-103">Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="02183-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="02183-104">Może być kierowana do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="02183-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="02183-105">Wykrywanych może być maksymalnie 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="02183-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="02183-106">Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian zakończyło się szybko i z ograniczeniem do 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="02183-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="02183-107">Polecenie Invoke-AzStorageSyncChangeDetection cmdlet nie wykryje następujących zmian w udziału plików platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="02183-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="02183-108">Pliki, które są usuwane.</span><span class="sxs-lookup"><span data-stu-id="02183-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="02183-109">Pliki przeniesione z udziału.</span><span class="sxs-lookup"><span data-stu-id="02183-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="02183-110">Pliki, które są usuwane i tworzone pod taką samą nazwą.</span><span class="sxs-lookup"><span data-stu-id="02183-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="02183-111">Te zmiany zostaną wykryte po [uruchomionym zadaniu wykrywania](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) zmian.</span><span class="sxs-lookup"><span data-stu-id="02183-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="02183-112">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02183-112">SYNTAX</span></span>

### <span data-ttu-id="02183-113">StringAndDirectoryParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="02183-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02183-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="02183-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02183-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="02183-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02183-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="02183-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02183-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="02183-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02183-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="02183-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02183-119">OPIS</span><span class="sxs-lookup"><span data-stu-id="02183-119">DESCRIPTION</span></span>
<span data-ttu-id="02183-120">Okresowo usługa Azure File Sync sprawdza przestrzeń nazw wewnątrz synchronizowania udziału plików platformy Azure pod uwagę pod uwagę zmian wprowadzonych do udziału plików w inny sposób niż w przypadku synchronizacji. Celem jest zidentyfikowanie tych zmian i ich ostateczne zsynchronizowanie z połączonymi serwerami.</span><span class="sxs-lookup"><span data-stu-id="02183-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="02183-121">Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="02183-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="02183-122">Może być kierowana do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="02183-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="02183-123">Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian można było szybko zakończyć z ograniczeniem do 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="02183-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="02183-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02183-124">EXAMPLES</span></span>

### <span data-ttu-id="02183-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02183-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="02183-126">W tym przykładzie wykrywanie zmian jest uruchamiane w katalogach "Dane" i "Raportowanie\Szablony" synchronizowania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02183-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="02183-127">Wszystkie ścieżki są względne do katalogu głównego przestrzeni nazw udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02183-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="02183-128">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="02183-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="02183-129">W tym przykładzie wykrywanie zmian jest uruchamiane w przypadku zestawu plików, które zostały zmienione przez obiekt wywołujący polecenie.</span><span class="sxs-lookup"><span data-stu-id="02183-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="02183-130">Celem jest także wykrywanie i synchronizowanie tych zmian przez synchronizację plików na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="02183-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="02183-131">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="02183-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="02183-132">W tym przykładzie wykrywanie zmian jest uruchamiane dla katalogu "Przykłady" i cyklicznie wykrywa zmiany w podkategorach.</span><span class="sxs-lookup"><span data-stu-id="02183-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="02183-133">Pamiętaj, że polecenie cmdlet nie powiedzie się, jeśli ścieżka będzie zawierała więcej niż 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="02183-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="02183-134">Jeśli ścieżka zawiera więcej niż 10 000 elementów, uruchom polecenie w pod partach przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="02183-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="02183-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02183-135">PARAMETERS</span></span>

### <span data-ttu-id="02183-136">— AsJob</span><span class="sxs-lookup"><span data-stu-id="02183-136">-AsJob</span></span>
<span data-ttu-id="02183-137">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="02183-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02183-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02183-138">-DefaultProfile</span></span>
<span data-ttu-id="02183-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02183-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="02183-140">-DirectoryPath</span></span>
<span data-ttu-id="02183-141">Katalog, w którym zostanie wykonane wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="02183-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02183-142">-InputObject</span></span>
<span data-ttu-id="02183-143">Obiekt CloudEndpoint, normalnie minął przez parametr.</span><span class="sxs-lookup"><span data-stu-id="02183-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02183-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="02183-144">-Name</span></span>
<span data-ttu-id="02183-145">Nazwa programu CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="02183-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="02183-146">Nazwa to identyfikator GUID, a nie przyjazna nazwa wyświetlana w portalu.</span><span class="sxs-lookup"><span data-stu-id="02183-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="02183-147">Aby uzyskać nazwę CloudEndpointName, użyj Get-AzStorageSyncCloudEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02183-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02183-148">-PassThru</span></span>
<span data-ttu-id="02183-149">W normalnym wykonywaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="02183-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="02183-150">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="02183-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="02183-151">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="02183-151">-Path</span></span>
<span data-ttu-id="02183-152">Ścieżka, w której zostanie wykonane wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="02183-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-153">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="02183-153">-Recursive</span></span>
<span data-ttu-id="02183-154">Wskazuje, czy wykrywanie zmiany katalogu ma rekurencyjną.</span><span class="sxs-lookup"><span data-stu-id="02183-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02183-155">-ResourceGroupName</span></span>
<span data-ttu-id="02183-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02183-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02183-157">-ResourceId</span></span>
<span data-ttu-id="02183-158">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="02183-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02183-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="02183-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="02183-160">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="02183-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="02183-161">-SyncGroupName</span></span>
<span data-ttu-id="02183-162">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="02183-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02183-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02183-163">-Confirm</span></span>
<span data-ttu-id="02183-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02183-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02183-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02183-165">-WhatIf</span></span>
<span data-ttu-id="02183-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02183-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02183-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02183-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02183-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02183-168">CommonParameters</span></span>
<span data-ttu-id="02183-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02183-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02183-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02183-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02183-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02183-171">INPUTS</span></span>

### <span data-ttu-id="02183-172">System.String</span><span class="sxs-lookup"><span data-stu-id="02183-172">System.String</span></span>

### <span data-ttu-id="02183-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02183-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="02183-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02183-174">OUTPUTS</span></span>

### <span data-ttu-id="02183-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="02183-175">System.Void</span></span>

## <span data-ttu-id="02183-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02183-176">NOTES</span></span>

## <span data-ttu-id="02183-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02183-177">RELATED LINKS</span></span>
