---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064187"
---
# <span data-ttu-id="cd652-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cd652-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cd652-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd652-102">SYNOPSIS</span></span>
<span data-ttu-id="cd652-103">Uzyskiwanie wyzwalaczy skonfigurowanych na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="cd652-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="cd652-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd652-104">SYNTAX</span></span>

### <span data-ttu-id="cd652-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd652-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd652-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd652-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd652-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd652-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd652-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd652-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cd652-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cd652-109">DESCRIPTION</span></span>
<span data-ttu-id="cd652-110">Polecenie cmdlet **Get-AzDataBoxEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="cd652-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="cd652-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegółowe dane dotyczące określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="cd652-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="cd652-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd652-112">EXAMPLES</span></span>

### <span data-ttu-id="cd652-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd652-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="cd652-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd652-114">PARAMETERS</span></span>

### <span data-ttu-id="cd652-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd652-115">-DefaultProfile</span></span>
<span data-ttu-id="cd652-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd652-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd652-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cd652-117">-DeviceName</span></span>
<span data-ttu-id="cd652-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="cd652-118">Device Name</span></span>

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

### <span data-ttu-id="cd652-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cd652-119">-DeviceObject</span></span>
<span data-ttu-id="cd652-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="cd652-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="cd652-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd652-121">-Name</span></span>
<span data-ttu-id="cd652-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="cd652-122">Resource Name</span></span>

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

### <span data-ttu-id="cd652-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd652-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd652-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd652-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cd652-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd652-125">-ResourceId</span></span>
<span data-ttu-id="cd652-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd652-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="cd652-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd652-127">CommonParameters</span></span>
<span data-ttu-id="cd652-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd652-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd652-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd652-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd652-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd652-130">INPUTS</span></span>

### <span data-ttu-id="cd652-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cd652-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cd652-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd652-132">OUTPUTS</span></span>

### <span data-ttu-id="cd652-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cd652-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cd652-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd652-134">NOTES</span></span>

## <span data-ttu-id="cd652-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd652-135">RELATED LINKS</span></span>
