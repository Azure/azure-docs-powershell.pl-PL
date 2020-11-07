---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 7a8c11bc4b24415e1baf826824596bc06e1fe99a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707460"
---
# <span data-ttu-id="70486-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="70486-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="70486-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70486-102">SYNOPSIS</span></span>
<span data-ttu-id="70486-103">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="70486-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="70486-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70486-104">SYNTAX</span></span>

### <span data-ttu-id="70486-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70486-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70486-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="70486-106">StringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70486-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="70486-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70486-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70486-108">DESCRIPTION</span></span>
<span data-ttu-id="70486-109">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70486-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="70486-110">Punkt końcowy w chmurze to odwołanie do istniejącego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70486-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="70486-111">Reprezentuje udział pliku i definiuje jego uczestnictwo w synchronizowaniu wszystkich plików w grupie synchronizacja, w której został utworzony punkt końcowy w chmurze.</span><span class="sxs-lookup"><span data-stu-id="70486-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="70486-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70486-112">EXAMPLES</span></span>

### <span data-ttu-id="70486-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70486-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="70486-114">Punkt końcowy w chmurze jest integralnym członkiem grupy synchronizacji, jest to przykład tworzenia jednej z istniejących w istniejącej grupie synchronizacji o nazwie "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="70486-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="70486-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70486-115">PARAMETERS</span></span>

### <span data-ttu-id="70486-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70486-116">-AsJob</span></span>
<span data-ttu-id="70486-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70486-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70486-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70486-118">-DefaultProfile</span></span>
<span data-ttu-id="70486-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70486-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70486-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70486-120">-Name</span></span>
<span data-ttu-id="70486-121">Nazwa punktu końcowego chmury.</span><span class="sxs-lookup"><span data-stu-id="70486-121">Name of the cloud endpoint.</span></span> <span data-ttu-id="70486-122">W przypadku tworzenia za pośrednictwem witryny Azure Portal nazwa jest ustawiana na nazwę z odwołaniami do udostępniania plików w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="70486-122">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="70486-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="70486-123">-ParentObject</span></span>
<span data-ttu-id="70486-124">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="70486-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="70486-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="70486-125">-ParentResourceId</span></span>
<span data-ttu-id="70486-126">Identyfikator zasobu nadrzędnego w obiekcie resync</span><span class="sxs-lookup"><span data-stu-id="70486-126">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="70486-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70486-127">-ResourceGroupName</span></span>
<span data-ttu-id="70486-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70486-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="70486-129">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="70486-129">-StorageAccountResourceId</span></span>
<span data-ttu-id="70486-130">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="70486-130">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="70486-131">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="70486-131">-AzureFileShareName</span></span>
<span data-ttu-id="70486-132">Nazwa udziału konta magazynu (nazwa udziału plików Azure)</span><span class="sxs-lookup"><span data-stu-id="70486-132">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="70486-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="70486-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="70486-134">Identyfikator dzierżawy konta magazynu (identyfikator katalogu firm)</span><span class="sxs-lookup"><span data-stu-id="70486-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="70486-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="70486-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="70486-136">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="70486-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="70486-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="70486-137">-SyncGroupName</span></span>
<span data-ttu-id="70486-138">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="70486-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="70486-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70486-139">-Confirm</span></span>
<span data-ttu-id="70486-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70486-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70486-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70486-141">-WhatIf</span></span>
<span data-ttu-id="70486-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70486-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70486-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70486-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70486-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70486-144">CommonParameters</span></span>
<span data-ttu-id="70486-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70486-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70486-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70486-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70486-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70486-147">INPUTS</span></span>

### <span data-ttu-id="70486-148">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="70486-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="70486-149">System. String</span><span class="sxs-lookup"><span data-stu-id="70486-149">System.String</span></span>

## <span data-ttu-id="70486-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70486-150">OUTPUTS</span></span>

### <span data-ttu-id="70486-151">Microsoft. Azure. Commands. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="70486-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="70486-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70486-152">NOTES</span></span>

## <span data-ttu-id="70486-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70486-153">RELATED LINKS</span></span>