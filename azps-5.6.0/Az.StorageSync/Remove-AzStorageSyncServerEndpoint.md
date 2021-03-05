---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: ed0f21c7a3ad2105073cb81a8dff174d201f96ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974026"
---
# <span data-ttu-id="48689-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="48689-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="48689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48689-102">SYNOPSIS</span></span>
<span data-ttu-id="48689-103">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="48689-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="48689-104">Synchronizacja z tą lokalizacją zostanie zatrzymana natychmiast.</span><span class="sxs-lookup"><span data-stu-id="48689-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="48689-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48689-105">SYNTAX</span></span>

### <span data-ttu-id="48689-106">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="48689-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48689-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48689-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48689-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48689-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48689-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="48689-109">DESCRIPTION</span></span>
<span data-ttu-id="48689-110">Usunięcie punktu końcowego serwera jest operacją szkodliwej.</span><span class="sxs-lookup"><span data-stu-id="48689-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="48689-111">Ta lokalizacja serwera zatrzyma synchronizację.</span><span class="sxs-lookup"><span data-stu-id="48689-111">This server location will stop syncing.</span></span> <span data-ttu-id="48689-112">Tej operacji nie należy wykonywać, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="48689-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="48689-113">Jeśli ta lokalizacja serwera (w tym pliki) zostanie ponownie dodana do tej samej grupy synchronizacji, co punkt końcowy serwera, może to prowadzić do konfliktu plików i innych niezamierzonych konsekwencji.</span><span class="sxs-lookup"><span data-stu-id="48689-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="48689-114">To polecenie jest przeznaczone tylko do zlikwidowania.</span><span class="sxs-lookup"><span data-stu-id="48689-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="48689-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48689-115">EXAMPLES</span></span>

### <span data-ttu-id="48689-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48689-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="48689-117">To polecenie spowoduje usunięcie punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="48689-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="48689-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48689-118">PARAMETERS</span></span>

### <span data-ttu-id="48689-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="48689-119">-AsJob</span></span>
<span data-ttu-id="48689-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="48689-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48689-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48689-121">-DefaultProfile</span></span>
<span data-ttu-id="48689-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48689-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48689-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="48689-123">-Force</span></span>
<span data-ttu-id="48689-124">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="48689-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="48689-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48689-125">-InputObject</span></span>
<span data-ttu-id="48689-126">Obiekt wejściowy ServerEndpoint, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="48689-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48689-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48689-127">-Name</span></span>
<span data-ttu-id="48689-128">Nazwa serweraEndpoint.</span><span class="sxs-lookup"><span data-stu-id="48689-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48689-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48689-129">-PassThru</span></span>
<span data-ttu-id="48689-130">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="48689-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="48689-131">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="48689-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="48689-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48689-132">-ResourceGroupName</span></span>
<span data-ttu-id="48689-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48689-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="48689-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48689-134">-ResourceId</span></span>
<span data-ttu-id="48689-135">Identyfikator zasobu Programu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="48689-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="48689-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="48689-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="48689-137">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="48689-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48689-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="48689-138">-SyncGroupName</span></span>
<span data-ttu-id="48689-139">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="48689-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48689-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48689-140">-Confirm</span></span>
<span data-ttu-id="48689-141">Przed uruchomieniem polecenia cmdlet jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48689-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48689-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48689-142">-WhatIf</span></span>
<span data-ttu-id="48689-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48689-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48689-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48689-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48689-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48689-145">CommonParameters</span></span>
<span data-ttu-id="48689-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48689-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48689-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48689-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48689-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48689-148">INPUTS</span></span>

### <span data-ttu-id="48689-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="48689-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="48689-150">System.String</span><span class="sxs-lookup"><span data-stu-id="48689-150">System.String</span></span>

## <span data-ttu-id="48689-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48689-151">OUTPUTS</span></span>

### <span data-ttu-id="48689-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="48689-152">System.Object</span></span>
## <span data-ttu-id="48689-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48689-153">NOTES</span></span>

## <span data-ttu-id="48689-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48689-154">RELATED LINKS</span></span>
