---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186314"
---
# <span data-ttu-id="dde41-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="dde41-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="dde41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde41-102">SYNOPSIS</span></span>
<span data-ttu-id="dde41-103">Pobiera dostępne udziały dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="dde41-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="dde41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dde41-104">SYNTAX</span></span>

### <span data-ttu-id="dde41-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dde41-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dde41-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde41-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dde41-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde41-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dde41-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde41-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="dde41-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="dde41-109">DESCRIPTION</span></span>
<span data-ttu-id="dde41-110">Polecenie **cmdlet Get-AzDataBoxEdgeShare** pobiera dostępne udziały dla urządzenia Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="dde41-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="dde41-111">Jeśli podano nazwę, to ta akcja będzie udostępniana według nazwy.</span><span class="sxs-lookup"><span data-stu-id="dde41-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="dde41-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dde41-112">EXAMPLES</span></span>

### <span data-ttu-id="dde41-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dde41-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="dde41-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde41-114">PARAMETERS</span></span>

### <span data-ttu-id="dde41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde41-115">-DefaultProfile</span></span>
<span data-ttu-id="dde41-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dde41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde41-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dde41-117">-DeviceName</span></span>
<span data-ttu-id="dde41-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="dde41-118">Device Name</span></span>

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

### <span data-ttu-id="dde41-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="dde41-119">-DeviceObject</span></span>
<span data-ttu-id="dde41-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="dde41-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="dde41-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dde41-121">-Name</span></span>
<span data-ttu-id="dde41-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="dde41-122">Resource Name</span></span>

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

### <span data-ttu-id="dde41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde41-123">-ResourceGroupName</span></span>
<span data-ttu-id="dde41-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dde41-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dde41-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dde41-125">-ResourceId</span></span>
<span data-ttu-id="dde41-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dde41-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="dde41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde41-127">CommonParameters</span></span>
<span data-ttu-id="dde41-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde41-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dde41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde41-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dde41-130">INPUTS</span></span>

### <span data-ttu-id="dde41-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="dde41-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="dde41-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dde41-132">OUTPUTS</span></span>

### <span data-ttu-id="dde41-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="dde41-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="dde41-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dde41-134">NOTES</span></span>

## <span data-ttu-id="dde41-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dde41-135">RELATED LINKS</span></span>
