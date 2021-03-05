---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: d15a8dd5aecaa57c54707b026ad05763563b2070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997102"
---
# <span data-ttu-id="21927-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="21927-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="21927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21927-102">SYNOPSIS</span></span>
<span data-ttu-id="21927-103">Uzyskaj szczegóły zamówienia dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="21927-103">Get the order details for a device</span></span>

## <span data-ttu-id="21927-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21927-104">SYNTAX</span></span>

### <span data-ttu-id="21927-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="21927-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21927-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21927-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21927-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21927-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21927-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="21927-108">DESCRIPTION</span></span>
<span data-ttu-id="21927-109">Polecenie **cmdlet Get-AzStackEdgeOrder** pobiera szczegóły zamówienia dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="21927-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="21927-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21927-110">EXAMPLES</span></span>

### <span data-ttu-id="21927-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21927-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="21927-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21927-112">PARAMETERS</span></span>

### <span data-ttu-id="21927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21927-113">-DefaultProfile</span></span>
<span data-ttu-id="21927-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21927-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21927-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="21927-115">-DeviceName</span></span>
<span data-ttu-id="21927-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="21927-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21927-117">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="21927-117">-DeviceObject</span></span>
<span data-ttu-id="21927-118">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="21927-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21927-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21927-119">-ResourceGroupName</span></span>
<span data-ttu-id="21927-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="21927-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21927-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21927-121">-ResourceId</span></span>
<span data-ttu-id="21927-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="21927-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="21927-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21927-123">CommonParameters</span></span>
<span data-ttu-id="21927-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21927-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21927-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21927-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21927-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21927-126">INPUTS</span></span>

### <span data-ttu-id="21927-127">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="21927-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="21927-128">System.String</span><span class="sxs-lookup"><span data-stu-id="21927-128">System.String</span></span>

## <span data-ttu-id="21927-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21927-129">OUTPUTS</span></span>

### <span data-ttu-id="21927-130">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="21927-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="21927-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21927-131">NOTES</span></span>

## <span data-ttu-id="21927-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21927-132">RELATED LINKS</span></span>
