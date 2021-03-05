---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 104313bf635f82250172fb2f34889c93a3dc92c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998075"
---
# <span data-ttu-id="17464-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="17464-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="17464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17464-102">SYNOPSIS</span></span>
<span data-ttu-id="17464-103">Uzyskaj szczegóły zamówienia dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="17464-103">Get the order details for a device</span></span>

## <span data-ttu-id="17464-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17464-104">SYNTAX</span></span>

### <span data-ttu-id="17464-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="17464-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17464-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17464-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17464-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17464-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17464-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="17464-108">DESCRIPTION</span></span>
<span data-ttu-id="17464-109">Polecenie **cmdlet Get-AzDataBoxEdgeOrder** pobiera szczegóły zamówienia dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="17464-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="17464-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17464-110">EXAMPLES</span></span>

### <span data-ttu-id="17464-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17464-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="17464-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17464-112">PARAMETERS</span></span>

### <span data-ttu-id="17464-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17464-113">-DefaultProfile</span></span>
<span data-ttu-id="17464-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17464-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17464-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="17464-115">-DeviceName</span></span>
<span data-ttu-id="17464-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="17464-116">Resource Group Name</span></span>

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

### <span data-ttu-id="17464-117">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="17464-117">-DeviceObject</span></span>
<span data-ttu-id="17464-118">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="17464-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="17464-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17464-119">-ResourceGroupName</span></span>
<span data-ttu-id="17464-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="17464-120">Resource Group Name</span></span>

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

### <span data-ttu-id="17464-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17464-121">-ResourceId</span></span>
<span data-ttu-id="17464-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="17464-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="17464-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17464-123">CommonParameters</span></span>
<span data-ttu-id="17464-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17464-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17464-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17464-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17464-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17464-126">INPUTS</span></span>

### <span data-ttu-id="17464-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="17464-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="17464-128">System.String</span><span class="sxs-lookup"><span data-stu-id="17464-128">System.String</span></span>

## <span data-ttu-id="17464-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17464-129">OUTPUTS</span></span>

### <span data-ttu-id="17464-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="17464-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="17464-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17464-131">NOTES</span></span>

## <span data-ttu-id="17464-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17464-132">RELATED LINKS</span></span>
