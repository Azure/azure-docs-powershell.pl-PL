---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367955"
---
# <span data-ttu-id="b076e-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b076e-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="b076e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b076e-102">SYNOPSIS</span></span>
<span data-ttu-id="b076e-103">Umożliwia wyświetlenie konta magazynu programu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="b076e-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="b076e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b076e-104">SYNTAX</span></span>

### <span data-ttu-id="b076e-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b076e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b076e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b076e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b076e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b076e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b076e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b076e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b076e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b076e-109">DESCRIPTION</span></span>
<span data-ttu-id="b076e-110">Polecenie cmdlet **Get-AzStackEdgeStorageAccount umożliwia wyświetlenie** konta magazynu z krawędziami dostępnymi na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="b076e-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="b076e-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby uzyskać informacje o konkretnym koncie magazynu Edge.</span><span class="sxs-lookup"><span data-stu-id="b076e-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="b076e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b076e-112">EXAMPLES</span></span>

### <span data-ttu-id="b076e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b076e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="b076e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b076e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b076e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b076e-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b076e-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b076e-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="b076e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b076e-117">PARAMETERS</span></span>

### <span data-ttu-id="b076e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b076e-118">-DefaultProfile</span></span>
<span data-ttu-id="b076e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b076e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b076e-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b076e-120">-DeviceName</span></span>
<span data-ttu-id="b076e-121">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b076e-121">Device Name</span></span>

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

### <span data-ttu-id="b076e-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b076e-122">-DeviceObject</span></span>
<span data-ttu-id="b076e-123">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="b076e-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b076e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b076e-124">-Name</span></span>
<span data-ttu-id="b076e-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b076e-125">Resource Name</span></span>

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

### <span data-ttu-id="b076e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b076e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b076e-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b076e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b076e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b076e-128">-ResourceId</span></span>
<span data-ttu-id="b076e-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b076e-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b076e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b076e-130">CommonParameters</span></span>
<span data-ttu-id="b076e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b076e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b076e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b076e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b076e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b076e-133">INPUTS</span></span>

### <span data-ttu-id="b076e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b076e-134">System.String</span></span>

### <span data-ttu-id="b076e-135">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b076e-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b076e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b076e-136">OUTPUTS</span></span>

### <span data-ttu-id="b076e-137">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b076e-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="b076e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b076e-138">NOTES</span></span>

## <span data-ttu-id="b076e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b076e-139">RELATED LINKS</span></span>
