---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 616830906621b673010ca8708b909608c06f93fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998628"
---
# <span data-ttu-id="5012a-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5012a-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="5012a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5012a-102">SYNOPSIS</span></span>
<span data-ttu-id="5012a-103">Pobiera dostępne udziały dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5012a-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="5012a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5012a-104">SYNTAX</span></span>

### <span data-ttu-id="5012a-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5012a-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5012a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5012a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5012a-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5012a-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5012a-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5012a-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5012a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5012a-109">DESCRIPTION</span></span>
<span data-ttu-id="5012a-110">Polecenie **cmdlet Get-AzDataBoxEdgeShare** pobiera dostępne udziały dla urządzenia Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="5012a-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="5012a-111">Jeśli podano nazwę, to ta akcja będzie udostępniana według nazwy.</span><span class="sxs-lookup"><span data-stu-id="5012a-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="5012a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5012a-112">EXAMPLES</span></span>

### <span data-ttu-id="5012a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5012a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="5012a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5012a-114">PARAMETERS</span></span>

### <span data-ttu-id="5012a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5012a-115">-DefaultProfile</span></span>
<span data-ttu-id="5012a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5012a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5012a-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5012a-117">-DeviceName</span></span>
<span data-ttu-id="5012a-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="5012a-118">Device Name</span></span>

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

### <span data-ttu-id="5012a-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5012a-119">-DeviceObject</span></span>
<span data-ttu-id="5012a-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="5012a-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5012a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5012a-121">-Name</span></span>
<span data-ttu-id="5012a-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="5012a-122">Resource Name</span></span>

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

### <span data-ttu-id="5012a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5012a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5012a-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5012a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5012a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5012a-125">-ResourceId</span></span>
<span data-ttu-id="5012a-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5012a-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5012a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5012a-127">CommonParameters</span></span>
<span data-ttu-id="5012a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5012a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5012a-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5012a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5012a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5012a-130">INPUTS</span></span>

### <span data-ttu-id="5012a-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5012a-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="5012a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5012a-132">OUTPUTS</span></span>

### <span data-ttu-id="5012a-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5012a-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="5012a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5012a-134">NOTES</span></span>

## <span data-ttu-id="5012a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5012a-135">RELATED LINKS</span></span>
