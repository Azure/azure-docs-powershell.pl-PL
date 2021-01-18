---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503403"
---
# <span data-ttu-id="f85d9-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f85d9-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="f85d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f85d9-102">SYNOPSIS</span></span>
<span data-ttu-id="f85d9-103">Pobiera sznurek modułowy urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="f85d9-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="f85d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f85d9-104">SYNTAX</span></span>

### <span data-ttu-id="f85d9-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f85d9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85d9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f85d9-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85d9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f85d9-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85d9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f85d9-108">DESCRIPTION</span></span>
<span data-ttu-id="f85d9-109">Pobiera sznurek modułowy urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="f85d9-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="f85d9-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="f85d9-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="f85d9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f85d9-111">EXAMPLES</span></span>

### <span data-ttu-id="f85d9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f85d9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="f85d9-113">Zwraca obiekt typu sznurek modułu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="f85d9-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="f85d9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f85d9-114">PARAMETERS</span></span>

### <span data-ttu-id="f85d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85d9-115">-DefaultProfile</span></span>
<span data-ttu-id="f85d9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f85d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f85d9-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f85d9-117">-DeviceId</span></span>
<span data-ttu-id="f85d9-118">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="f85d9-118">Target Device Id.</span></span>

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

### <span data-ttu-id="f85d9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f85d9-119">-InputObject</span></span>
<span data-ttu-id="f85d9-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="f85d9-120">IotHub object</span></span>

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

### <span data-ttu-id="f85d9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f85d9-121">-IotHubName</span></span>
<span data-ttu-id="f85d9-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="f85d9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f85d9-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f85d9-123">-ModuleId</span></span>
<span data-ttu-id="f85d9-124">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="f85d9-124">Target Module Id.</span></span>

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

### <span data-ttu-id="f85d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="f85d9-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f85d9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f85d9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f85d9-127">-ResourceId</span></span>
<span data-ttu-id="f85d9-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="f85d9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f85d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85d9-129">CommonParameters</span></span>
<span data-ttu-id="f85d9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85d9-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85d9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85d9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f85d9-132">INPUTS</span></span>

### <span data-ttu-id="f85d9-133">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f85d9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f85d9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f85d9-134">System.String</span></span>

## <span data-ttu-id="f85d9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f85d9-135">OUTPUTS</span></span>

### <span data-ttu-id="f85d9-136">Microsoft. Azure. Commands. Management. IotHub. models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f85d9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="f85d9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f85d9-137">NOTES</span></span>

## <span data-ttu-id="f85d9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f85d9-138">RELATED LINKS</span></span>
