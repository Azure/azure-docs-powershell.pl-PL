---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185747"
---
# <span data-ttu-id="6fe90-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="6fe90-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="6fe90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe90-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe90-103">Pobierz parametrów połączenia docelowego urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="6fe90-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="6fe90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fe90-104">SYNTAX</span></span>

### <span data-ttu-id="6fe90-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6fe90-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe90-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fe90-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe90-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6fe90-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe90-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fe90-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe90-109">Lista parametrów połączenia wszystkich urządzeń lub docelowego urządzenia IoT zawartego w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6fe90-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="6fe90-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fe90-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe90-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fe90-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="6fe90-112">Pokazywanie wszystkich parametrów połączenia urządzeń w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="6fe90-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="6fe90-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6fe90-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="6fe90-114">Uzyskaj dodatkowe parametrów połączenia urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="6fe90-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="6fe90-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe90-115">PARAMETERS</span></span>

### <span data-ttu-id="6fe90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe90-116">-DefaultProfile</span></span>
<span data-ttu-id="6fe90-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe90-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="6fe90-118">-DeviceId</span></span>
<span data-ttu-id="6fe90-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="6fe90-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6fe90-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe90-120">-InputObject</span></span>
<span data-ttu-id="6fe90-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="6fe90-121">IotHub object</span></span>

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

### <span data-ttu-id="6fe90-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6fe90-122">-IotHubName</span></span>
<span data-ttu-id="6fe90-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="6fe90-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6fe90-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6fe90-124">-KeyType</span></span>
<span data-ttu-id="6fe90-125">Typ klucza zasad dostępu udostępnionego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="6fe90-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="6fe90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe90-126">-ResourceGroupName</span></span>
<span data-ttu-id="6fe90-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6fe90-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6fe90-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe90-128">-ResourceId</span></span>
<span data-ttu-id="6fe90-129">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="6fe90-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6fe90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe90-130">CommonParameters</span></span>
<span data-ttu-id="6fe90-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe90-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe90-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe90-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe90-133">INPUTS</span></span>

### <span data-ttu-id="6fe90-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6fe90-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6fe90-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6fe90-135">System.String</span></span>

## <span data-ttu-id="6fe90-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe90-136">OUTPUTS</span></span>

### <span data-ttu-id="6fe90-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="6fe90-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="6fe90-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fe90-138">NOTES</span></span>

## <span data-ttu-id="6fe90-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fe90-139">RELATED LINKS</span></span>
