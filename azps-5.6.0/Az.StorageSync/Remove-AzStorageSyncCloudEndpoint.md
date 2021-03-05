---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974074"
---
# <span data-ttu-id="227ca-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="227ca-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="227ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227ca-102">SYNOPSIS</span></span>
<span data-ttu-id="227ca-103">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="227ca-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="227ca-104">Bez co najmniej jednego punktu końcowego chmury żadne inne punkty końcowe serwera w tej grupie synchronizacji nie mogą być synchronizowane.</span><span class="sxs-lookup"><span data-stu-id="227ca-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="227ca-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="227ca-105">SYNTAX</span></span>

### <span data-ttu-id="227ca-106">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="227ca-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="227ca-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="227ca-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="227ca-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="227ca-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227ca-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="227ca-109">DESCRIPTION</span></span>
<span data-ttu-id="227ca-110">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="227ca-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="227ca-111">Ten proces nie dotyczy plików platformy Azure, które współużytkuje odwołania do punktów końcowych w chmurze.</span><span class="sxs-lookup"><span data-stu-id="227ca-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="227ca-112">To polecenie jest przeznaczone tylko do zlikwidowania.</span><span class="sxs-lookup"><span data-stu-id="227ca-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="227ca-113">Usunięcie punktu końcowego w chmurze jest operacją szkodliwej.</span><span class="sxs-lookup"><span data-stu-id="227ca-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="227ca-114">Punkty końcowe serwera nie mogą być synchronizowane bez co najmniej jednego punktu końcowego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="227ca-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="227ca-115">Tej operacji nie należy wykonywać, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="227ca-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="227ca-116">Ponowne dodanie tego udziału plików platformy Azure do tej samej grupy synchronizacji jako punktu końcowego chmury może prowadzić do konfliktu plików i innych niezamierzonych konsekwencji.</span><span class="sxs-lookup"><span data-stu-id="227ca-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="227ca-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="227ca-117">EXAMPLES</span></span>

### <span data-ttu-id="227ca-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="227ca-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="227ca-119">To polecenie spowoduje usunięcie punktu końcowego chmury.</span><span class="sxs-lookup"><span data-stu-id="227ca-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="227ca-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="227ca-120">PARAMETERS</span></span>

### <span data-ttu-id="227ca-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="227ca-121">-AsJob</span></span>
<span data-ttu-id="227ca-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="227ca-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="227ca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227ca-123">-DefaultProfile</span></span>
<span data-ttu-id="227ca-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="227ca-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="227ca-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="227ca-125">-Force</span></span>
<span data-ttu-id="227ca-126">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="227ca-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="227ca-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="227ca-127">-InputObject</span></span>
<span data-ttu-id="227ca-128">Obiekt wejściowy CloudEndpoint, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="227ca-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="227ca-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="227ca-129">-Name</span></span>
<span data-ttu-id="227ca-130">Nazwa programu CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="227ca-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="227ca-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="227ca-131">-PassThru</span></span>
<span data-ttu-id="227ca-132">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="227ca-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="227ca-133">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="227ca-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="227ca-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227ca-134">-ResourceGroupName</span></span>
<span data-ttu-id="227ca-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="227ca-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="227ca-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="227ca-136">-ResourceId</span></span>
<span data-ttu-id="227ca-137">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="227ca-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="227ca-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="227ca-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="227ca-139">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="227ca-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="227ca-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="227ca-140">-SyncGroupName</span></span>
<span data-ttu-id="227ca-141">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="227ca-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="227ca-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="227ca-142">-Confirm</span></span>
<span data-ttu-id="227ca-143">Przed uruchomieniem polecenia cmdlet jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="227ca-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227ca-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227ca-144">-WhatIf</span></span>
<span data-ttu-id="227ca-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="227ca-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="227ca-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="227ca-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227ca-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227ca-147">CommonParameters</span></span>
<span data-ttu-id="227ca-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="227ca-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227ca-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="227ca-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227ca-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="227ca-150">INPUTS</span></span>

### <span data-ttu-id="227ca-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="227ca-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="227ca-152">System.String</span><span class="sxs-lookup"><span data-stu-id="227ca-152">System.String</span></span>

## <span data-ttu-id="227ca-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="227ca-153">OUTPUTS</span></span>

### <span data-ttu-id="227ca-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="227ca-154">System.Object</span></span>
## <span data-ttu-id="227ca-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="227ca-155">NOTES</span></span>

## <span data-ttu-id="227ca-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="227ca-156">RELATED LINKS</span></span>
