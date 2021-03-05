---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011418"
---
# <span data-ttu-id="d99f9-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d99f9-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="d99f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d99f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d99f9-103">To polecenie tworzy punkt końcowy chmury synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d99f9-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="d99f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d99f9-104">SYNTAX</span></span>

### <span data-ttu-id="d99f9-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d99f9-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d99f9-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d99f9-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d99f9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d99f9-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d99f9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d99f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d99f9-109">To polecenie tworzy punkt końcowy chmury synchronizacji plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d99f9-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="d99f9-110">Punkt końcowy chmury jest odwołaniem do istniejącego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d99f9-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="d99f9-111">Reprezentuje on udział plików i definiuje jego udział w synchronizacji wszystkich plików w grupie synchronizacji, w których utworzono punkt końcowy w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d99f9-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="d99f9-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d99f9-112">EXAMPLES</span></span>

### <span data-ttu-id="d99f9-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d99f9-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="d99f9-114">Punkt końcowy chmury jest integralnym elementem grupy synchronizacji. Jest to przykład tworzenia punktu wewnątrz istniejącej grupy synchronizacji o nazwie "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="d99f9-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="d99f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d99f9-115">PARAMETERS</span></span>

### <span data-ttu-id="d99f9-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d99f9-116">-AsJob</span></span>
<span data-ttu-id="d99f9-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d99f9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d99f9-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="d99f9-118">-AzureFileShareName</span></span>
<span data-ttu-id="d99f9-119">Nazwa udziału konta magazynu (nazwa udziału plików platformy Azure)</span><span class="sxs-lookup"><span data-stu-id="d99f9-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99f9-120">-DefaultProfile</span></span>
<span data-ttu-id="d99f9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d99f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d99f9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d99f9-122">-Name</span></span>
<span data-ttu-id="d99f9-123">Nazwa punktu końcowego chmury.</span><span class="sxs-lookup"><span data-stu-id="d99f9-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="d99f9-124">Po utworzeniu za pośrednictwem portalu Azure nazwa jest ustawiana jako nazwa pliku platformy Azure, do których się odwołuje.</span><span class="sxs-lookup"><span data-stu-id="d99f9-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99f9-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d99f9-125">-ParentObject</span></span>
<span data-ttu-id="d99f9-126">Obiekt SyncGroup, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="d99f9-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d99f9-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d99f9-127">-ParentResourceId</span></span>
<span data-ttu-id="d99f9-128">Identyfikator zasobu nadrzędnego grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d99f9-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="d99f9-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d99f9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="d99f9-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d99f9-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="d99f9-132">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d99f9-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99f9-133">- StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="d99f9-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="d99f9-134">Identyfikator dzierżawy konta magazynu (identyfikator katalogu firmy)</span><span class="sxs-lookup"><span data-stu-id="d99f9-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="d99f9-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d99f9-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="d99f9-136">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d99f9-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d99f9-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d99f9-137">-SyncGroupName</span></span>
<span data-ttu-id="d99f9-138">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d99f9-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d99f9-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d99f9-139">-Confirm</span></span>
<span data-ttu-id="d99f9-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d99f9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d99f9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d99f9-141">-WhatIf</span></span>
<span data-ttu-id="d99f9-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d99f9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d99f9-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d99f9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d99f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99f9-144">CommonParameters</span></span>
<span data-ttu-id="d99f9-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d99f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99f9-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99f9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99f9-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d99f9-147">INPUTS</span></span>

### <span data-ttu-id="d99f9-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d99f9-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="d99f9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d99f9-149">System.String</span></span>

## <span data-ttu-id="d99f9-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d99f9-150">OUTPUTS</span></span>

### <span data-ttu-id="d99f9-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d99f9-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="d99f9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d99f9-152">NOTES</span></span>

## <span data-ttu-id="d99f9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d99f9-153">RELATED LINKS</span></span>
