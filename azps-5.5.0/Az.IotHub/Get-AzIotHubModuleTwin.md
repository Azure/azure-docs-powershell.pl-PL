---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185667"
---
# <span data-ttu-id="91705-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="91705-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="91705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91705-102">SYNOPSIS</span></span>
<span data-ttu-id="91705-103">Pobiera moduł urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="91705-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="91705-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91705-104">SYNTAX</span></span>

### <span data-ttu-id="91705-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="91705-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91705-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91705-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91705-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91705-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91705-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="91705-108">DESCRIPTION</span></span>
<span data-ttu-id="91705-109">Pobiera moduł urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="91705-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="91705-110">Aby https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="91705-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="91705-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91705-111">EXAMPLES</span></span>

### <span data-ttu-id="91705-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91705-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="91705-113">Zwraca obiekt modułu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="91705-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="91705-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91705-114">PARAMETERS</span></span>

### <span data-ttu-id="91705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91705-115">-DefaultProfile</span></span>
<span data-ttu-id="91705-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91705-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91705-117">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="91705-117">-DeviceId</span></span>
<span data-ttu-id="91705-118">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="91705-118">Target Device Id.</span></span>

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

### <span data-ttu-id="91705-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91705-119">-InputObject</span></span>
<span data-ttu-id="91705-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="91705-120">IotHub object</span></span>

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

### <span data-ttu-id="91705-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="91705-121">-IotHubName</span></span>
<span data-ttu-id="91705-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="91705-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91705-123">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="91705-123">-ModuleId</span></span>
<span data-ttu-id="91705-124">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="91705-124">Target Module Id.</span></span>

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

### <span data-ttu-id="91705-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91705-125">-ResourceGroupName</span></span>
<span data-ttu-id="91705-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="91705-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91705-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91705-127">-ResourceId</span></span>
<span data-ttu-id="91705-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="91705-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="91705-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91705-129">CommonParameters</span></span>
<span data-ttu-id="91705-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91705-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91705-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91705-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91705-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91705-132">INPUTS</span></span>

### <span data-ttu-id="91705-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="91705-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="91705-134">System.String</span><span class="sxs-lookup"><span data-stu-id="91705-134">System.String</span></span>

## <span data-ttu-id="91705-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91705-135">OUTPUTS</span></span>

### <span data-ttu-id="91705-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="91705-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="91705-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91705-137">NOTES</span></span>

## <span data-ttu-id="91705-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91705-138">RELATED LINKS</span></span>
