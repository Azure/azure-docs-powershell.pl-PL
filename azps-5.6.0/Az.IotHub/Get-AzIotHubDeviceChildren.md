---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988079"
---
# <span data-ttu-id="bba0d-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="bba0d-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="bba0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba0d-102">SYNOPSIS</span></span>
<span data-ttu-id="bba0d-103">Drukowanie rozdzielonych przecinkami listy przypisanych urządzeń dzieci.</span><span class="sxs-lookup"><span data-stu-id="bba0d-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="bba0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bba0d-104">SYNTAX</span></span>

### <span data-ttu-id="bba0d-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bba0d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba0d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bba0d-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba0d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bba0d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba0d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bba0d-108">DESCRIPTION</span></span>
<span data-ttu-id="bba0d-109">Pokaż wszystkie przypisane urządzenia, które nie są krawędziami, jako rozdzieloną przecinkami listę wszystkich urządzeń brzegowych lub określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="bba0d-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="bba0d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bba0d-110">EXAMPLES</span></span>

### <span data-ttu-id="bba0d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bba0d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="bba0d-112">Pokaż wszystkie przypisane urządzenia, które nie są krawędziami, jako listę rozdzielaną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="bba0d-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="bba0d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bba0d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="bba0d-114">Pokaż wszystkie przypisane urządzenia, które nie są krawędziami, jako rozdzieloną przecinkami listę wszystkich urządzeń brzegowych.</span><span class="sxs-lookup"><span data-stu-id="bba0d-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="bba0d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bba0d-115">PARAMETERS</span></span>

### <span data-ttu-id="bba0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba0d-116">-DefaultProfile</span></span>
<span data-ttu-id="bba0d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bba0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba0d-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="bba0d-118">-DeviceId</span></span>
<span data-ttu-id="bba0d-119">Identyfikator urządzenia edge.</span><span class="sxs-lookup"><span data-stu-id="bba0d-119">Id of edge device.</span></span>

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

### <span data-ttu-id="bba0d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bba0d-120">-InputObject</span></span>
<span data-ttu-id="bba0d-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="bba0d-121">IotHub object</span></span>

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

### <span data-ttu-id="bba0d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bba0d-122">-IotHubName</span></span>
<span data-ttu-id="bba0d-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="bba0d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bba0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="bba0d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bba0d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bba0d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bba0d-126">-ResourceId</span></span>
<span data-ttu-id="bba0d-127">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="bba0d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bba0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba0d-128">CommonParameters</span></span>
<span data-ttu-id="bba0d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba0d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba0d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba0d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bba0d-131">INPUTS</span></span>

### <span data-ttu-id="bba0d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bba0d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bba0d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bba0d-133">System.String</span></span>

## <span data-ttu-id="bba0d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bba0d-134">OUTPUTS</span></span>

### <span data-ttu-id="bba0d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDdyseksjadowa</span><span class="sxs-lookup"><span data-stu-id="bba0d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="bba0d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices Jednakowy[]</span><span class="sxs-lookup"><span data-stu-id="bba0d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="bba0d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bba0d-137">NOTES</span></span>

## <span data-ttu-id="bba0d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bba0d-138">RELATED LINKS</span></span>
