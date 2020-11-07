---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c8ace72aae518de3af27045507fb8c4cfaf72242
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887782"
---
# <span data-ttu-id="ab272-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab272-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="ab272-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab272-102">SYNOPSIS</span></span>
<span data-ttu-id="ab272-103">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="ab272-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab272-104">SYNTAX</span></span>

### <span data-ttu-id="ab272-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab272-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab272-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab272-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab272-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab272-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab272-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab272-108">DESCRIPTION</span></span>
<span data-ttu-id="ab272-109">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="ab272-110">Za pomocą tej funkcji można również wyświetlić listę atrybutów każdego punktu końcowego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ab272-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="ab272-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab272-111">EXAMPLES</span></span>

### <span data-ttu-id="ab272-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab272-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="ab272-113">To polecenie pobiera wszystkie chmury punktów końcowych zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="ab272-114">Określ — CloudEndpointName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="ab272-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="ab272-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab272-115">PARAMETERS</span></span>

### <span data-ttu-id="ab272-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab272-116">-DefaultProfile</span></span>
<span data-ttu-id="ab272-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab272-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab272-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab272-118">-Name</span></span>
<span data-ttu-id="ab272-119">Nazwa CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ab272-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="ab272-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ab272-120">-ParentObject</span></span>
<span data-ttu-id="ab272-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ab272-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ab272-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ab272-122">-ParentResourceId</span></span>
<span data-ttu-id="ab272-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ab272-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ab272-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab272-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab272-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab272-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ab272-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ab272-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ab272-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ab272-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ab272-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ab272-128">-SyncGroupName</span></span>
<span data-ttu-id="ab272-129">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="ab272-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ab272-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab272-130">CommonParameters</span></span>
<span data-ttu-id="ab272-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab272-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab272-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab272-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab272-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab272-133">INPUTS</span></span>

### <span data-ttu-id="ab272-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab272-134">System.String</span></span>

### <span data-ttu-id="ab272-135">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ab272-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ab272-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab272-136">OUTPUTS</span></span>

### <span data-ttu-id="ab272-137">Microsoft. Azure. Commands. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab272-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="ab272-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab272-138">NOTES</span></span>

## <span data-ttu-id="ab272-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab272-139">RELATED LINKS</span></span>
