---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: bacb7575f7c4bf8a29d84e507e40d45ffc69ec1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988065"
---
# <span data-ttu-id="851f1-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="851f1-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="851f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851f1-102">SYNOPSIS</span></span>
<span data-ttu-id="851f1-103">Pobierz parametrów połączenia docelowego urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="851f1-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="851f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="851f1-104">SYNTAX</span></span>

### <span data-ttu-id="851f1-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="851f1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="851f1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="851f1-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="851f1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="851f1-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="851f1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="851f1-108">DESCRIPTION</span></span>
<span data-ttu-id="851f1-109">Lista parametrów połączenia wszystkich urządzeń lub docelowego urządzenia IoT zawartego w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="851f1-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="851f1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="851f1-110">EXAMPLES</span></span>

### <span data-ttu-id="851f1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="851f1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="851f1-112">Pokazywanie wszystkich parametrów połączenia urządzeń w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="851f1-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="851f1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="851f1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="851f1-114">Uzyskaj dodatkowe parametrów połączenia urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="851f1-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="851f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="851f1-115">PARAMETERS</span></span>

### <span data-ttu-id="851f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851f1-116">-DefaultProfile</span></span>
<span data-ttu-id="851f1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="851f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851f1-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="851f1-118">-DeviceId</span></span>
<span data-ttu-id="851f1-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="851f1-119">Target Device Id.</span></span>

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

### <span data-ttu-id="851f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="851f1-120">-InputObject</span></span>
<span data-ttu-id="851f1-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="851f1-121">IotHub object</span></span>

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

### <span data-ttu-id="851f1-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="851f1-122">-IotHubName</span></span>
<span data-ttu-id="851f1-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="851f1-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="851f1-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="851f1-124">-KeyType</span></span>
<span data-ttu-id="851f1-125">Typ klucza zasad dostępu udostępnionego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="851f1-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="851f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="851f1-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="851f1-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="851f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="851f1-128">-ResourceId</span></span>
<span data-ttu-id="851f1-129">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="851f1-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="851f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851f1-130">CommonParameters</span></span>
<span data-ttu-id="851f1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851f1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851f1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851f1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="851f1-133">INPUTS</span></span>

### <span data-ttu-id="851f1-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="851f1-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="851f1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="851f1-135">System.String</span></span>

## <span data-ttu-id="851f1-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="851f1-136">OUTPUTS</span></span>

### <span data-ttu-id="851f1-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="851f1-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="851f1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="851f1-138">NOTES</span></span>

## <span data-ttu-id="851f1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="851f1-139">RELATED LINKS</span></span>
