---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194907"
---
# <span data-ttu-id="fe2fa-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2fa-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="fe2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2fa-103">Pobiera konta magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="fe2fa-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="fe2fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe2fa-104">SYNTAX</span></span>

### <span data-ttu-id="fe2fa-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fe2fa-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fa-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2fa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2fa-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2fa-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fa-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2fa-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fe2fa-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe2fa-109">DESCRIPTION</span></span>
<span data-ttu-id="fe2fa-110">Polecenie **cmdlet Get-AzDataBoxEdgeStorageAccount** pobiera konta magazynu edge dostępne na urządzeniu z programem Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="fe2fa-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="fe2fa-111">Możesz określić nazwę jako parametr w poleceniach cmdlet, aby uzyskać informacje o określonym koncie magazynu edge.</span><span class="sxs-lookup"><span data-stu-id="fe2fa-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="fe2fa-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe2fa-112">EXAMPLES</span></span>

### <span data-ttu-id="fe2fa-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe2fa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="fe2fa-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe2fa-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="fe2fa-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fe2fa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="fe2fa-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="fe2fa-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="fe2fa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe2fa-117">PARAMETERS</span></span>

### <span data-ttu-id="fe2fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2fa-118">-DefaultProfile</span></span>
<span data-ttu-id="fe2fa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2fa-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fe2fa-120">-DeviceName</span></span>
<span data-ttu-id="fe2fa-121">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="fe2fa-121">Device Name</span></span>

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

### <span data-ttu-id="fe2fa-122">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fe2fa-122">-DeviceObject</span></span>
<span data-ttu-id="fe2fa-123">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="fe2fa-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="fe2fa-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe2fa-124">-Name</span></span>
<span data-ttu-id="fe2fa-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="fe2fa-125">Resource Name</span></span>

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

### <span data-ttu-id="fe2fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe2fa-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fe2fa-127">Resource Group Name</span></span>

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

### <span data-ttu-id="fe2fa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2fa-128">-ResourceId</span></span>
<span data-ttu-id="fe2fa-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2fa-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="fe2fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2fa-130">CommonParameters</span></span>
<span data-ttu-id="fe2fa-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2fa-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe2fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2fa-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe2fa-133">INPUTS</span></span>

### <span data-ttu-id="fe2fa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fe2fa-134">System.String</span></span>

### <span data-ttu-id="fe2fa-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fe2fa-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="fe2fa-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe2fa-136">OUTPUTS</span></span>

### <span data-ttu-id="fe2fa-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2fa-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="fe2fa-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe2fa-138">NOTES</span></span>

## <span data-ttu-id="fe2fa-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe2fa-139">RELATED LINKS</span></span>
