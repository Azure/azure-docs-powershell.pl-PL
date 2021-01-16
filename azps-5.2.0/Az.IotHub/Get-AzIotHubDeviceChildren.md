---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329986"
---
# <span data-ttu-id="5c1cf-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5c1cf-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="5c1cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1cf-103">Drukowanie listy rozdzielonych przecinkami urządzeń podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="5c1cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c1cf-104">SYNTAX</span></span>

### <span data-ttu-id="5c1cf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c1cf-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c1cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c1cf-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c1cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c1cf-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c1cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5c1cf-108">DESCRIPTION</span></span>
<span data-ttu-id="5c1cf-109">Pokaż wszystkie przypisane urządzenia niebędące granicą jako listę rozdzielonych przecinkami wszystkich urządzeń brzegowych lub określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="5c1cf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c1cf-110">EXAMPLES</span></span>

### <span data-ttu-id="5c1cf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c1cf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="5c1cf-112">Pokaż wszystkie przypisane urządzenia niebędące granicą jako listę rozdzielaną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="5c1cf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c1cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="5c1cf-114">Pokaż wszystkie przypisane urządzenia niebędące krawędziami jako listę rozdzielonych przecinkami wszystkich urządzeń brzegowych.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="5c1cf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c1cf-115">PARAMETERS</span></span>

### <span data-ttu-id="5c1cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1cf-116">-DefaultProfile</span></span>
<span data-ttu-id="5c1cf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1cf-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5c1cf-118">-DeviceId</span></span>
<span data-ttu-id="5c1cf-119">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-119">Id of edge device.</span></span>

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

### <span data-ttu-id="5c1cf-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c1cf-120">-InputObject</span></span>
<span data-ttu-id="5c1cf-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="5c1cf-121">IotHub object</span></span>

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

### <span data-ttu-id="5c1cf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5c1cf-122">-IotHubName</span></span>
<span data-ttu-id="5c1cf-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5c1cf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5c1cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c1cf-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5c1cf-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c1cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1cf-126">-ResourceId</span></span>
<span data-ttu-id="5c1cf-127">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="5c1cf-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5c1cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1cf-128">CommonParameters</span></span>
<span data-ttu-id="5c1cf-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1cf-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1cf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1cf-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c1cf-131">INPUTS</span></span>

### <span data-ttu-id="5c1cf-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5c1cf-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5c1cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1cf-133">System.String</span></span>

## <span data-ttu-id="5c1cf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c1cf-134">OUTPUTS</span></span>

### <span data-ttu-id="5c1cf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5c1cf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="5c1cf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="5c1cf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="5c1cf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c1cf-137">NOTES</span></span>

## <span data-ttu-id="5c1cf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c1cf-138">RELATED LINKS</span></span>
