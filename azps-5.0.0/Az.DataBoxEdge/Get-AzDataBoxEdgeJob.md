---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306612"
---
# <span data-ttu-id="4e56c-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="4e56c-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="4e56c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e56c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e56c-103">Pobiera zadania zaplanowane na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="4e56c-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="4e56c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e56c-104">SYNTAX</span></span>

### <span data-ttu-id="4e56c-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e56c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e56c-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="4e56c-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e56c-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e56c-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4e56c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4e56c-108">DESCRIPTION</span></span>
<span data-ttu-id="4e56c-109">Polecenie cmdlet **Get-AzDataBoxEdgeJob** umożliwia pobieranie aktywnych zadań na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="4e56c-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="4e56c-110">Możesz wspomnieć o parametrze Name, aby uzyskać szczegółowe informacje o konkretnym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="4e56c-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="4e56c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e56c-111">EXAMPLES</span></span>

### <span data-ttu-id="4e56c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e56c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="4e56c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e56c-113">PARAMETERS</span></span>

### <span data-ttu-id="4e56c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e56c-114">-DefaultProfile</span></span>
<span data-ttu-id="4e56c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e56c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e56c-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4e56c-116">-DeviceName</span></span>
<span data-ttu-id="4e56c-117">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="4e56c-117">Name of the device</span></span>

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

### <span data-ttu-id="4e56c-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4e56c-118">-DeviceObject</span></span>
<span data-ttu-id="4e56c-119">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="4e56c-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="4e56c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e56c-120">-Name</span></span>
<span data-ttu-id="4e56c-121">Nazwa zadania, zwykle identyfikator GUID</span><span class="sxs-lookup"><span data-stu-id="4e56c-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="4e56c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e56c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e56c-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4e56c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4e56c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e56c-124">-ResourceId</span></span>
<span data-ttu-id="4e56c-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4e56c-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="4e56c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e56c-126">CommonParameters</span></span>
<span data-ttu-id="4e56c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e56c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e56c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e56c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e56c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e56c-129">INPUTS</span></span>

### <span data-ttu-id="4e56c-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4e56c-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4e56c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e56c-131">OUTPUTS</span></span>

### <span data-ttu-id="4e56c-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="4e56c-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="4e56c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e56c-133">NOTES</span></span>

## <span data-ttu-id="4e56c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e56c-134">RELATED LINKS</span></span>
