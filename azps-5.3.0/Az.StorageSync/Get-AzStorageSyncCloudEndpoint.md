---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375930"
---
# <span data-ttu-id="94a48-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="94a48-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="94a48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94a48-102">SYNOPSIS</span></span>
<span data-ttu-id="94a48-103">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="94a48-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="94a48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94a48-104">SYNTAX</span></span>

### <span data-ttu-id="94a48-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94a48-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a48-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a48-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a48-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a48-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94a48-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94a48-108">DESCRIPTION</span></span>
<span data-ttu-id="94a48-109">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="94a48-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="94a48-110">Za pomocą tej funkcji można również wyświetlić listę atrybutów każdego punktu końcowego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="94a48-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="94a48-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94a48-111">EXAMPLES</span></span>

### <span data-ttu-id="94a48-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94a48-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="94a48-113">To polecenie pobiera wszystkie chmury punktów końcowych zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="94a48-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="94a48-114">Określ — CloudEndpointName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="94a48-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="94a48-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94a48-115">PARAMETERS</span></span>

### <span data-ttu-id="94a48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a48-116">-DefaultProfile</span></span>
<span data-ttu-id="94a48-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94a48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a48-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94a48-118">-Name</span></span>
<span data-ttu-id="94a48-119">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="94a48-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a48-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="94a48-120">-ParentObject</span></span>
<span data-ttu-id="94a48-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="94a48-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="94a48-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="94a48-122">-ParentResourceId</span></span>
<span data-ttu-id="94a48-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="94a48-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="94a48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a48-124">-ResourceGroupName</span></span>
<span data-ttu-id="94a48-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94a48-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a48-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="94a48-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="94a48-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="94a48-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a48-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="94a48-128">-SyncGroupName</span></span>
<span data-ttu-id="94a48-129">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="94a48-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a48-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a48-130">CommonParameters</span></span>
<span data-ttu-id="94a48-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a48-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a48-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a48-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a48-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94a48-133">INPUTS</span></span>

### <span data-ttu-id="94a48-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94a48-134">System.String</span></span>

### <span data-ttu-id="94a48-135">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="94a48-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="94a48-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94a48-136">OUTPUTS</span></span>

### <span data-ttu-id="94a48-137">Microsoft. Azure. Commands. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="94a48-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="94a48-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94a48-138">NOTES</span></span>

## <span data-ttu-id="94a48-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94a48-139">RELATED LINKS</span></span>
