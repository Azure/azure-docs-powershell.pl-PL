---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195850"
---
# <span data-ttu-id="8e060-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e060-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8e060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e060-102">SYNOPSIS</span></span>
<span data-ttu-id="8e060-103">Pobiera konta magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="8e060-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="8e060-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e060-104">SYNTAX</span></span>

### <span data-ttu-id="8e060-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8e060-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e060-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e060-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e060-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e060-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e060-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e060-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8e060-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e060-109">DESCRIPTION</span></span>
<span data-ttu-id="8e060-110">Polecenie **cmdlet Get-AzStackEdgeStorageAccount** pobiera konta magazynu edge dostępne na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="8e060-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="8e060-111">Możesz określić nazwę jako parametr w poleceniach cmdlet, aby uzyskać informacje o określonym koncie magazynu edge.</span><span class="sxs-lookup"><span data-stu-id="8e060-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="8e060-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e060-112">EXAMPLES</span></span>

### <span data-ttu-id="8e060-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8e060-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="8e060-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8e060-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8e060-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8e060-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8e060-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8e060-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="8e060-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e060-117">PARAMETERS</span></span>

### <span data-ttu-id="8e060-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e060-118">-DefaultProfile</span></span>
<span data-ttu-id="8e060-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e060-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e060-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8e060-120">-DeviceName</span></span>
<span data-ttu-id="8e060-121">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="8e060-121">Device Name</span></span>

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

### <span data-ttu-id="8e060-122">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8e060-122">-DeviceObject</span></span>
<span data-ttu-id="8e060-123">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="8e060-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8e060-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e060-124">-Name</span></span>
<span data-ttu-id="8e060-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="8e060-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e060-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e060-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e060-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8e060-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8e060-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e060-128">-ResourceId</span></span>
<span data-ttu-id="8e060-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e060-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8e060-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e060-130">CommonParameters</span></span>
<span data-ttu-id="8e060-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e060-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e060-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e060-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e060-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e060-133">INPUTS</span></span>

### <span data-ttu-id="8e060-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8e060-134">System.String</span></span>

### <span data-ttu-id="8e060-135">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8e060-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="8e060-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e060-136">OUTPUTS</span></span>

### <span data-ttu-id="8e060-137">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e060-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8e060-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e060-138">NOTES</span></span>

## <span data-ttu-id="8e060-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e060-139">RELATED LINKS</span></span>
