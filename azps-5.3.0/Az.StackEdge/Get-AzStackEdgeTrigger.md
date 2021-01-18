---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502746"
---
# <span data-ttu-id="f3525-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f3525-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="f3525-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3525-102">SYNOPSIS</span></span>
<span data-ttu-id="f3525-103">Uzyskiwanie wyzwalaczy skonfigurowanych na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="f3525-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="f3525-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3525-104">SYNTAX</span></span>

### <span data-ttu-id="f3525-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3525-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3525-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3525-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3525-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3525-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3525-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3525-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f3525-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f3525-109">DESCRIPTION</span></span>
<span data-ttu-id="f3525-110">Polecenie cmdlet **Get-AzStackEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="f3525-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="f3525-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegółowe dane dotyczące określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="f3525-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="f3525-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3525-112">EXAMPLES</span></span>

### <span data-ttu-id="f3525-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3525-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="f3525-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3525-114">PARAMETERS</span></span>

### <span data-ttu-id="f3525-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3525-115">-DefaultProfile</span></span>
<span data-ttu-id="f3525-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3525-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3525-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f3525-117">-DeviceName</span></span>
<span data-ttu-id="f3525-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="f3525-118">Device Name</span></span>

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

### <span data-ttu-id="f3525-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f3525-119">-DeviceObject</span></span>
<span data-ttu-id="f3525-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="f3525-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f3525-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3525-121">-Name</span></span>
<span data-ttu-id="f3525-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="f3525-122">Resource Name</span></span>

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

### <span data-ttu-id="f3525-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3525-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3525-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f3525-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f3525-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3525-125">-ResourceId</span></span>
<span data-ttu-id="f3525-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f3525-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f3525-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3525-127">CommonParameters</span></span>
<span data-ttu-id="f3525-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3525-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3525-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3525-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3525-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3525-130">INPUTS</span></span>

### <span data-ttu-id="f3525-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f3525-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f3525-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3525-132">OUTPUTS</span></span>

### <span data-ttu-id="f3525-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f3525-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="f3525-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3525-134">NOTES</span></span>

## <span data-ttu-id="f3525-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3525-135">RELATED LINKS</span></span>
