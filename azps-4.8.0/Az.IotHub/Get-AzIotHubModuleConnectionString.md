---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223886"
---
# <span data-ttu-id="26e46-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="26e46-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="26e46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26e46-102">SYNOPSIS</span></span>
<span data-ttu-id="26e46-103">Pobierz parametry połączenia z docelowym modułem urządzenia IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="26e46-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="26e46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26e46-104">SYNTAX</span></span>

### <span data-ttu-id="26e46-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26e46-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e46-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26e46-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e46-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26e46-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e46-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26e46-108">DESCRIPTION</span></span>
<span data-ttu-id="26e46-109">Lista parametrów połączenia wszystkich modułów lub określonego modułu docelowego urządzenia IoT zawartego w usłudze Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="26e46-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="26e46-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26e46-110">EXAMPLES</span></span>

### <span data-ttu-id="26e46-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26e46-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="26e46-112">Pokazywanie wszystkich modułów parametry połączenia z docelowym urządzeniem IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="26e46-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="26e46-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="26e46-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="26e46-114">Pobierz parametry połączenia z modułem pomocniczym docelowego urządzenia IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="26e46-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="26e46-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26e46-115">PARAMETERS</span></span>

### <span data-ttu-id="26e46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e46-116">-DefaultProfile</span></span>
<span data-ttu-id="26e46-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26e46-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e46-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="26e46-118">-DeviceId</span></span>
<span data-ttu-id="26e46-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="26e46-119">Target Device Id.</span></span>

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

### <span data-ttu-id="26e46-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26e46-120">-InputObject</span></span>
<span data-ttu-id="26e46-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="26e46-121">IotHub object</span></span>

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

### <span data-ttu-id="26e46-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="26e46-122">-IotHubName</span></span>
<span data-ttu-id="26e46-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="26e46-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="26e46-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="26e46-124">-KeyType</span></span>
<span data-ttu-id="26e46-125">Typ klucza zasad dostępu współdzielonego dla uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="26e46-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="26e46-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="26e46-126">-ModuleId</span></span>
<span data-ttu-id="26e46-127">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="26e46-127">Target Module Id.</span></span>

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

### <span data-ttu-id="26e46-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e46-128">-ResourceGroupName</span></span>
<span data-ttu-id="26e46-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26e46-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="26e46-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e46-130">-ResourceId</span></span>
<span data-ttu-id="26e46-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="26e46-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="26e46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e46-132">CommonParameters</span></span>
<span data-ttu-id="26e46-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e46-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e46-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e46-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26e46-135">INPUTS</span></span>

### <span data-ttu-id="26e46-136">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="26e46-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="26e46-137">System. String</span><span class="sxs-lookup"><span data-stu-id="26e46-137">System.String</span></span>

## <span data-ttu-id="26e46-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26e46-138">OUTPUTS</span></span>

### <span data-ttu-id="26e46-139">Microsoft. Azure. Commands. Management. IotHub. models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="26e46-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="26e46-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26e46-140">NOTES</span></span>

## <span data-ttu-id="26e46-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26e46-141">RELATED LINKS</span></span>
