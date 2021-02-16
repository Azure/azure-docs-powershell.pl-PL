---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185715"
---
# <span data-ttu-id="130a9-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="130a9-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="130a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="130a9-102">SYNOPSIS</span></span>
<span data-ttu-id="130a9-103">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="130a9-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="130a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="130a9-104">SYNTAX</span></span>

### <span data-ttu-id="130a9-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="130a9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="130a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="130a9-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="130a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="130a9-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="130a9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="130a9-108">DESCRIPTION</span></span>
<span data-ttu-id="130a9-109">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="130a9-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="130a9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="130a9-110">EXAMPLES</span></span>

### <span data-ttu-id="130a9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="130a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="130a9-112">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="130a9-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="130a9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="130a9-113">PARAMETERS</span></span>

### <span data-ttu-id="130a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130a9-114">-DefaultProfile</span></span>
<span data-ttu-id="130a9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="130a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="130a9-116">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="130a9-116">-DeviceId</span></span>
<span data-ttu-id="130a9-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="130a9-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="130a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="130a9-118">-InputObject</span></span>
<span data-ttu-id="130a9-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="130a9-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="130a9-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="130a9-120">-IotHubName</span></span>
<span data-ttu-id="130a9-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="130a9-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="130a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="130a9-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="130a9-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="130a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="130a9-124">-ResourceId</span></span>
<span data-ttu-id="130a9-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="130a9-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="130a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130a9-126">CommonParameters</span></span>
<span data-ttu-id="130a9-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="130a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130a9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="130a9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130a9-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="130a9-129">INPUTS</span></span>

### <span data-ttu-id="130a9-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="130a9-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="130a9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="130a9-131">System.String</span></span>

## <span data-ttu-id="130a9-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="130a9-132">OUTPUTS</span></span>

### <span data-ttu-id="130a9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="130a9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="130a9-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="130a9-134">NOTES</span></span>

## <span data-ttu-id="130a9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="130a9-135">RELATED LINKS</span></span>
