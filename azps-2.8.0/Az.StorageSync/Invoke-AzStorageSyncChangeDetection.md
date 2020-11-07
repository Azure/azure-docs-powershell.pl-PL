---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888306"
---
# <span data-ttu-id="dcc27-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="dcc27-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="dcc27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcc27-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc27-103">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="dcc27-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="dcc27-104">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="dcc27-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="dcc27-105">Można wykryć maksymalnie 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="dcc27-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="dcc27-106">Jeśli zakres zmian jest dla Ciebie znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="dcc27-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="dcc27-107">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcc27-107">SYNTAX</span></span>

### <span data-ttu-id="dcc27-108">StringAndDirectoryParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcc27-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc27-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc27-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc27-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc27-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc27-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc27-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc27-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc27-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc27-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc27-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc27-114">Opis</span><span class="sxs-lookup"><span data-stu-id="dcc27-114">DESCRIPTION</span></span>
<span data-ttu-id="dcc27-115">Usługa Azure File Sync sprawdza okresowo obszar nazw w ramach synchronizowania udziału plików platformy Azure na potrzeby zmian, które zostały udostępnione do udziału plików w inny sposób niż synchronizacja. Celem jest zidentyfikowanie tych zmian, a następnie zsynchronizowanie ich z serwerami podłączonymi.</span><span class="sxs-lookup"><span data-stu-id="dcc27-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="dcc27-116">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="dcc27-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="dcc27-117">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="dcc27-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="dcc27-118">Jeśli zakres zmian jest dla Ciebie znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="dcc27-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="dcc27-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcc27-119">EXAMPLES</span></span>

### <span data-ttu-id="dcc27-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcc27-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="dcc27-121">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w katalogach "dane" i "Reporting\Templates" w katalogu synchronizowanym udziale plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc27-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="dcc27-122">Wszystkie ścieżki są powiązane z głównym obszarem nazw udziału plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc27-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="dcc27-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dcc27-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="dcc27-124">W tym przykładzie funkcja wykrywania zmian jest uruchamiana w przypadku zestawu plików, które są znane identyfikatorowi rozmówcy polecenia.</span><span class="sxs-lookup"><span data-stu-id="dcc27-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="dcc27-125">Celem jest również wykrycie i zsynchronizowanie tych zmian przez synchronizację plików Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc27-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="dcc27-126">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dcc27-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="dcc27-127">W tym przykładzie funkcja wykrywania zmian jest uruchamiana dla katalogu "Przykłady" i rekursywnie wykrywa zmiany w podkatalogach.</span><span class="sxs-lookup"><span data-stu-id="dcc27-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="dcc27-128">Pamiętaj, że to polecenie może wykryć do 10 000 zmian, zanim zostanie automatycznie przerwane.</span><span class="sxs-lookup"><span data-stu-id="dcc27-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="dcc27-129">Jeśli podejrzewasz, że wystąpił więcej niż 10 000 zmian, uruchom polecenie w części podrzędnej obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="dcc27-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="dcc27-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcc27-130">PARAMETERS</span></span>

### <span data-ttu-id="dcc27-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcc27-131">-AsJob</span></span>
<span data-ttu-id="dcc27-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dcc27-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcc27-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc27-133">-DefaultProfile</span></span>
<span data-ttu-id="dcc27-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc27-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc27-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="dcc27-135">-DirectoryPath</span></span>
<span data-ttu-id="dcc27-136">Katalog, w którym zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="dcc27-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="dcc27-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dcc27-137">-InputObject</span></span>
<span data-ttu-id="dcc27-138">Obiekt CloudEndpoint, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="dcc27-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dcc27-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcc27-139">-Name</span></span>
<span data-ttu-id="dcc27-140">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dcc27-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="dcc27-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcc27-141">-PassThru</span></span>
<span data-ttu-id="dcc27-142">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="dcc27-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="dcc27-143">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="dcc27-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="dcc27-144">-Path</span><span class="sxs-lookup"><span data-stu-id="dcc27-144">-Path</span></span>
<span data-ttu-id="dcc27-145">Ścieżka, w której zostanie przeprowadzone wykrywanie zmian.</span><span class="sxs-lookup"><span data-stu-id="dcc27-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="dcc27-146">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="dcc27-146">-Recursive</span></span>
<span data-ttu-id="dcc27-147">Wskazuje, czy wykrywanie zmian katalogów jest cykliczne.</span><span class="sxs-lookup"><span data-stu-id="dcc27-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="dcc27-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc27-148">-ResourceGroupName</span></span>
<span data-ttu-id="dcc27-149">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcc27-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="dcc27-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc27-150">-ResourceId</span></span>
<span data-ttu-id="dcc27-151">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcc27-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="dcc27-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dcc27-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="dcc27-153">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dcc27-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dcc27-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc27-154">-SyncGroupName</span></span>
<span data-ttu-id="dcc27-155">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="dcc27-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="dcc27-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcc27-156">-Confirm</span></span>
<span data-ttu-id="dcc27-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc27-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcc27-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc27-158">-WhatIf</span></span>
<span data-ttu-id="dcc27-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc27-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc27-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcc27-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcc27-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc27-161">CommonParameters</span></span>
<span data-ttu-id="dcc27-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc27-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc27-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc27-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc27-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcc27-164">INPUTS</span></span>

### <span data-ttu-id="dcc27-165">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc27-165">System.String</span></span>

### <span data-ttu-id="dcc27-166">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcc27-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="dcc27-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcc27-167">OUTPUTS</span></span>

### <span data-ttu-id="dcc27-168">System. void</span><span class="sxs-lookup"><span data-stu-id="dcc27-168">System.Void</span></span>

## <span data-ttu-id="dcc27-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcc27-169">NOTES</span></span>

## <span data-ttu-id="dcc27-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcc27-170">RELATED LINKS</span></span>
