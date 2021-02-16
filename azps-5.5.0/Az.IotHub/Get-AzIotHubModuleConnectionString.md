---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185675"
---
# <span data-ttu-id="97550-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="97550-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="97550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97550-102">SYNOPSIS</span></span>
<span data-ttu-id="97550-103">Pobierz ciąg połączenia docelowego modułu urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="97550-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="97550-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97550-104">SYNTAX</span></span>

### <span data-ttu-id="97550-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97550-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97550-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97550-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97550-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="97550-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97550-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="97550-108">DESCRIPTION</span></span>
<span data-ttu-id="97550-109">Lista parametrów połączenia wszystkich modułów lub określonego modułu docelowego urządzenia IoT znajdującego się w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="97550-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="97550-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97550-110">EXAMPLES</span></span>

### <span data-ttu-id="97550-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97550-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="97550-112">Pokaż wszystkie moduły parametrów połączenia docelowego urządzenia IoT w Centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="97550-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="97550-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97550-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="97550-114">Uzyskaj dodatkowe parametrów połączenia modułu docelowego urządzenia IoT w centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="97550-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="97550-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97550-115">PARAMETERS</span></span>

### <span data-ttu-id="97550-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97550-116">-DefaultProfile</span></span>
<span data-ttu-id="97550-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97550-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97550-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="97550-118">-DeviceId</span></span>
<span data-ttu-id="97550-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="97550-119">Target Device Id.</span></span>

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

### <span data-ttu-id="97550-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97550-120">-InputObject</span></span>
<span data-ttu-id="97550-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="97550-121">IotHub object</span></span>

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

### <span data-ttu-id="97550-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="97550-122">-IotHubName</span></span>
<span data-ttu-id="97550-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="97550-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="97550-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="97550-124">-KeyType</span></span>
<span data-ttu-id="97550-125">Typ klucza zasad dostępu udostępnionego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="97550-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="97550-126">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="97550-126">-ModuleId</span></span>
<span data-ttu-id="97550-127">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="97550-127">Target Module Id.</span></span>

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

### <span data-ttu-id="97550-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97550-128">-ResourceGroupName</span></span>
<span data-ttu-id="97550-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="97550-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="97550-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97550-130">-ResourceId</span></span>
<span data-ttu-id="97550-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="97550-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="97550-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97550-132">CommonParameters</span></span>
<span data-ttu-id="97550-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97550-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97550-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97550-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97550-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97550-135">INPUTS</span></span>

### <span data-ttu-id="97550-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="97550-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="97550-137">System.String</span><span class="sxs-lookup"><span data-stu-id="97550-137">System.String</span></span>

## <span data-ttu-id="97550-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97550-138">OUTPUTS</span></span>

### <span data-ttu-id="97550-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="97550-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="97550-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97550-140">NOTES</span></span>

## <span data-ttu-id="97550-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97550-141">RELATED LINKS</span></span>
