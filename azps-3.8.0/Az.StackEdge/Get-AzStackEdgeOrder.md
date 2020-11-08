---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050036"
---
# <span data-ttu-id="fb205-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="fb205-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="fb205-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb205-102">SYNOPSIS</span></span>
<span data-ttu-id="fb205-103">Uzyskiwanie szczegółowych informacji o zamówieniach dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="fb205-103">Get the order details for a device</span></span>

## <span data-ttu-id="fb205-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb205-104">SYNTAX</span></span>

### <span data-ttu-id="fb205-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb205-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb205-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb205-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb205-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb205-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb205-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fb205-108">DESCRIPTION</span></span>
<span data-ttu-id="fb205-109">Polecenie cmdlet **Get-AzStackEdgeOrder** pobiera Szczegóły zamówień na urządzeniu z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="fb205-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="fb205-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb205-110">EXAMPLES</span></span>

### <span data-ttu-id="fb205-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb205-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="fb205-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb205-112">PARAMETERS</span></span>

### <span data-ttu-id="fb205-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb205-113">-DefaultProfile</span></span>
<span data-ttu-id="fb205-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb205-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb205-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb205-115">-DeviceName</span></span>
<span data-ttu-id="fb205-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fb205-116">Resource Group Name</span></span>

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

### <span data-ttu-id="fb205-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fb205-117">-DeviceObject</span></span>
<span data-ttu-id="fb205-118">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="fb205-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="fb205-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb205-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb205-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fb205-120">Resource Group Name</span></span>

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

### <span data-ttu-id="fb205-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb205-121">-ResourceId</span></span>
<span data-ttu-id="fb205-122">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fb205-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="fb205-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb205-123">CommonParameters</span></span>
<span data-ttu-id="fb205-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb205-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb205-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb205-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb205-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb205-126">INPUTS</span></span>

### <span data-ttu-id="fb205-127">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fb205-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="fb205-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb205-128">System.String</span></span>

## <span data-ttu-id="fb205-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb205-129">OUTPUTS</span></span>

### <span data-ttu-id="fb205-130">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="fb205-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="fb205-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb205-131">NOTES</span></span>

## <span data-ttu-id="fb205-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb205-132">RELATED LINKS</span></span>
