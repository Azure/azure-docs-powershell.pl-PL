---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222804"
---
# <span data-ttu-id="3085e-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3085e-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="3085e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3085e-102">SYNOPSIS</span></span>
<span data-ttu-id="3085e-103">Pobiera dostępne role dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3085e-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="3085e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3085e-104">SYNTAX</span></span>

### <span data-ttu-id="3085e-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3085e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3085e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3085e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3085e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3085e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3085e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3085e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3085e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3085e-109">DESCRIPTION</span></span>
<span data-ttu-id="3085e-110">Polecenie cmdlet **Get-AzStackEdgeRole** umożliwia pobranie dostępnych ról usługi IoT dla urządzenia z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="3085e-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="3085e-111">Parametr name można wspominać, aby uzyskać szczegółowe informacje o konkretnej roli IoT.</span><span class="sxs-lookup"><span data-stu-id="3085e-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="3085e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3085e-112">EXAMPLES</span></span>

### <span data-ttu-id="3085e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3085e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="3085e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3085e-114">PARAMETERS</span></span>

### <span data-ttu-id="3085e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3085e-115">-DefaultProfile</span></span>
<span data-ttu-id="3085e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3085e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3085e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3085e-117">-DeviceName</span></span>
<span data-ttu-id="3085e-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="3085e-118">Device Name</span></span>

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

### <span data-ttu-id="3085e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3085e-119">-DeviceObject</span></span>
<span data-ttu-id="3085e-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="3085e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3085e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3085e-121">-Name</span></span>
<span data-ttu-id="3085e-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="3085e-122">Resource Name</span></span>

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

### <span data-ttu-id="3085e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3085e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3085e-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3085e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3085e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3085e-125">-ResourceId</span></span>
<span data-ttu-id="3085e-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3085e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="3085e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3085e-127">CommonParameters</span></span>
<span data-ttu-id="3085e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3085e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3085e-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3085e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3085e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3085e-130">INPUTS</span></span>

### <span data-ttu-id="3085e-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3085e-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="3085e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3085e-132">OUTPUTS</span></span>

### <span data-ttu-id="3085e-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3085e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3085e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3085e-134">NOTES</span></span>

## <span data-ttu-id="3085e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3085e-135">RELATED LINKS</span></span>
