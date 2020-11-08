---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051966"
---
# <span data-ttu-id="39184-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="39184-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="39184-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39184-102">SYNOPSIS</span></span>
<span data-ttu-id="39184-103">Uzyskaj parametry połączenia z docelowym urządzeniem IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="39184-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="39184-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39184-104">SYNTAX</span></span>

### <span data-ttu-id="39184-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39184-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39184-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39184-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39184-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="39184-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39184-108">Opis</span><span class="sxs-lookup"><span data-stu-id="39184-108">DESCRIPTION</span></span>
<span data-ttu-id="39184-109">Lista parametrów połączenia z wszystkimi urządzeniami lub docelowym urządzeniem IoT zawartym w centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="39184-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="39184-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39184-110">EXAMPLES</span></span>

### <span data-ttu-id="39184-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39184-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="39184-112">Pokazywanie wszystkich urządzeń parametry połączenia w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="39184-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="39184-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="39184-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="39184-114">Pobierz dodatkowe parametry połączenia z urządzeniem IoT.</span><span class="sxs-lookup"><span data-stu-id="39184-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="39184-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39184-115">PARAMETERS</span></span>

### <span data-ttu-id="39184-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39184-116">-DefaultProfile</span></span>
<span data-ttu-id="39184-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39184-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39184-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="39184-118">-DeviceId</span></span>
<span data-ttu-id="39184-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="39184-119">Target Device Id.</span></span>

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

### <span data-ttu-id="39184-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39184-120">-InputObject</span></span>
<span data-ttu-id="39184-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="39184-121">IotHub object</span></span>

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

### <span data-ttu-id="39184-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="39184-122">-IotHubName</span></span>
<span data-ttu-id="39184-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="39184-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="39184-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="39184-124">-KeyType</span></span>
<span data-ttu-id="39184-125">Typ klucza zasad dostępu współdzielonego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="39184-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39184-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39184-126">-ResourceGroupName</span></span>
<span data-ttu-id="39184-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="39184-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="39184-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39184-128">-ResourceId</span></span>
<span data-ttu-id="39184-129">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="39184-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="39184-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39184-130">CommonParameters</span></span>
<span data-ttu-id="39184-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39184-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39184-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39184-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39184-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39184-133">INPUTS</span></span>

### <span data-ttu-id="39184-134">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="39184-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="39184-135">System. String</span><span class="sxs-lookup"><span data-stu-id="39184-135">System.String</span></span>

## <span data-ttu-id="39184-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39184-136">OUTPUTS</span></span>

### <span data-ttu-id="39184-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="39184-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="39184-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39184-138">NOTES</span></span>

## <span data-ttu-id="39184-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39184-139">RELATED LINKS</span></span>
