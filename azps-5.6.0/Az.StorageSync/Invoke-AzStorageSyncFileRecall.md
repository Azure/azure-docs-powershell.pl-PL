---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 4da44d6ecff7dbf6de9c0fb20f74988688e9826d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002193"
---
# <span data-ttu-id="1afdb-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="1afdb-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="1afdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1afdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1afdb-103">To polecenie przypomina wszystkie pliki warstwowe z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="1afdb-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="1afdb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1afdb-104">SYNTAX</span></span>

### <span data-ttu-id="1afdb-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1afdb-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afdb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afdb-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afdb-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afdb-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afdb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1afdb-108">DESCRIPTION</span></span>
<span data-ttu-id="1afdb-109">Gdy dla punktu końcowego serwera (określonej lokalizacji na zarejestrowanym serwerze) jest włączone warstwowanie chmury, za pomocą tego polecenia można odwołać wszystkie pliki warstwowe na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="1afdb-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="1afdb-110">Przed rozpoczęciem odwoływania zdecydowanie zalecane jest wyłączenie funkcji warstw w chmurze dla tego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="1afdb-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="1afdb-111">Jeśli wciąż trwa warstwowanie, odwoływanie może spowodować, że inne pliki zostaną warstwowe, co może okazać się chybne, aby osiągnąć cel, jaki ma zapewnić cała zawartość, która znajduje się na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="1afdb-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="1afdb-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1afdb-112">EXAMPLES</span></span>

### <span data-ttu-id="1afdb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1afdb-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="1afdb-114">To polecenie cyklicznie przypomina wszystkie pliki warstwowe znajdujące się w ścieżce głównej określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="1afdb-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="1afdb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1afdb-115">PARAMETERS</span></span>

### <span data-ttu-id="1afdb-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1afdb-116">-AsJob</span></span>
<span data-ttu-id="1afdb-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1afdb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1afdb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afdb-118">-DefaultProfile</span></span>
<span data-ttu-id="1afdb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1afdb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afdb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1afdb-120">-InputObject</span></span>
<span data-ttu-id="1afdb-121">Obiekt SyncGroup, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="1afdb-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1afdb-122">-Name</span></span>
<span data-ttu-id="1afdb-123">Nazwa serweraEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1afdb-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1afdb-124">-PassThru</span></span>
<span data-ttu-id="1afdb-125">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="1afdb-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="1afdb-126">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="1afdb-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="1afdb-127">— Deseń</span><span class="sxs-lookup"><span data-stu-id="1afdb-127">-Pattern</span></span>
<span data-ttu-id="1afdb-128">Wzorzec nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="1afdb-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="1afdb-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="1afdb-129">-RecallPath</span></span>
<span data-ttu-id="1afdb-130">Odwołaj ścieżkę, którą należy odwołać.</span><span class="sxs-lookup"><span data-stu-id="1afdb-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="1afdb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afdb-131">-ResourceGroupName</span></span>
<span data-ttu-id="1afdb-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1afdb-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1afdb-133">-ResourceId</span></span>
<span data-ttu-id="1afdb-134">Identyfikator zasobu Programu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1afdb-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1afdb-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="1afdb-136">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1afdb-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1afdb-137">-SyncGroupName</span></span>
<span data-ttu-id="1afdb-138">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1afdb-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afdb-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1afdb-139">-Confirm</span></span>
<span data-ttu-id="1afdb-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1afdb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afdb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afdb-141">-WhatIf</span></span>
<span data-ttu-id="1afdb-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1afdb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1afdb-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1afdb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afdb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afdb-144">CommonParameters</span></span>
<span data-ttu-id="1afdb-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afdb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afdb-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afdb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afdb-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1afdb-147">INPUTS</span></span>

### <span data-ttu-id="1afdb-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1afdb-148">System.String</span></span>

### <span data-ttu-id="1afdb-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1afdb-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1afdb-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1afdb-150">OUTPUTS</span></span>

### <span data-ttu-id="1afdb-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1afdb-151">System.Boolean</span></span>

## <span data-ttu-id="1afdb-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1afdb-152">NOTES</span></span>

## <span data-ttu-id="1afdb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1afdb-153">RELATED LINKS</span></span>
