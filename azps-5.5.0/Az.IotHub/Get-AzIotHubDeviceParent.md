---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185746"
---
# <span data-ttu-id="0ee73-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="0ee73-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="0ee73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee73-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee73-103">Pobierz urządzenie nadrzędne określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="0ee73-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="0ee73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ee73-104">SYNTAX</span></span>

### <span data-ttu-id="0ee73-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ee73-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ee73-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0ee73-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ee73-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0ee73-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ee73-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ee73-108">DESCRIPTION</span></span>
<span data-ttu-id="0ee73-109">Pobierz urządzenie nadrzędne określonego urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="0ee73-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="0ee73-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ee73-110">EXAMPLES</span></span>

### <span data-ttu-id="0ee73-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ee73-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="0ee73-112">Pobierz urządzenie nadrzędne określonego urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="0ee73-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="0ee73-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ee73-113">PARAMETERS</span></span>

### <span data-ttu-id="0ee73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee73-114">-DefaultProfile</span></span>
<span data-ttu-id="0ee73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ee73-116">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="0ee73-116">-DeviceId</span></span>
<span data-ttu-id="0ee73-117">Identyfikator urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="0ee73-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="0ee73-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ee73-118">-InputObject</span></span>
<span data-ttu-id="0ee73-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="0ee73-119">IotHub object</span></span>

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

### <span data-ttu-id="0ee73-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0ee73-120">-IotHubName</span></span>
<span data-ttu-id="0ee73-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="0ee73-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0ee73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ee73-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ee73-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ee73-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0ee73-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ee73-124">-ResourceId</span></span>
<span data-ttu-id="0ee73-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="0ee73-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0ee73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee73-126">CommonParameters</span></span>
<span data-ttu-id="0ee73-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee73-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee73-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee73-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ee73-129">INPUTS</span></span>

### <span data-ttu-id="0ee73-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0ee73-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0ee73-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0ee73-131">System.String</span></span>

## <span data-ttu-id="0ee73-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ee73-132">OUTPUTS</span></span>

### <span data-ttu-id="0ee73-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="0ee73-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="0ee73-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ee73-134">NOTES</span></span>

## <span data-ttu-id="0ee73-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ee73-135">RELATED LINKS</span></span>
