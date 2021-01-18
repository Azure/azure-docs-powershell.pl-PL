---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503407"
---
# <span data-ttu-id="38fb9-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="38fb9-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="38fb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="38fb9-103">Zapoznaj się z informacjami na temat modułu urządzenia IoT lub modułów list znajdujących się na urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="38fb9-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38fb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38fb9-104">SYNTAX</span></span>

### <span data-ttu-id="38fb9-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38fb9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38fb9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38fb9-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38fb9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38fb9-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38fb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="38fb9-108">DESCRIPTION</span></span>
<span data-ttu-id="38fb9-109">Zapoznaj się z informacjami na temat modułu urządzenia IoT lub modułów list znajdujących się na urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="38fb9-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38fb9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38fb9-110">EXAMPLES</span></span>

### <span data-ttu-id="38fb9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38fb9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="38fb9-112">Zapoznaj się z informacjami dotyczącymi modułu urządzenia IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="38fb9-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="38fb9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="38fb9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="38fb9-114">Pokaż wszystkie moduły zlokalizowane na urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="38fb9-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38fb9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38fb9-115">PARAMETERS</span></span>

### <span data-ttu-id="38fb9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fb9-116">-DefaultProfile</span></span>
<span data-ttu-id="38fb9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38fb9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38fb9-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="38fb9-118">-DeviceId</span></span>
<span data-ttu-id="38fb9-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="38fb9-119">Target Device Id.</span></span>

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

### <span data-ttu-id="38fb9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38fb9-120">-InputObject</span></span>
<span data-ttu-id="38fb9-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="38fb9-121">IotHub object</span></span>

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

### <span data-ttu-id="38fb9-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="38fb9-122">-IotHubName</span></span>
<span data-ttu-id="38fb9-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="38fb9-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="38fb9-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="38fb9-124">-ModuleId</span></span>
<span data-ttu-id="38fb9-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="38fb9-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38fb9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fb9-126">-ResourceGroupName</span></span>
<span data-ttu-id="38fb9-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="38fb9-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38fb9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38fb9-128">-ResourceId</span></span>
<span data-ttu-id="38fb9-129">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="38fb9-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="38fb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fb9-130">CommonParameters</span></span>
<span data-ttu-id="38fb9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fb9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38fb9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fb9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38fb9-133">INPUTS</span></span>

### <span data-ttu-id="38fb9-134">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="38fb9-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="38fb9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="38fb9-135">System.String</span></span>

## <span data-ttu-id="38fb9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38fb9-136">OUTPUTS</span></span>

### <span data-ttu-id="38fb9-137">Microsoft. Azure. Commands. Management. IotHub. models. PSModule</span><span class="sxs-lookup"><span data-stu-id="38fb9-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="38fb9-138">Microsoft. Azure. Commands. Management. IotHub. models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="38fb9-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="38fb9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38fb9-139">NOTES</span></span>

## <span data-ttu-id="38fb9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38fb9-140">RELATED LINKS</span></span>
