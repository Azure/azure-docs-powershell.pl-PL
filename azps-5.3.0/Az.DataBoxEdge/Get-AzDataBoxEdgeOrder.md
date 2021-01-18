---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501646"
---
# <span data-ttu-id="6169f-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6169f-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="6169f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6169f-102">SYNOPSIS</span></span>
<span data-ttu-id="6169f-103">Uzyskiwanie szczegółowych informacji o zamówieniach dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="6169f-103">Get the order details for a device</span></span>

## <span data-ttu-id="6169f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6169f-104">SYNTAX</span></span>

### <span data-ttu-id="6169f-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6169f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6169f-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6169f-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6169f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6169f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6169f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6169f-108">DESCRIPTION</span></span>
<span data-ttu-id="6169f-109">Polecenie cmdlet **Get-AzDataBoxEdgeOrder** pobiera szczegóły zamówienia na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="6169f-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="6169f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6169f-110">EXAMPLES</span></span>

### <span data-ttu-id="6169f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6169f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="6169f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6169f-112">PARAMETERS</span></span>

### <span data-ttu-id="6169f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6169f-113">-DefaultProfile</span></span>
<span data-ttu-id="6169f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6169f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6169f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6169f-115">-DeviceName</span></span>
<span data-ttu-id="6169f-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6169f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6169f-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6169f-117">-DeviceObject</span></span>
<span data-ttu-id="6169f-118">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="6169f-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6169f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6169f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6169f-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6169f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="6169f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6169f-121">-ResourceId</span></span>
<span data-ttu-id="6169f-122">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6169f-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="6169f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6169f-123">CommonParameters</span></span>
<span data-ttu-id="6169f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6169f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6169f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6169f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6169f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6169f-126">INPUTS</span></span>

### <span data-ttu-id="6169f-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6169f-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="6169f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6169f-128">System.String</span></span>

## <span data-ttu-id="6169f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6169f-129">OUTPUTS</span></span>

### <span data-ttu-id="6169f-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6169f-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="6169f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6169f-131">NOTES</span></span>

## <span data-ttu-id="6169f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6169f-132">RELATED LINKS</span></span>
