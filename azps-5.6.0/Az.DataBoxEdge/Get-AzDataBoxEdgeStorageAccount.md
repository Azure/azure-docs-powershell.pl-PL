---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 8f89f45e1752b0a41d2d20e6521f0591ab0d90ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998614"
---
# <span data-ttu-id="04cec-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04cec-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="04cec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04cec-102">SYNOPSIS</span></span>
<span data-ttu-id="04cec-103">Pobiera konta magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="04cec-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="04cec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04cec-104">SYNTAX</span></span>

### <span data-ttu-id="04cec-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="04cec-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04cec-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04cec-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04cec-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04cec-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04cec-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04cec-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="04cec-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="04cec-109">DESCRIPTION</span></span>
<span data-ttu-id="04cec-110">Polecenie **cmdlet Get-AzDataBoxEdgeStorageAccount** pobiera konta magazynu edge dostępne na urządzeniu z programem Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="04cec-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="04cec-111">Możesz określić nazwę jako parametr w poleceniach cmdlet, aby uzyskać informacje o określonym koncie magazynu edge.</span><span class="sxs-lookup"><span data-stu-id="04cec-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="04cec-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04cec-112">EXAMPLES</span></span>

### <span data-ttu-id="04cec-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="04cec-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="04cec-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="04cec-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="04cec-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="04cec-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="04cec-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="04cec-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="04cec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04cec-117">PARAMETERS</span></span>

### <span data-ttu-id="04cec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cec-118">-DefaultProfile</span></span>
<span data-ttu-id="04cec-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04cec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cec-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="04cec-120">-DeviceName</span></span>
<span data-ttu-id="04cec-121">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="04cec-121">Device Name</span></span>

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

### <span data-ttu-id="04cec-122">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="04cec-122">-DeviceObject</span></span>
<span data-ttu-id="04cec-123">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="04cec-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="04cec-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04cec-124">-Name</span></span>
<span data-ttu-id="04cec-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="04cec-125">Resource Name</span></span>

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

### <span data-ttu-id="04cec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cec-126">-ResourceGroupName</span></span>
<span data-ttu-id="04cec-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="04cec-127">Resource Group Name</span></span>

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

### <span data-ttu-id="04cec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04cec-128">-ResourceId</span></span>
<span data-ttu-id="04cec-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="04cec-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="04cec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cec-130">CommonParameters</span></span>
<span data-ttu-id="04cec-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04cec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cec-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04cec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cec-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04cec-133">INPUTS</span></span>

### <span data-ttu-id="04cec-134">System.String</span><span class="sxs-lookup"><span data-stu-id="04cec-134">System.String</span></span>

### <span data-ttu-id="04cec-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="04cec-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="04cec-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04cec-136">OUTPUTS</span></span>

### <span data-ttu-id="04cec-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04cec-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="04cec-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04cec-138">NOTES</span></span>

## <span data-ttu-id="04cec-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04cec-139">RELATED LINKS</span></span>
