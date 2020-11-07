---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893278"
---
# <span data-ttu-id="88455-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="88455-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="88455-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88455-102">SYNOPSIS</span></span>
<span data-ttu-id="88455-103">Uzyskiwanie wyzwalaczy skonfigurowanych na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="88455-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="88455-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88455-104">SYNTAX</span></span>

### <span data-ttu-id="88455-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88455-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88455-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88455-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88455-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88455-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88455-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88455-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="88455-109">Opis</span><span class="sxs-lookup"><span data-stu-id="88455-109">DESCRIPTION</span></span>
<span data-ttu-id="88455-110">Polecenie cmdlet **Get-AzDataBoxEdgeTriger** pobiera wyzwalacze dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="88455-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="88455-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegółowe dane dotyczące określonych wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="88455-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="88455-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88455-112">EXAMPLES</span></span>

### <span data-ttu-id="88455-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88455-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="88455-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88455-114">PARAMETERS</span></span>

### <span data-ttu-id="88455-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88455-115">-DefaultProfile</span></span>
<span data-ttu-id="88455-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88455-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88455-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="88455-117">-DeviceName</span></span>
<span data-ttu-id="88455-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="88455-118">Device Name</span></span>

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

### <span data-ttu-id="88455-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="88455-119">-DeviceObject</span></span>
<span data-ttu-id="88455-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="88455-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="88455-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88455-121">-Name</span></span>
<span data-ttu-id="88455-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="88455-122">Resource Name</span></span>

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

### <span data-ttu-id="88455-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88455-123">-ResourceGroupName</span></span>
<span data-ttu-id="88455-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="88455-124">Resource Group Name</span></span>

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

### <span data-ttu-id="88455-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88455-125">-ResourceId</span></span>
<span data-ttu-id="88455-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="88455-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="88455-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88455-127">CommonParameters</span></span>
<span data-ttu-id="88455-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88455-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88455-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88455-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88455-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88455-130">INPUTS</span></span>

### <span data-ttu-id="88455-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="88455-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="88455-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88455-132">OUTPUTS</span></span>

### <span data-ttu-id="88455-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="88455-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="88455-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88455-134">NOTES</span></span>

## <span data-ttu-id="88455-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88455-135">RELATED LINKS</span></span>
