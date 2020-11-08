---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052100"
---
# <span data-ttu-id="5053a-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="5053a-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="5053a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5053a-102">SYNOPSIS</span></span>
<span data-ttu-id="5053a-103">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="5053a-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="5053a-104">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="5053a-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="5053a-105">Można wykryć maksymalnie 10 000 elementów.</span><span class="sxs-lookup"><span data-stu-id="5053a-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="5053a-106">Jeśli zakres zmian jest znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, więc funkcja wykrywania zmian może szybko zakończyć działanie i w ramach limitu elementów 10 000.</span><span class="sxs-lookup"><span data-stu-id="5053a-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="5053a-107">Polecenie cmdlet Invoke-AzStorageSyncChangeDetection nie wykrywa plików, które zostały usunięte z udziału plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="5053a-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="5053a-108">Jeśli pliki zostaną usunięte z udziału plików w usłudze Azure, będą one wykrywane po uruchomieniu [zadania wykrywania zmian](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) .</span><span class="sxs-lookup"><span data-stu-id="5053a-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="5053a-109">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5053a-109">SYNTAX</span></span>

### <span data-ttu-id="5053a-110">StringAndDirectoryParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5053a-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5053a-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5053a-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5053a-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="5053a-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5053a-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5053a-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5053a-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="5053a-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5053a-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="5053a-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5053a-116">Opis</span><span class="sxs-lookup"><span data-stu-id="5053a-116">DESCRIPTION</span></span>
<span data-ttu-id="5053a-117">Usługa Azure File Sync sprawdza okresowo obszar nazw w ramach synchronizowania udziału plików platformy Azure na potrzeby zmian, które zostały udostępnione do udziału plików w inny sposób niż synchronizacja. Celem jest zidentyfikowanie tych zmian, a następnie zsynchronizowanie ich z serwerami podłączonymi.</span><span class="sxs-lookup"><span data-stu-id="5053a-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="5053a-118">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="5053a-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="5053a-119">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="5053a-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="5053a-120">Jeśli zakres zmian jest dla Ciebie znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="5053a-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="5053a-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5053a-121">EXAMPLES</span></span>

### <span data-ttu-id="5053a-122">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5053a-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="5053a-123">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w katalogach "dane" i "Reporting\Templates" w katalogu synchronizowanym udziale plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5053a-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="5053a-124">Wszystkie ścieżki są powiązane z głównym obszarem nazw udziału plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="5053a-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="5053a-125">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5053a-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="5053a-126">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w przypadku zestawu plików, które są znane identyfikatorowi rozmówcy polecenia.</span><span class="sxs-lookup"><span data-stu-id="5053a-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="5053a-127">Celem jest również wykrycie i zsynchronizowanie tych zmian przez synchronizację plików Azure.</span><span class="sxs-lookup"><span data-stu-id="5053a-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="5053a-128">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5053a-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="5053a-129">W tym przykładzie funkcja wykrywania zmian jest uruchamiana dla katalogu "Przykłady" i rekursywnie wykrywa zmiany w podkatalogach.</span><span class="sxs-lookup"><span data-stu-id="5053a-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="5053a-130">Pamiętaj, że to polecenie może wykryć do 10 000 zmian, zanim zostanie automatycznie przerwane.</span><span class="sxs-lookup"><span data-stu-id="5053a-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="5053a-131">Jeśli podejrzewasz, że wystąpił więcej niż 10 000 zmian, uruchom polecenie w części podrzędnej obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="5053a-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="5053a-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5053a-132">PARAMETERS</span></span>

### <span data-ttu-id="5053a-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5053a-133">-AsJob</span></span>
<span data-ttu-id="5053a-134">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5053a-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5053a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5053a-135">-DefaultProfile</span></span>
<span data-ttu-id="5053a-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5053a-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5053a-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="5053a-137">-DirectoryPath</span></span>
<span data-ttu-id="5053a-138">Katalog, w którym zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="5053a-138">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="5053a-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5053a-139">-InputObject</span></span>
<span data-ttu-id="5053a-140">Obiekt CloudEndpoint, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="5053a-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5053a-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5053a-141">-Name</span></span>
<span data-ttu-id="5053a-142">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5053a-142">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="5053a-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5053a-143">-PassThru</span></span>
<span data-ttu-id="5053a-144">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="5053a-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5053a-145">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="5053a-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5053a-146">-Path</span><span class="sxs-lookup"><span data-stu-id="5053a-146">-Path</span></span>
<span data-ttu-id="5053a-147">Ścieżka, w której zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="5053a-147">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="5053a-148">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="5053a-148">-Recursive</span></span>
<span data-ttu-id="5053a-149">Wskazuje, czy wykrywanie zmian katalogów jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="5053a-149">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="5053a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5053a-150">-ResourceGroupName</span></span>
<span data-ttu-id="5053a-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5053a-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="5053a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5053a-152">-ResourceId</span></span>
<span data-ttu-id="5053a-153">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5053a-153">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="5053a-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5053a-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="5053a-155">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5053a-155">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5053a-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5053a-156">-SyncGroupName</span></span>
<span data-ttu-id="5053a-157">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="5053a-157">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5053a-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5053a-158">-Confirm</span></span>
<span data-ttu-id="5053a-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5053a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5053a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5053a-160">-WhatIf</span></span>
<span data-ttu-id="5053a-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5053a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5053a-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5053a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5053a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5053a-163">CommonParameters</span></span>
<span data-ttu-id="5053a-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5053a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5053a-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5053a-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5053a-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5053a-166">INPUTS</span></span>

### <span data-ttu-id="5053a-167">System. String</span><span class="sxs-lookup"><span data-stu-id="5053a-167">System.String</span></span>

### <span data-ttu-id="5053a-168">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5053a-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="5053a-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5053a-169">OUTPUTS</span></span>

### <span data-ttu-id="5053a-170">System. void</span><span class="sxs-lookup"><span data-stu-id="5053a-170">System.Void</span></span>

## <span data-ttu-id="5053a-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5053a-171">NOTES</span></span>

## <span data-ttu-id="5053a-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5053a-172">RELATED LINKS</span></span>
