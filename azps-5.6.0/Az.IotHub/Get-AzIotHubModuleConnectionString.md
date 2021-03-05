---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987946"
---
# <span data-ttu-id="c96a5-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="c96a5-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="c96a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c96a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c96a5-103">Pobierz ciąg połączenia docelowego modułu urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="c96a5-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="c96a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c96a5-104">SYNTAX</span></span>

### <span data-ttu-id="c96a5-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c96a5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c96a5-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c96a5-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96a5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c96a5-108">DESCRIPTION</span></span>
<span data-ttu-id="c96a5-109">Lista parametrów połączenia wszystkich modułów lub określonego modułu docelowego urządzenia IoT znajdującego się w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c96a5-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="c96a5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c96a5-110">EXAMPLES</span></span>

### <span data-ttu-id="c96a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c96a5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="c96a5-112">Pokaż wszystkie moduły parametrów połączenia docelowego urządzenia IoT w Centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="c96a5-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="c96a5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c96a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="c96a5-114">Uzyskaj dodatkowe parametrów połączenia modułu docelowego urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="c96a5-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="c96a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c96a5-115">PARAMETERS</span></span>

### <span data-ttu-id="c96a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96a5-116">-DefaultProfile</span></span>
<span data-ttu-id="c96a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c96a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c96a5-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="c96a5-118">-DeviceId</span></span>
<span data-ttu-id="c96a5-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="c96a5-119">Target Device Id.</span></span>

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

### <span data-ttu-id="c96a5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c96a5-120">-InputObject</span></span>
<span data-ttu-id="c96a5-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="c96a5-121">IotHub object</span></span>

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

### <span data-ttu-id="c96a5-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c96a5-122">-IotHubName</span></span>
<span data-ttu-id="c96a5-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="c96a5-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c96a5-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c96a5-124">-KeyType</span></span>
<span data-ttu-id="c96a5-125">Typ klucza zasad dostępu udostępnionego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="c96a5-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="c96a5-126">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="c96a5-126">-ModuleId</span></span>
<span data-ttu-id="c96a5-127">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="c96a5-127">Target Module Id.</span></span>

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

### <span data-ttu-id="c96a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="c96a5-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c96a5-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c96a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c96a5-130">-ResourceId</span></span>
<span data-ttu-id="c96a5-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="c96a5-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c96a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96a5-132">CommonParameters</span></span>
<span data-ttu-id="c96a5-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96a5-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96a5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96a5-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c96a5-135">INPUTS</span></span>

### <span data-ttu-id="c96a5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c96a5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c96a5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c96a5-137">System.String</span></span>

## <span data-ttu-id="c96a5-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c96a5-138">OUTPUTS</span></span>

### <span data-ttu-id="c96a5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="c96a5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="c96a5-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c96a5-140">NOTES</span></span>

## <span data-ttu-id="c96a5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c96a5-141">RELATED LINKS</span></span>
