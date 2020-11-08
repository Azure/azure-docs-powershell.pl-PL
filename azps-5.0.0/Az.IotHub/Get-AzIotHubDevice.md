---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232225"
---
# <span data-ttu-id="daefb-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="daefb-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="daefb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daefb-102">SYNOPSIS</span></span>
<span data-ttu-id="daefb-103">Wyświetla listę wszystkich urządzeń lub konkretne urządzenie zawarte w centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="daefb-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="daefb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daefb-104">SYNTAX</span></span>

### <span data-ttu-id="daefb-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="daefb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daefb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="daefb-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="daefb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="daefb-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daefb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="daefb-108">DESCRIPTION</span></span>
<span data-ttu-id="daefb-109">Uzyskaj szczegółowe informacje o urządzeniu z Centrum IoT lub Wyświetl listę wszystkich urządzeń w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="daefb-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="daefb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daefb-110">EXAMPLES</span></span>

### <span data-ttu-id="daefb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daefb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="daefb-112">Pokaż wszystkie urządzenia w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="daefb-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="daefb-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="daefb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="daefb-114">Zapoznaj się ze szczegółami dotyczącymi urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="daefb-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="daefb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daefb-115">PARAMETERS</span></span>

### <span data-ttu-id="daefb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daefb-116">-DefaultProfile</span></span>
<span data-ttu-id="daefb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="daefb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daefb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="daefb-118">-DeviceId</span></span>
<span data-ttu-id="daefb-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="daefb-119">Target Device Id.</span></span>

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

### <span data-ttu-id="daefb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="daefb-120">-InputObject</span></span>
<span data-ttu-id="daefb-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="daefb-121">IotHub object</span></span>

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

### <span data-ttu-id="daefb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="daefb-122">-IotHubName</span></span>
<span data-ttu-id="daefb-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="daefb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="daefb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daefb-124">-ResourceGroupName</span></span>
<span data-ttu-id="daefb-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="daefb-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="daefb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daefb-126">-ResourceId</span></span>
<span data-ttu-id="daefb-127">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="daefb-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="daefb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daefb-128">CommonParameters</span></span>
<span data-ttu-id="daefb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daefb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daefb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daefb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daefb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daefb-131">INPUTS</span></span>

### <span data-ttu-id="daefb-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="daefb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="daefb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="daefb-133">System.String</span></span>

## <span data-ttu-id="daefb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daefb-134">OUTPUTS</span></span>

### <span data-ttu-id="daefb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="daefb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="daefb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices []</span><span class="sxs-lookup"><span data-stu-id="daefb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="daefb-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daefb-137">NOTES</span></span>

## <span data-ttu-id="daefb-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daefb-138">RELATED LINKS</span></span>
