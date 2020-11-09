---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306601"
---
# <span data-ttu-id="0210e-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0210e-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="0210e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0210e-102">SYNOPSIS</span></span>
<span data-ttu-id="0210e-103">Pobiera dostępne role dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="0210e-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="0210e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0210e-104">SYNTAX</span></span>

### <span data-ttu-id="0210e-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0210e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0210e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0210e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0210e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0210e-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0210e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0210e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0210e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0210e-109">DESCRIPTION</span></span>
<span data-ttu-id="0210e-110">Polecenie cmdlet **Get-AzDataBoxEdgeRole** umożliwia pobranie dostępnych ról usługi IoT dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="0210e-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="0210e-111">Parametr name można wspominać, aby uzyskać szczegółowe informacje o konkretnej roli IoT.</span><span class="sxs-lookup"><span data-stu-id="0210e-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="0210e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0210e-112">EXAMPLES</span></span>

### <span data-ttu-id="0210e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0210e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="0210e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0210e-114">PARAMETERS</span></span>

### <span data-ttu-id="0210e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0210e-115">-DefaultProfile</span></span>
<span data-ttu-id="0210e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0210e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0210e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0210e-117">-DeviceName</span></span>
<span data-ttu-id="0210e-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0210e-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0210e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0210e-119">-DeviceObject</span></span>
<span data-ttu-id="0210e-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="0210e-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0210e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0210e-121">-Name</span></span>
<span data-ttu-id="0210e-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0210e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0210e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0210e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0210e-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0210e-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0210e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0210e-125">-ResourceId</span></span>
<span data-ttu-id="0210e-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0210e-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0210e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0210e-127">CommonParameters</span></span>
<span data-ttu-id="0210e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0210e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0210e-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0210e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0210e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0210e-130">INPUTS</span></span>

### <span data-ttu-id="0210e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0210e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0210e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0210e-132">OUTPUTS</span></span>

### <span data-ttu-id="0210e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0210e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="0210e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0210e-134">NOTES</span></span>

## <span data-ttu-id="0210e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0210e-135">RELATED LINKS</span></span>
