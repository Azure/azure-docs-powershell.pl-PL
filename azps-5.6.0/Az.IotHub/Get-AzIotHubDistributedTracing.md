---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988023"
---
# <span data-ttu-id="4bfda-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="4bfda-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="4bfda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bfda-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfda-103">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="4bfda-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="4bfda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4bfda-104">SYNTAX</span></span>

### <span data-ttu-id="4bfda-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bfda-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bfda-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4bfda-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bfda-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4bfda-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bfda-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4bfda-108">DESCRIPTION</span></span>
<span data-ttu-id="4bfda-109">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="4bfda-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="4bfda-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4bfda-110">EXAMPLES</span></span>

### <span data-ttu-id="4bfda-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bfda-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="4bfda-112">Pobierz ustawienia śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="4bfda-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="4bfda-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bfda-113">PARAMETERS</span></span>

### <span data-ttu-id="4bfda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bfda-114">-DefaultProfile</span></span>
<span data-ttu-id="4bfda-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bfda-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bfda-116">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="4bfda-116">-DeviceId</span></span>
<span data-ttu-id="4bfda-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="4bfda-117">Target Device Id.</span></span>

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

### <span data-ttu-id="4bfda-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bfda-118">-InputObject</span></span>
<span data-ttu-id="4bfda-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="4bfda-119">IotHub object</span></span>

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

### <span data-ttu-id="4bfda-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4bfda-120">-IotHubName</span></span>
<span data-ttu-id="4bfda-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="4bfda-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4bfda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bfda-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bfda-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4bfda-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4bfda-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bfda-124">-ResourceId</span></span>
<span data-ttu-id="4bfda-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="4bfda-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4bfda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfda-126">CommonParameters</span></span>
<span data-ttu-id="4bfda-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bfda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfda-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bfda-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfda-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bfda-129">INPUTS</span></span>

### <span data-ttu-id="4bfda-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4bfda-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4bfda-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4bfda-131">System.String</span></span>

## <span data-ttu-id="4bfda-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bfda-132">OUTPUTS</span></span>

### <span data-ttu-id="4bfda-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="4bfda-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="4bfda-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4bfda-134">NOTES</span></span>

## <span data-ttu-id="4bfda-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bfda-135">RELATED LINKS</span></span>
