---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183235"
---
# <span data-ttu-id="ced94-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced94-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ced94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced94-102">SYNOPSIS</span></span>
<span data-ttu-id="ced94-103">Pobiera kontenery na konto magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="ced94-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="ced94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ced94-104">SYNTAX</span></span>

### <span data-ttu-id="ced94-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ced94-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ced94-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced94-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ced94-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced94-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ced94-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced94-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="ced94-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ced94-109">DESCRIPTION</span></span>
<span data-ttu-id="ced94-110">Polecenie **cmdlet Get-AzStackEdgeStorageContainer** pobiera kontener magazynu dla konta magazynu edge na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="ced94-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="ced94-111">Możesz określić nazwę jako parametr w poleceniach cmdlet, aby uzyskać dostęp do szczegółów określonego kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="ced94-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="ced94-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ced94-112">EXAMPLES</span></span>

### <span data-ttu-id="ced94-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ced94-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="ced94-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ced94-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="ced94-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ced94-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="ced94-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced94-116">PARAMETERS</span></span>

### <span data-ttu-id="ced94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced94-117">-DefaultProfile</span></span>
<span data-ttu-id="ced94-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ced94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced94-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ced94-119">-DeviceName</span></span>
<span data-ttu-id="ced94-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="ced94-120">Device Name</span></span>

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

### <span data-ttu-id="ced94-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ced94-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="ced94-122">Podaj nazwę istniejącego konta EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced94-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced94-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="ced94-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="ced94-124">Podaj istniejący obiekt EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced94-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ced94-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ced94-125">-Name</span></span>
<span data-ttu-id="ced94-126">Nazwa serwera EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced94-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced94-127">-ResourceGroupName</span></span>
<span data-ttu-id="ced94-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ced94-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ced94-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced94-129">-ResourceId</span></span>
<span data-ttu-id="ced94-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced94-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced94-131">CommonParameters</span></span>
<span data-ttu-id="ced94-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced94-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ced94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced94-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ced94-134">INPUTS</span></span>

### <span data-ttu-id="ced94-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ced94-135">System.String</span></span>

### <span data-ttu-id="ced94-136">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced94-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ced94-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ced94-137">OUTPUTS</span></span>

### <span data-ttu-id="ced94-138">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced94-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ced94-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ced94-139">NOTES</span></span>

## <span data-ttu-id="ced94-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ced94-140">RELATED LINKS</span></span>
