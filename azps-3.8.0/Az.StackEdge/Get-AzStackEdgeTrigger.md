---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050019"
---
# <span data-ttu-id="294b5-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="294b5-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="294b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="294b5-102">SYNOPSIS</span></span>
<span data-ttu-id="294b5-103">Uzyskiwanie wyzwalaczy skonfigurowanych na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="294b5-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="294b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="294b5-104">SYNTAX</span></span>

### <span data-ttu-id="294b5-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="294b5-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294b5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="294b5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294b5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="294b5-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294b5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="294b5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="294b5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="294b5-109">DESCRIPTION</span></span>
<span data-ttu-id="294b5-110">Polecenie cmdlet **Get-AzStackEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="294b5-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="294b5-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegółowe dane dotyczące określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="294b5-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="294b5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="294b5-112">EXAMPLES</span></span>

### <span data-ttu-id="294b5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="294b5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="294b5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="294b5-114">PARAMETERS</span></span>

### <span data-ttu-id="294b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294b5-115">-DefaultProfile</span></span>
<span data-ttu-id="294b5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="294b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="294b5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="294b5-117">-DeviceName</span></span>
<span data-ttu-id="294b5-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="294b5-118">Device Name</span></span>

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

### <span data-ttu-id="294b5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="294b5-119">-DeviceObject</span></span>
<span data-ttu-id="294b5-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="294b5-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="294b5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="294b5-121">-Name</span></span>
<span data-ttu-id="294b5-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="294b5-122">Resource Name</span></span>

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

### <span data-ttu-id="294b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="294b5-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="294b5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="294b5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="294b5-125">-ResourceId</span></span>
<span data-ttu-id="294b5-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="294b5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="294b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294b5-127">CommonParameters</span></span>
<span data-ttu-id="294b5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294b5-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="294b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294b5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="294b5-130">INPUTS</span></span>

### <span data-ttu-id="294b5-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="294b5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="294b5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="294b5-132">OUTPUTS</span></span>

### <span data-ttu-id="294b5-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="294b5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="294b5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="294b5-134">NOTES</span></span>

## <span data-ttu-id="294b5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="294b5-135">RELATED LINKS</span></span>
