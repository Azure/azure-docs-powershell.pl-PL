---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491218"
---
# <span data-ttu-id="21f98-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="21f98-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="21f98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21f98-102">SYNOPSIS</span></span>
<span data-ttu-id="21f98-103">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="21f98-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="21f98-104">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="21f98-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="21f98-105">Można wykryć maksymalnie 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="21f98-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="21f98-106">Jeśli zakres zmian jest znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, więc funkcja wykrywania zmian może szybko zakończyć działanie i w ramach limitu elementów 10 000.</span><span class="sxs-lookup"><span data-stu-id="21f98-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="21f98-107">Polecenie cmdlet Invoke-AzStorageSyncChangeDetection nie będzie wykrywać następujących zmian w udziale plików platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="21f98-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="21f98-108">Pliki, które zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="21f98-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="21f98-109">Pliki przenoszone z udziału.</span><span class="sxs-lookup"><span data-stu-id="21f98-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="21f98-110">Pliki, które zostały usunięte i utworzone pod tą samą nazwą.</span><span class="sxs-lookup"><span data-stu-id="21f98-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="21f98-111">Te zmiany zostaną wykryte po uruchomieniu [zadania wykrywania zmian](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) .</span><span class="sxs-lookup"><span data-stu-id="21f98-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="21f98-112">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21f98-112">SYNTAX</span></span>

### <span data-ttu-id="21f98-113">StringAndDirectoryParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21f98-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f98-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f98-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f98-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f98-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f98-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f98-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f98-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f98-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f98-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f98-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f98-119">Opis</span><span class="sxs-lookup"><span data-stu-id="21f98-119">DESCRIPTION</span></span>
<span data-ttu-id="21f98-120">Usługa Azure File Sync sprawdza okresowo obszar nazw w ramach synchronizowania udziału plików platformy Azure na potrzeby zmian, które zostały udostępnione do udziału plików w inny sposób niż synchronizacja. Celem jest zidentyfikowanie tych zmian, a następnie zsynchronizowanie ich z serwerami podłączonymi.</span><span class="sxs-lookup"><span data-stu-id="21f98-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="21f98-121">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="21f98-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="21f98-122">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="21f98-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="21f98-123">Jeśli zakres zmian jest znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="21f98-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="21f98-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21f98-124">EXAMPLES</span></span>

### <span data-ttu-id="21f98-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21f98-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="21f98-126">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w katalogach "dane" i "Reporting\Templates" w katalogu synchronizowanym udziale plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21f98-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="21f98-127">Wszystkie ścieżki są powiązane z głównym obszarem nazw udziału plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="21f98-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="21f98-128">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21f98-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="21f98-129">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w przypadku zestawu plików, które są znane identyfikatorowi rozmówcy polecenia.</span><span class="sxs-lookup"><span data-stu-id="21f98-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="21f98-130">Celem jest również wykrycie i zsynchronizowanie tych zmian przez synchronizację plików Azure.</span><span class="sxs-lookup"><span data-stu-id="21f98-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="21f98-131">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="21f98-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="21f98-132">W tym przykładzie funkcja wykrywania zmian jest uruchamiana dla katalogu "Przykłady" i rekursywnie wykrywa zmiany w podkatalogach.</span><span class="sxs-lookup"><span data-stu-id="21f98-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="21f98-133">Pamiętaj, że polecenie cmdlet nie powiedzie się, jeśli ścieżka zawiera więcej niż 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="21f98-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="21f98-134">Jeśli ścieżka zawiera więcej niż 10 000 elementów, uruchom polecenie w części podrzędnej obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="21f98-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="21f98-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21f98-135">PARAMETERS</span></span>

### <span data-ttu-id="21f98-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21f98-136">-AsJob</span></span>
<span data-ttu-id="21f98-137">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="21f98-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21f98-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f98-138">-DefaultProfile</span></span>
<span data-ttu-id="21f98-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21f98-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f98-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="21f98-140">-DirectoryPath</span></span>
<span data-ttu-id="21f98-141">Katalog, w którym zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="21f98-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="21f98-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21f98-142">-InputObject</span></span>
<span data-ttu-id="21f98-143">Obiekt CloudEndpoint, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="21f98-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="21f98-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21f98-144">-Name</span></span>
<span data-ttu-id="21f98-145">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="21f98-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="21f98-146">Nazwa jest identyfikatorem GUID, a nie jest przyjazną nazwą wyświetlaną w portalu.</span><span class="sxs-lookup"><span data-stu-id="21f98-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="21f98-147">Aby uzyskać CloudEndpointName, użyj polecenia cmdlet Get-AzStorageSyncCloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="21f98-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="21f98-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21f98-148">-PassThru</span></span>
<span data-ttu-id="21f98-149">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="21f98-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="21f98-150">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="21f98-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="21f98-151">-Path</span><span class="sxs-lookup"><span data-stu-id="21f98-151">-Path</span></span>
<span data-ttu-id="21f98-152">Ścieżka, w której zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="21f98-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="21f98-153">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="21f98-153">-Recursive</span></span>
<span data-ttu-id="21f98-154">Wskazuje, czy wykrywanie zmian katalogów jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="21f98-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="21f98-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f98-155">-ResourceGroupName</span></span>
<span data-ttu-id="21f98-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21f98-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="21f98-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f98-157">-ResourceId</span></span>
<span data-ttu-id="21f98-158">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f98-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="21f98-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="21f98-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="21f98-160">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="21f98-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="21f98-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="21f98-161">-SyncGroupName</span></span>
<span data-ttu-id="21f98-162">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="21f98-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="21f98-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21f98-163">-Confirm</span></span>
<span data-ttu-id="21f98-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f98-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f98-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f98-165">-WhatIf</span></span>
<span data-ttu-id="21f98-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f98-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f98-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21f98-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f98-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f98-168">CommonParameters</span></span>
<span data-ttu-id="21f98-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f98-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f98-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f98-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f98-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21f98-171">INPUTS</span></span>

### <span data-ttu-id="21f98-172">System. String</span><span class="sxs-lookup"><span data-stu-id="21f98-172">System.String</span></span>

### <span data-ttu-id="21f98-173">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f98-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="21f98-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21f98-174">OUTPUTS</span></span>

### <span data-ttu-id="21f98-175">System. void</span><span class="sxs-lookup"><span data-stu-id="21f98-175">System.Void</span></span>

## <span data-ttu-id="21f98-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21f98-176">NOTES</span></span>

## <span data-ttu-id="21f98-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21f98-177">RELATED LINKS</span></span>
