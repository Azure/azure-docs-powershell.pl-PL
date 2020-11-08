---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221057"
---
# <span data-ttu-id="0ba96-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="0ba96-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="0ba96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ba96-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba96-103">Pobiera zadania zaplanowane na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="0ba96-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="0ba96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ba96-104">SYNTAX</span></span>

### <span data-ttu-id="0ba96-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ba96-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba96-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="0ba96-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba96-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ba96-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0ba96-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0ba96-108">DESCRIPTION</span></span>
<span data-ttu-id="0ba96-109">Polecenie cmdlet **Get-AzStackEdgeJob** pobiera zadania aktywne na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="0ba96-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="0ba96-110">Możesz wspomnieć o parametrze Name, aby uzyskać szczegółowe informacje o konkretnym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="0ba96-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="0ba96-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ba96-111">EXAMPLES</span></span>

### <span data-ttu-id="0ba96-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ba96-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="0ba96-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ba96-113">PARAMETERS</span></span>

### <span data-ttu-id="0ba96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba96-114">-DefaultProfile</span></span>
<span data-ttu-id="0ba96-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ba96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba96-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0ba96-116">-DeviceName</span></span>
<span data-ttu-id="0ba96-117">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0ba96-117">Name of the device</span></span>

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

### <span data-ttu-id="0ba96-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0ba96-118">-DeviceObject</span></span>
<span data-ttu-id="0ba96-119">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="0ba96-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba96-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ba96-120">-Name</span></span>
<span data-ttu-id="0ba96-121">Nazwa zadania, zwykle identyfikator GUID</span><span class="sxs-lookup"><span data-stu-id="0ba96-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba96-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ba96-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ba96-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0ba96-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ba96-124">-ResourceId</span></span>
<span data-ttu-id="0ba96-125">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0ba96-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba96-126">CommonParameters</span></span>
<span data-ttu-id="0ba96-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba96-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ba96-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba96-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ba96-129">INPUTS</span></span>

### <span data-ttu-id="0ba96-130">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0ba96-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0ba96-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ba96-131">OUTPUTS</span></span>

### <span data-ttu-id="0ba96-132">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="0ba96-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="0ba96-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ba96-133">NOTES</span></span>

## <span data-ttu-id="0ba96-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ba96-134">RELATED LINKS</span></span>
