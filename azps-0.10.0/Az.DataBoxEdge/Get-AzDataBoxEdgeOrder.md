---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 40cd719a374d5ec2fdaacfe616884b395bd24434
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893297"
---
# <span data-ttu-id="26e54-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26e54-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="26e54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26e54-102">SYNOPSIS</span></span>
<span data-ttu-id="26e54-103">Uzyskiwanie szczegółowych informacji o zamówieniach dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="26e54-103">Get the order details for a device</span></span>

## <span data-ttu-id="26e54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26e54-104">SYNTAX</span></span>

### <span data-ttu-id="26e54-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26e54-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e54-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e54-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e54-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e54-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e54-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26e54-108">DESCRIPTION</span></span>
<span data-ttu-id="26e54-109">Polecenie cmdlet **Get-AzDataBoxEdgeOrder** pobiera szczegóły zamówienia na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="26e54-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="26e54-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26e54-110">EXAMPLES</span></span>

### <span data-ttu-id="26e54-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26e54-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="26e54-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26e54-112">PARAMETERS</span></span>

### <span data-ttu-id="26e54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e54-113">-DefaultProfile</span></span>
<span data-ttu-id="26e54-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26e54-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e54-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="26e54-115">-DeviceName</span></span>
<span data-ttu-id="26e54-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26e54-116">Resource Group Name</span></span>

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

### <span data-ttu-id="26e54-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="26e54-117">-DeviceObject</span></span>
<span data-ttu-id="26e54-118">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="26e54-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="26e54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e54-119">-ResourceGroupName</span></span>
<span data-ttu-id="26e54-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26e54-120">Resource Group Name</span></span>

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

### <span data-ttu-id="26e54-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e54-121">-ResourceId</span></span>
<span data-ttu-id="26e54-122">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="26e54-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="26e54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e54-123">CommonParameters</span></span>
<span data-ttu-id="26e54-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e54-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e54-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e54-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26e54-126">INPUTS</span></span>

### <span data-ttu-id="26e54-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="26e54-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="26e54-128">System. String</span><span class="sxs-lookup"><span data-stu-id="26e54-128">System.String</span></span>

## <span data-ttu-id="26e54-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26e54-129">OUTPUTS</span></span>

### <span data-ttu-id="26e54-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26e54-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="26e54-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26e54-131">NOTES</span></span>

## <span data-ttu-id="26e54-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26e54-132">RELATED LINKS</span></span>
