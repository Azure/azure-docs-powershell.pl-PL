---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: d55ffe30554c70b9d7b8fa1ed90380c6a5b181cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011425"
---
# <span data-ttu-id="f9d8a-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="f9d8a-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="f9d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d8a-103">Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="f9d8a-104">Może być kierowana do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="f9d8a-105">Wykrywanych może być maksymalnie 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="f9d8a-106">Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian zakończyło się szybko i z ograniczeniem do 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="f9d8a-107">Polecenie Invoke-AzStorageSyncChangeDetection cmdlet nie wykryje następujących zmian w udziału plików platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="f9d8a-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="f9d8a-108">Pliki, które zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="f9d8a-109">Pliki przeniesione z udziału.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="f9d8a-110">Pliki, które są usuwane i tworzone pod taką samą nazwą.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="f9d8a-111">Te zmiany zostaną wykryte po [uruchomionym zadaniu wykrywania](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) zmian.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="f9d8a-112">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9d8a-112">SYNTAX</span></span>

### <span data-ttu-id="f9d8a-113">StringAndDirectoryParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f9d8a-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d8a-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d8a-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d8a-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d8a-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d8a-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d8a-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d8a-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d8a-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d8a-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d8a-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d8a-119">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9d8a-119">DESCRIPTION</span></span>
<span data-ttu-id="f9d8a-120">Okresowo usługa Azure File Sync sprawdza przestrzeń nazw wewnątrz synchronizowania udziału plików platformy Azure pod uwagę pod uwagę zmian wprowadzonych do udziału plików w inny sposób niż w przypadku synchronizacji. Celem jest zidentyfikowanie tych zmian i ich ostateczne zsynchronizowanie z połączonymi serwerami.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="f9d8a-121">Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="f9d8a-122">Może być kierowana do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="f9d8a-123">Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian można było szybko zakończyć z ograniczeniem do 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="f9d8a-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9d8a-124">EXAMPLES</span></span>

### <span data-ttu-id="f9d8a-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9d8a-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="f9d8a-126">W tym przykładzie wykrywanie zmian jest uruchamiane w katalogach "Dane" i "Raportowanie\Szablony" synchronizowania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="f9d8a-127">Wszystkie ścieżki są względne do katalogu głównego przestrzeni nazw udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="f9d8a-128">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9d8a-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="f9d8a-129">W tym przykładzie wykrywanie zmian jest uruchamiane w przypadku zestawu plików, które zostały zmienione przez obiekt wywołujący polecenie.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="f9d8a-130">Celem jest także wykrycie i zsynchronizowanie tych zmian przez synchronizację plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="f9d8a-131">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9d8a-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="f9d8a-132">W tym przykładzie wykrywanie zmian jest uruchamiane dla katalogu "Przykłady" i cyklicznie wykrywa zmiany w podkategorach.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="f9d8a-133">Pamiętaj, że polecenie cmdlet nie powiedzie się, jeśli ścieżka będzie zawierała więcej niż 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="f9d8a-134">Jeśli ścieżka zawiera więcej niż 10 000 elementów, uruchom polecenie w pod partach przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="f9d8a-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9d8a-135">PARAMETERS</span></span>

### <span data-ttu-id="f9d8a-136">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f9d8a-136">-AsJob</span></span>
<span data-ttu-id="f9d8a-137">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f9d8a-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9d8a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d8a-138">-DefaultProfile</span></span>
<span data-ttu-id="f9d8a-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d8a-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="f9d8a-140">-DirectoryPath</span></span>
<span data-ttu-id="f9d8a-141">Katalog, w którym zostanie wykonane wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="f9d8a-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d8a-142">-InputObject</span></span>
<span data-ttu-id="f9d8a-143">Obiekt CloudEndpoint, normalnie minął przez parametr.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f9d8a-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f9d8a-144">-Name</span></span>
<span data-ttu-id="f9d8a-145">Nazwa programu CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="f9d8a-146">Nazwa to identyfikator GUID, a nie przyjazna nazwa wyświetlana w portalu.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="f9d8a-147">Aby uzyskać nazwę CloudEndpointName, użyj Get-AzStorageSyncCloudEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="f9d8a-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9d8a-148">-PassThru</span></span>
<span data-ttu-id="f9d8a-149">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f9d8a-150">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f9d8a-151">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="f9d8a-151">-Path</span></span>
<span data-ttu-id="f9d8a-152">Ścieżka, w której zostanie wykonane wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="f9d8a-153">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="f9d8a-153">-Recursive</span></span>
<span data-ttu-id="f9d8a-154">Wskazuje, czy wykrywanie zmiany katalogu ma rekurencyjną.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="f9d8a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d8a-155">-ResourceGroupName</span></span>
<span data-ttu-id="f9d8a-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9d8a-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d8a-157">-ResourceId</span></span>
<span data-ttu-id="f9d8a-158">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9d8a-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="f9d8a-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f9d8a-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="f9d8a-160">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f9d8a-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d8a-161">-SyncGroupName</span></span>
<span data-ttu-id="f9d8a-162">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="f9d8a-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9d8a-163">-Confirm</span></span>
<span data-ttu-id="f9d8a-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d8a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d8a-165">-WhatIf</span></span>
<span data-ttu-id="f9d8a-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d8a-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d8a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d8a-168">CommonParameters</span></span>
<span data-ttu-id="f9d8a-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d8a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d8a-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d8a-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d8a-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9d8a-171">INPUTS</span></span>

### <span data-ttu-id="f9d8a-172">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d8a-172">System.String</span></span>

### <span data-ttu-id="f9d8a-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9d8a-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="f9d8a-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9d8a-174">OUTPUTS</span></span>

### <span data-ttu-id="f9d8a-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="f9d8a-175">System.Void</span></span>

## <span data-ttu-id="f9d8a-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9d8a-176">NOTES</span></span>

## <span data-ttu-id="f9d8a-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9d8a-177">RELATED LINKS</span></span>
