---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341458"
---
# <span data-ttu-id="0be09-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="0be09-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="0be09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0be09-102">SYNOPSIS</span></span>
<span data-ttu-id="0be09-103">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="0be09-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="0be09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0be09-104">SYNTAX</span></span>

### <span data-ttu-id="0be09-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0be09-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be09-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0be09-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be09-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0be09-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be09-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0be09-108">DESCRIPTION</span></span>
<span data-ttu-id="0be09-109">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="0be09-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="0be09-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0be09-110">EXAMPLES</span></span>

### <span data-ttu-id="0be09-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0be09-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="0be09-112">Uzyskaj ustawienia śledzenia rozproszone dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="0be09-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="0be09-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0be09-113">PARAMETERS</span></span>

### <span data-ttu-id="0be09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be09-114">-DefaultProfile</span></span>
<span data-ttu-id="0be09-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0be09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be09-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0be09-116">-DeviceId</span></span>
<span data-ttu-id="0be09-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="0be09-117">Target Device Id.</span></span>

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

### <span data-ttu-id="0be09-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0be09-118">-InputObject</span></span>
<span data-ttu-id="0be09-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="0be09-119">IotHub object</span></span>

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

### <span data-ttu-id="0be09-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0be09-120">-IotHubName</span></span>
<span data-ttu-id="0be09-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="0be09-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0be09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be09-122">-ResourceGroupName</span></span>
<span data-ttu-id="0be09-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0be09-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0be09-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0be09-124">-ResourceId</span></span>
<span data-ttu-id="0be09-125">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="0be09-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0be09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be09-126">CommonParameters</span></span>
<span data-ttu-id="0be09-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be09-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be09-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be09-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0be09-129">INPUTS</span></span>

### <span data-ttu-id="0be09-130">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0be09-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0be09-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0be09-131">System.String</span></span>

## <span data-ttu-id="0be09-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0be09-132">OUTPUTS</span></span>

### <span data-ttu-id="0be09-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="0be09-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="0be09-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0be09-134">NOTES</span></span>

## <span data-ttu-id="0be09-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0be09-135">RELATED LINKS</span></span>
