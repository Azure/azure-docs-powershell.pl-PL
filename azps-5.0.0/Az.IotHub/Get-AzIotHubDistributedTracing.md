---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234759"
---
# <span data-ttu-id="aa804-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="aa804-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="aa804-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa804-102">SYNOPSIS</span></span>
<span data-ttu-id="aa804-103">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="aa804-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="aa804-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa804-104">SYNTAX</span></span>

### <span data-ttu-id="aa804-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa804-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa804-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa804-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa804-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa804-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa804-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa804-108">DESCRIPTION</span></span>
<span data-ttu-id="aa804-109">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="aa804-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="aa804-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa804-110">EXAMPLES</span></span>

### <span data-ttu-id="aa804-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa804-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="aa804-112">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="aa804-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="aa804-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa804-113">PARAMETERS</span></span>

### <span data-ttu-id="aa804-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa804-114">-DefaultProfile</span></span>
<span data-ttu-id="aa804-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa804-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa804-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="aa804-116">-DeviceId</span></span>
<span data-ttu-id="aa804-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="aa804-117">Target Device Id.</span></span>

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

### <span data-ttu-id="aa804-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa804-118">-InputObject</span></span>
<span data-ttu-id="aa804-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="aa804-119">IotHub object</span></span>

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

### <span data-ttu-id="aa804-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="aa804-120">-IotHubName</span></span>
<span data-ttu-id="aa804-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="aa804-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aa804-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa804-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa804-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa804-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa804-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa804-124">-ResourceId</span></span>
<span data-ttu-id="aa804-125">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="aa804-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aa804-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa804-126">CommonParameters</span></span>
<span data-ttu-id="aa804-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa804-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa804-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa804-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa804-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa804-129">INPUTS</span></span>

### <span data-ttu-id="aa804-130">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aa804-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aa804-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aa804-131">System.String</span></span>

## <span data-ttu-id="aa804-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa804-132">OUTPUTS</span></span>

### <span data-ttu-id="aa804-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="aa804-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="aa804-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa804-134">NOTES</span></span>

## <span data-ttu-id="aa804-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa804-135">RELATED LINKS</span></span>
