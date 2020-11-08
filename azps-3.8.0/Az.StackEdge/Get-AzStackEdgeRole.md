---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050029"
---
# <span data-ttu-id="b97db-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b97db-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="b97db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b97db-102">SYNOPSIS</span></span>
<span data-ttu-id="b97db-103">Pobiera dostępne role dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="b97db-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="b97db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b97db-104">SYNTAX</span></span>

### <span data-ttu-id="b97db-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b97db-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97db-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b97db-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97db-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b97db-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97db-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b97db-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b97db-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b97db-109">DESCRIPTION</span></span>
<span data-ttu-id="b97db-110">Polecenie cmdlet **Get-AzStackEdgeRole** umożliwia pobranie dostępnych ról usługi IoT dla urządzenia z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="b97db-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="b97db-111">Parametr name można wspominać, aby uzyskać szczegółowe informacje o konkretnej roli IoT.</span><span class="sxs-lookup"><span data-stu-id="b97db-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="b97db-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b97db-112">EXAMPLES</span></span>

### <span data-ttu-id="b97db-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b97db-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="b97db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b97db-114">PARAMETERS</span></span>

### <span data-ttu-id="b97db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97db-115">-DefaultProfile</span></span>
<span data-ttu-id="b97db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b97db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97db-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b97db-117">-DeviceName</span></span>
<span data-ttu-id="b97db-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b97db-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97db-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b97db-119">-DeviceObject</span></span>
<span data-ttu-id="b97db-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="b97db-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b97db-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b97db-121">-Name</span></span>
<span data-ttu-id="b97db-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b97db-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b97db-123">-ResourceGroupName</span></span>
<span data-ttu-id="b97db-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b97db-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97db-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b97db-125">-ResourceId</span></span>
<span data-ttu-id="b97db-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b97db-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97db-127">CommonParameters</span></span>
<span data-ttu-id="b97db-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97db-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b97db-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97db-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b97db-130">INPUTS</span></span>

### <span data-ttu-id="b97db-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b97db-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b97db-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b97db-132">OUTPUTS</span></span>

### <span data-ttu-id="b97db-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b97db-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b97db-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b97db-134">NOTES</span></span>

## <span data-ttu-id="b97db-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b97db-135">RELATED LINKS</span></span>
