---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188826"
---
# <span data-ttu-id="38cf6-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="38cf6-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="38cf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="38cf6-103">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="38cf6-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="38cf6-104">Synchronizacja z tą lokalizacją zostanie zatrzymana natychmiast.</span><span class="sxs-lookup"><span data-stu-id="38cf6-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="38cf6-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38cf6-105">SYNTAX</span></span>

### <span data-ttu-id="38cf6-106">StringParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="38cf6-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38cf6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38cf6-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38cf6-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38cf6-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38cf6-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="38cf6-109">DESCRIPTION</span></span>
<span data-ttu-id="38cf6-110">Usunięcie punktu końcowego serwera jest operacją szkodliwej.</span><span class="sxs-lookup"><span data-stu-id="38cf6-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="38cf6-111">Ta lokalizacja serwera zatrzyma synchronizację.</span><span class="sxs-lookup"><span data-stu-id="38cf6-111">This server location will stop syncing.</span></span> <span data-ttu-id="38cf6-112">Tej operacji nie należy wykonywać, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="38cf6-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="38cf6-113">Jeśli ta lokalizacja serwera (łącznie z plikami) zostanie ponownie dodana do tej samej grupy synchronizacji co punkt końcowy serwera, może to prowadzić do konfliktu plików i innych niezamierzonych konsekwencji.</span><span class="sxs-lookup"><span data-stu-id="38cf6-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="38cf6-114">To polecenie jest przeznaczone tylko do zlikwidowania.</span><span class="sxs-lookup"><span data-stu-id="38cf6-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="38cf6-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38cf6-115">EXAMPLES</span></span>

### <span data-ttu-id="38cf6-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38cf6-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="38cf6-117">To polecenie spowoduje usunięcie punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="38cf6-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="38cf6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38cf6-118">PARAMETERS</span></span>

### <span data-ttu-id="38cf6-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="38cf6-119">-AsJob</span></span>
<span data-ttu-id="38cf6-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="38cf6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38cf6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cf6-121">-DefaultProfile</span></span>
<span data-ttu-id="38cf6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38cf6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38cf6-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="38cf6-123">-Force</span></span>
<span data-ttu-id="38cf6-124">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="38cf6-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="38cf6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38cf6-125">-InputObject</span></span>
<span data-ttu-id="38cf6-126">Obiekt wejściowy ServerEndpoint, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="38cf6-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="38cf6-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38cf6-127">-Name</span></span>
<span data-ttu-id="38cf6-128">Nazwa serweraEndpoint.</span><span class="sxs-lookup"><span data-stu-id="38cf6-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="38cf6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38cf6-129">-PassThru</span></span>
<span data-ttu-id="38cf6-130">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="38cf6-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="38cf6-131">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="38cf6-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="38cf6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38cf6-132">-ResourceGroupName</span></span>
<span data-ttu-id="38cf6-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38cf6-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="38cf6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38cf6-134">-ResourceId</span></span>
<span data-ttu-id="38cf6-135">Identyfikator zasobu Programu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="38cf6-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="38cf6-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="38cf6-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="38cf6-137">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="38cf6-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="38cf6-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="38cf6-138">-SyncGroupName</span></span>
<span data-ttu-id="38cf6-139">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="38cf6-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="38cf6-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38cf6-140">-Confirm</span></span>
<span data-ttu-id="38cf6-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38cf6-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38cf6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38cf6-142">-WhatIf</span></span>
<span data-ttu-id="38cf6-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cf6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38cf6-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38cf6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38cf6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cf6-145">CommonParameters</span></span>
<span data-ttu-id="38cf6-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38cf6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cf6-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38cf6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cf6-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38cf6-148">INPUTS</span></span>

### <span data-ttu-id="38cf6-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="38cf6-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="38cf6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="38cf6-150">System.String</span></span>

## <span data-ttu-id="38cf6-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38cf6-151">OUTPUTS</span></span>

### <span data-ttu-id="38cf6-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="38cf6-152">System.Object</span></span>
## <span data-ttu-id="38cf6-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38cf6-153">NOTES</span></span>

## <span data-ttu-id="38cf6-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38cf6-154">RELATED LINKS</span></span>
