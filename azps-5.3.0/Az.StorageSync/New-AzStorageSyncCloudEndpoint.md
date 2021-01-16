---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375874"
---
# <span data-ttu-id="3d278-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d278-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="3d278-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d278-102">SYNOPSIS</span></span>
<span data-ttu-id="3d278-103">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3d278-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="3d278-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d278-104">SYNTAX</span></span>

### <span data-ttu-id="3d278-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3d278-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d278-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d278-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d278-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d278-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d278-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d278-108">DESCRIPTION</span></span>
<span data-ttu-id="3d278-109">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d278-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="3d278-110">Punkt końcowy w chmurze to odwołanie do istniejącego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d278-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="3d278-111">Reprezentuje udział pliku i definiuje jego uczestnictwo w synchronizowaniu wszystkich plików w grupie synchronizacja, w której został utworzony punkt końcowy w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3d278-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="3d278-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d278-112">EXAMPLES</span></span>

### <span data-ttu-id="3d278-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d278-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="3d278-114">Punkt końcowy w chmurze jest integralnym członkiem grupy synchronizacji, jest to przykład tworzenia jednej z istniejących w istniejącej grupie synchronizacji o nazwie "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="3d278-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="3d278-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d278-115">PARAMETERS</span></span>

### <span data-ttu-id="3d278-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d278-116">-AsJob</span></span>
<span data-ttu-id="3d278-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3d278-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d278-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="3d278-118">-AzureFileShareName</span></span>
<span data-ttu-id="3d278-119">Nazwa udziału konta magazynu (nazwa udziału plików Azure)</span><span class="sxs-lookup"><span data-stu-id="3d278-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="3d278-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d278-120">-DefaultProfile</span></span>
<span data-ttu-id="3d278-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d278-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d278-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d278-122">-Name</span></span>
<span data-ttu-id="3d278-123">Nazwa punktu końcowego chmury.</span><span class="sxs-lookup"><span data-stu-id="3d278-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="3d278-124">W przypadku tworzenia za pośrednictwem witryny Azure Portal nazwa jest ustawiana na nazwę z odwołaniami do udostępniania plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3d278-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="3d278-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3d278-125">-ParentObject</span></span>
<span data-ttu-id="3d278-126">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="3d278-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3d278-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3d278-127">-ParentResourceId</span></span>
<span data-ttu-id="3d278-128">Identyfikator zasobu nadrzędnego w obiekcie resync</span><span class="sxs-lookup"><span data-stu-id="3d278-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="3d278-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d278-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d278-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d278-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d278-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3d278-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="3d278-132">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3d278-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="3d278-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="3d278-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="3d278-134">Identyfikator dzierżawy konta magazynu (identyfikator katalogu firm)</span><span class="sxs-lookup"><span data-stu-id="3d278-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="3d278-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3d278-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="3d278-136">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3d278-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3d278-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3d278-137">-SyncGroupName</span></span>
<span data-ttu-id="3d278-138">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="3d278-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="3d278-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d278-139">-Confirm</span></span>
<span data-ttu-id="3d278-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d278-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d278-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d278-141">-WhatIf</span></span>
<span data-ttu-id="3d278-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d278-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d278-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d278-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d278-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d278-144">CommonParameters</span></span>
<span data-ttu-id="3d278-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d278-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d278-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d278-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d278-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d278-147">INPUTS</span></span>

### <span data-ttu-id="3d278-148">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3d278-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="3d278-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3d278-149">System.String</span></span>

## <span data-ttu-id="3d278-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d278-150">OUTPUTS</span></span>

### <span data-ttu-id="3d278-151">Microsoft. Azure. Commands. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d278-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="3d278-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d278-152">NOTES</span></span>

## <span data-ttu-id="3d278-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d278-153">RELATED LINKS</span></span>
