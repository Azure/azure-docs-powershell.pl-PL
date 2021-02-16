---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183234"
---
# <span data-ttu-id="fb65e-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fb65e-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="fb65e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb65e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb65e-103">Konfigurowanie wyzwalaczy na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="fb65e-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="fb65e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb65e-104">SYNTAX</span></span>

### <span data-ttu-id="fb65e-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fb65e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb65e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb65e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb65e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb65e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb65e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb65e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fb65e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb65e-109">DESCRIPTION</span></span>
<span data-ttu-id="fb65e-110">Polecenie **cmdlet Get-AzStackEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="fb65e-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="fb65e-111">Nazwę można określić jako parametr w poleceniach cmdlet w celu zdalnego dostępu do szczegółów określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="fb65e-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="fb65e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb65e-112">EXAMPLES</span></span>

### <span data-ttu-id="fb65e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb65e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="fb65e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb65e-114">PARAMETERS</span></span>

### <span data-ttu-id="fb65e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb65e-115">-DefaultProfile</span></span>
<span data-ttu-id="fb65e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb65e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb65e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb65e-117">-DeviceName</span></span>
<span data-ttu-id="fb65e-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="fb65e-118">Device Name</span></span>

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

### <span data-ttu-id="fb65e-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fb65e-119">-DeviceObject</span></span>
<span data-ttu-id="fb65e-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="fb65e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="fb65e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb65e-121">-Name</span></span>
<span data-ttu-id="fb65e-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="fb65e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb65e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb65e-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb65e-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fb65e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fb65e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb65e-125">-ResourceId</span></span>
<span data-ttu-id="fb65e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb65e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="fb65e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb65e-127">CommonParameters</span></span>
<span data-ttu-id="fb65e-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb65e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb65e-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb65e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb65e-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb65e-130">INPUTS</span></span>

### <span data-ttu-id="fb65e-131">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fb65e-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="fb65e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb65e-132">OUTPUTS</span></span>

### <span data-ttu-id="fb65e-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fb65e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="fb65e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb65e-134">NOTES</span></span>

## <span data-ttu-id="fb65e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb65e-135">RELATED LINKS</span></span>
