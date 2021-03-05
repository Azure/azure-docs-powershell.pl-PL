---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988030"
---
# <span data-ttu-id="718a9-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="718a9-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="718a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718a9-102">SYNOPSIS</span></span>
<span data-ttu-id="718a9-103">Pobiera urządzenie.</span><span class="sxs-lookup"><span data-stu-id="718a9-103">Gets a device twin.</span></span>

## <span data-ttu-id="718a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="718a9-104">SYNTAX</span></span>

### <span data-ttu-id="718a9-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="718a9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="718a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="718a9-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="718a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="718a9-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="718a9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="718a9-108">DESCRIPTION</span></span>
<span data-ttu-id="718a9-109">Pobiera urządzenie.</span><span class="sxs-lookup"><span data-stu-id="718a9-109">Gets a device twin.</span></span> <span data-ttu-id="718a9-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="718a9-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="718a9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="718a9-111">EXAMPLES</span></span>

### <span data-ttu-id="718a9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="718a9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="718a9-113">Zwraca obiekt device object.</span><span class="sxs-lookup"><span data-stu-id="718a9-113">Returns the device twin object.</span></span>

## <span data-ttu-id="718a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718a9-114">PARAMETERS</span></span>

### <span data-ttu-id="718a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718a9-115">-DefaultProfile</span></span>
<span data-ttu-id="718a9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="718a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718a9-117">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="718a9-117">-DeviceId</span></span>
<span data-ttu-id="718a9-118">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="718a9-118">Target Device Id.</span></span>

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

### <span data-ttu-id="718a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="718a9-119">-InputObject</span></span>
<span data-ttu-id="718a9-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="718a9-120">IotHub object</span></span>

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

### <span data-ttu-id="718a9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="718a9-121">-IotHubName</span></span>
<span data-ttu-id="718a9-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="718a9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="718a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="718a9-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="718a9-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="718a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="718a9-125">-ResourceId</span></span>
<span data-ttu-id="718a9-126">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="718a9-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="718a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718a9-127">CommonParameters</span></span>
<span data-ttu-id="718a9-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718a9-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718a9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718a9-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="718a9-130">INPUTS</span></span>

### <span data-ttu-id="718a9-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="718a9-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="718a9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="718a9-132">System.String</span></span>

## <span data-ttu-id="718a9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="718a9-133">OUTPUTS</span></span>

### <span data-ttu-id="718a9-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="718a9-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="718a9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="718a9-135">NOTES</span></span>

## <span data-ttu-id="718a9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="718a9-136">RELATED LINKS</span></span>
