---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: e722fdae30b841a92cf225f27230820fbabe4e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998586"
---
# <span data-ttu-id="985c3-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="985c3-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="985c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985c3-102">SYNOPSIS</span></span>
<span data-ttu-id="985c3-103">Konfigurowanie wyzwalaczy na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="985c3-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="985c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="985c3-104">SYNTAX</span></span>

### <span data-ttu-id="985c3-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="985c3-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="985c3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="985c3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="985c3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="985c3-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="985c3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="985c3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="985c3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="985c3-109">DESCRIPTION</span></span>
<span data-ttu-id="985c3-110">Polecenie **cmdlet Get-AzDataBoxEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="985c3-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="985c3-111">Nazwę można określić jako parametr w poleceniach cmdlet w celu pobrania szczegółów określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="985c3-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="985c3-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="985c3-112">EXAMPLES</span></span>

### <span data-ttu-id="985c3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="985c3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="985c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985c3-114">PARAMETERS</span></span>

### <span data-ttu-id="985c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985c3-115">-DefaultProfile</span></span>
<span data-ttu-id="985c3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="985c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="985c3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="985c3-117">-DeviceName</span></span>
<span data-ttu-id="985c3-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="985c3-118">Device Name</span></span>

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

### <span data-ttu-id="985c3-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="985c3-119">-DeviceObject</span></span>
<span data-ttu-id="985c3-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="985c3-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="985c3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="985c3-121">-Name</span></span>
<span data-ttu-id="985c3-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="985c3-122">Resource Name</span></span>

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

### <span data-ttu-id="985c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="985c3-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="985c3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="985c3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="985c3-125">-ResourceId</span></span>
<span data-ttu-id="985c3-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="985c3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="985c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985c3-127">CommonParameters</span></span>
<span data-ttu-id="985c3-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985c3-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="985c3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985c3-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="985c3-130">INPUTS</span></span>

### <span data-ttu-id="985c3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="985c3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="985c3-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="985c3-132">OUTPUTS</span></span>

### <span data-ttu-id="985c3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="985c3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="985c3-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="985c3-134">NOTES</span></span>

## <span data-ttu-id="985c3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="985c3-135">RELATED LINKS</span></span>
