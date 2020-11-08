---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052381"
---
# <span data-ttu-id="b739c-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b739c-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b739c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b739c-102">SYNOPSIS</span></span>
<span data-ttu-id="b739c-103">Umożliwia wyświetlenie konta magazynu programu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="b739c-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="b739c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b739c-104">SYNTAX</span></span>

### <span data-ttu-id="b739c-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b739c-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b739c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b739c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b739c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b739c-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b739c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b739c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b739c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b739c-109">DESCRIPTION</span></span>
<span data-ttu-id="b739c-110">Polecenie cmdlet **Get-AzDataBoxEdgeStorageAccount umożliwia wyświetlenie** konta magazynu z krawędziami dostępnymi na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="b739c-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="b739c-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby uzyskać informacje o konkretnym koncie magazynu Edge.</span><span class="sxs-lookup"><span data-stu-id="b739c-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="b739c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b739c-112">EXAMPLES</span></span>

### <span data-ttu-id="b739c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b739c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="b739c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b739c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b739c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b739c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b739c-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b739c-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="b739c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b739c-117">PARAMETERS</span></span>

### <span data-ttu-id="b739c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b739c-118">-DefaultProfile</span></span>
<span data-ttu-id="b739c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b739c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b739c-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b739c-120">-DeviceName</span></span>
<span data-ttu-id="b739c-121">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b739c-121">Device Name</span></span>

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

### <span data-ttu-id="b739c-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b739c-122">-DeviceObject</span></span>
<span data-ttu-id="b739c-123">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="b739c-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b739c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b739c-124">-Name</span></span>
<span data-ttu-id="b739c-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b739c-125">Resource Name</span></span>

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

### <span data-ttu-id="b739c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b739c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b739c-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b739c-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b739c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b739c-128">-ResourceId</span></span>
<span data-ttu-id="b739c-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b739c-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b739c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b739c-130">CommonParameters</span></span>
<span data-ttu-id="b739c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b739c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b739c-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b739c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b739c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b739c-133">INPUTS</span></span>

### <span data-ttu-id="b739c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b739c-134">System.String</span></span>

### <span data-ttu-id="b739c-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b739c-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b739c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b739c-136">OUTPUTS</span></span>

### <span data-ttu-id="b739c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b739c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b739c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b739c-138">NOTES</span></span>

## <span data-ttu-id="b739c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b739c-139">RELATED LINKS</span></span>
