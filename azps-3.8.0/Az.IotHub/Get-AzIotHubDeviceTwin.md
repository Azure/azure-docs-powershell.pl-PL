---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051961"
---
# <span data-ttu-id="21053-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="21053-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="21053-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21053-102">SYNOPSIS</span></span>
<span data-ttu-id="21053-103">Pobiera sznurek urządzenia.</span><span class="sxs-lookup"><span data-stu-id="21053-103">Gets a device twin.</span></span>

## <span data-ttu-id="21053-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21053-104">SYNTAX</span></span>

### <span data-ttu-id="21053-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21053-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21053-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21053-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21053-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="21053-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21053-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21053-108">DESCRIPTION</span></span>
<span data-ttu-id="21053-109">Pobiera sznurek urządzenia.</span><span class="sxs-lookup"><span data-stu-id="21053-109">Gets a device twin.</span></span> <span data-ttu-id="21053-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="21053-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="21053-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21053-111">EXAMPLES</span></span>

### <span data-ttu-id="21053-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21053-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="21053-113">Zwraca obiekt z urządzenia z sznurem.</span><span class="sxs-lookup"><span data-stu-id="21053-113">Returns the device twin object.</span></span>

## <span data-ttu-id="21053-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21053-114">PARAMETERS</span></span>

### <span data-ttu-id="21053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21053-115">-DefaultProfile</span></span>
<span data-ttu-id="21053-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21053-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21053-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="21053-117">-DeviceId</span></span>
<span data-ttu-id="21053-118">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="21053-118">Target Device Id.</span></span>

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

### <span data-ttu-id="21053-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21053-119">-InputObject</span></span>
<span data-ttu-id="21053-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="21053-120">IotHub object</span></span>

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

### <span data-ttu-id="21053-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="21053-121">-IotHubName</span></span>
<span data-ttu-id="21053-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="21053-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="21053-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21053-123">-ResourceGroupName</span></span>
<span data-ttu-id="21053-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="21053-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="21053-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21053-125">-ResourceId</span></span>
<span data-ttu-id="21053-126">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="21053-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="21053-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21053-127">CommonParameters</span></span>
<span data-ttu-id="21053-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21053-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21053-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21053-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21053-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21053-130">INPUTS</span></span>

### <span data-ttu-id="21053-131">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="21053-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="21053-132">System. String</span><span class="sxs-lookup"><span data-stu-id="21053-132">System.String</span></span>

## <span data-ttu-id="21053-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21053-133">OUTPUTS</span></span>

### <span data-ttu-id="21053-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="21053-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="21053-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21053-135">NOTES</span></span>

## <span data-ttu-id="21053-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21053-136">RELATED LINKS</span></span>
