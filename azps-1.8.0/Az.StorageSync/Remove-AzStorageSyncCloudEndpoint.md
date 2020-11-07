---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 2d9ad2417041f39ea43f48813310869f1ea7f353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707448"
---
# <span data-ttu-id="563fa-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="563fa-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="563fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="563fa-102">SYNOPSIS</span></span>
<span data-ttu-id="563fa-103">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="563fa-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="563fa-104">Bez co najmniej jednego punktu końcowego w chmurze nie można zsynchronizować innych punktów końcowych serwera w tej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="563fa-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="563fa-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="563fa-105">SYNTAX</span></span>

### <span data-ttu-id="563fa-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="563fa-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="563fa-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="563fa-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="563fa-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="563fa-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="563fa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="563fa-109">DESCRIPTION</span></span>
<span data-ttu-id="563fa-110">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="563fa-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="563fa-111">Usługa Azure File Share odwołania do punktów końcowych w chmurze pozostaną nienaruszone przez ten proces.</span><span class="sxs-lookup"><span data-stu-id="563fa-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="563fa-112">To polecenie jest przeznaczone tylko do likwidacji.</span><span class="sxs-lookup"><span data-stu-id="563fa-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="563fa-113">Usunięcie punktu końcowego w chmurze jest operacją niszczącą.</span><span class="sxs-lookup"><span data-stu-id="563fa-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="563fa-114">Punkty końcowe serwera nie mogą być synchronizowane bez co najmniej jednego punktu końcowego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="563fa-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="563fa-115">Nie należy wykonywać tej operacji, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="563fa-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="563fa-116">Jeśli ten udział plików w usłudze Azure zostanie dodany ponownie do tej samej grupy synchronizacji, w ramach punktu końcowego w chmurze, może on powodować konflikty z plikami i inne niezamierzone konsekwencje.</span><span class="sxs-lookup"><span data-stu-id="563fa-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="563fa-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="563fa-117">EXAMPLES</span></span>

### <span data-ttu-id="563fa-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="563fa-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="563fa-119">To polecenie spowoduje usunięcie punktu końcowego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="563fa-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="563fa-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="563fa-120">PARAMETERS</span></span>

### <span data-ttu-id="563fa-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="563fa-121">-AsJob</span></span>
<span data-ttu-id="563fa-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="563fa-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="563fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563fa-123">-DefaultProfile</span></span>
<span data-ttu-id="563fa-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="563fa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563fa-125">-Force</span><span class="sxs-lookup"><span data-stu-id="563fa-125">-Force</span></span>
<span data-ttu-id="563fa-126">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="563fa-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="563fa-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="563fa-127">-InputObject</span></span>
<span data-ttu-id="563fa-128">Obiekt wejściowy CloudEndpoint, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="563fa-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="563fa-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="563fa-129">-Name</span></span>
<span data-ttu-id="563fa-130">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="563fa-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="563fa-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="563fa-131">-PassThru</span></span>
<span data-ttu-id="563fa-132">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="563fa-132">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="563fa-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="563fa-133">-ResourceGroupName</span></span>
<span data-ttu-id="563fa-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="563fa-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="563fa-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="563fa-135">-ResourceId</span></span>
<span data-ttu-id="563fa-136">Identyfikator zasobu CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="563fa-136">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="563fa-137">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="563fa-137">-StorageSyncServiceName</span></span>
<span data-ttu-id="563fa-138">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="563fa-138">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="563fa-139">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="563fa-139">-SyncGroupName</span></span>
<span data-ttu-id="563fa-140">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="563fa-140">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="563fa-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="563fa-141">-Confirm</span></span>
<span data-ttu-id="563fa-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="563fa-142">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="563fa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="563fa-143">-WhatIf</span></span>
<span data-ttu-id="563fa-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="563fa-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="563fa-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="563fa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="563fa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563fa-146">CommonParameters</span></span>
<span data-ttu-id="563fa-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="563fa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563fa-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563fa-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563fa-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="563fa-149">INPUTS</span></span>

### <span data-ttu-id="563fa-150">Microsoft. Azure. Commands. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="563fa-150">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="563fa-151">System. String</span><span class="sxs-lookup"><span data-stu-id="563fa-151">System.String</span></span>

## <span data-ttu-id="563fa-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="563fa-152">OUTPUTS</span></span>

### <span data-ttu-id="563fa-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="563fa-153">System.Object</span></span>
## <span data-ttu-id="563fa-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="563fa-154">NOTES</span></span>

## <span data-ttu-id="563fa-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="563fa-155">RELATED LINKS</span></span>