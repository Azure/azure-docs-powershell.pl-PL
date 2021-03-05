---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 34ef411b96aaee2a6caa32452c678d888cf62b65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962602"
---
# <span data-ttu-id="10f52-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="10f52-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="10f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f52-102">SYNOPSIS</span></span>
<span data-ttu-id="10f52-103">Pobiera dostępne udziały dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="10f52-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="10f52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10f52-104">SYNTAX</span></span>

### <span data-ttu-id="10f52-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10f52-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10f52-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f52-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10f52-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f52-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10f52-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f52-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="10f52-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="10f52-109">DESCRIPTION</span></span>
<span data-ttu-id="10f52-110">Polecenie **cmdlet Get-AzStackEdgeShare** pobiera dostępne udziały dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="10f52-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="10f52-111">Jeśli podano nazwę, to ta akcja będzie udostępniana według nazwy.</span><span class="sxs-lookup"><span data-stu-id="10f52-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="10f52-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10f52-112">EXAMPLES</span></span>

### <span data-ttu-id="10f52-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10f52-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="10f52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f52-114">PARAMETERS</span></span>

### <span data-ttu-id="10f52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f52-115">-DefaultProfile</span></span>
<span data-ttu-id="10f52-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10f52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10f52-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="10f52-117">-DeviceName</span></span>
<span data-ttu-id="10f52-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="10f52-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="10f52-119">-DeviceObject</span></span>
<span data-ttu-id="10f52-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="10f52-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10f52-121">-Name</span></span>
<span data-ttu-id="10f52-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="10f52-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f52-123">-ResourceGroupName</span></span>
<span data-ttu-id="10f52-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="10f52-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10f52-125">-ResourceId</span></span>
<span data-ttu-id="10f52-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="10f52-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="10f52-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f52-127">CommonParameters</span></span>
<span data-ttu-id="10f52-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f52-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f52-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f52-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f52-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f52-130">INPUTS</span></span>

### <span data-ttu-id="10f52-131">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="10f52-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="10f52-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f52-132">OUTPUTS</span></span>

### <span data-ttu-id="10f52-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="10f52-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="10f52-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10f52-134">NOTES</span></span>

## <span data-ttu-id="10f52-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f52-135">RELATED LINKS</span></span>
