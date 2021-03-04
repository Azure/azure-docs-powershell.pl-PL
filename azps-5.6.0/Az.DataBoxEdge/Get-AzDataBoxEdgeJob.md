---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c6fd1c94700d33dda6aafa6f2b73004f75d4a655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998642"
---
# <span data-ttu-id="7d6d0-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="7d6d0-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="7d6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6d0-103">Pobiera zadania zaplanowane na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="7d6d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d6d0-104">SYNTAX</span></span>

### <span data-ttu-id="7d6d0-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7d6d0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d6d0-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="7d6d0-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d6d0-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d6d0-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7d6d0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d6d0-108">DESCRIPTION</span></span>
<span data-ttu-id="7d6d0-109">Polecenie **cmdlet Get-AzDataBoxEdgeJob** pobiera aktywne zadania na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="7d6d0-110">Możesz wspomnieć o parametrze Name, aby uzyskać szczegółowe informacje o określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="7d6d0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d6d0-111">EXAMPLES</span></span>

### <span data-ttu-id="7d6d0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d6d0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="7d6d0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d6d0-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6d0-114">-DefaultProfile</span></span>
<span data-ttu-id="7d6d0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d6d0-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7d6d0-116">-DeviceName</span></span>
<span data-ttu-id="7d6d0-117">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="7d6d0-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6d0-118">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7d6d0-118">-DeviceObject</span></span>
<span data-ttu-id="7d6d0-119">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="7d6d0-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7d6d0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7d6d0-120">-Name</span></span>
<span data-ttu-id="7d6d0-121">Nazwa zadania, ogólnie identyfikator GUID</span><span class="sxs-lookup"><span data-stu-id="7d6d0-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d6d0-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7d6d0-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6d0-124">-ResourceId</span></span>
<span data-ttu-id="7d6d0-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6d0-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6d0-126">CommonParameters</span></span>
<span data-ttu-id="7d6d0-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6d0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d6d0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6d0-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d6d0-129">INPUTS</span></span>

### <span data-ttu-id="7d6d0-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7d6d0-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7d6d0-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d6d0-131">OUTPUTS</span></span>

### <span data-ttu-id="7d6d0-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="7d6d0-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="7d6d0-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d6d0-133">NOTES</span></span>

## <span data-ttu-id="7d6d0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d6d0-134">RELATED LINKS</span></span>
