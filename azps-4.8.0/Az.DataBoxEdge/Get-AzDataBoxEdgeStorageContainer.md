---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221322"
---
# <span data-ttu-id="a0614-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0614-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="a0614-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0614-102">SYNOPSIS</span></span>
<span data-ttu-id="a0614-103">Pobiera kontenery dla konta magazynu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="a0614-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="a0614-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0614-104">SYNTAX</span></span>

### <span data-ttu-id="a0614-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0614-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0614-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0614-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0614-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0614-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0614-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0614-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="a0614-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a0614-109">DESCRIPTION</span></span>
<span data-ttu-id="a0614-110">Polecenie cmdlet **Get-AzDataBoxEdgeStorageContainer** Pobiera kontener magazynu dla konta magazynu Edge na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="a0614-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="a0614-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegóły określonego kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0614-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="a0614-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0614-112">EXAMPLES</span></span>

### <span data-ttu-id="a0614-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0614-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="a0614-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0614-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="a0614-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a0614-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="a0614-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0614-116">PARAMETERS</span></span>

### <span data-ttu-id="a0614-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0614-117">-DefaultProfile</span></span>
<span data-ttu-id="a0614-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0614-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0614-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a0614-119">-DeviceName</span></span>
<span data-ttu-id="a0614-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a0614-120">Device Name</span></span>

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

### <span data-ttu-id="a0614-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0614-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a0614-122">Podaj nazwę istniejącego EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0614-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="a0614-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="a0614-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="a0614-124">Dostarczenie istniejącego obiektu EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0614-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0614-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0614-125">-Name</span></span>
<span data-ttu-id="a0614-126">Nazwa EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0614-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="a0614-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0614-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0614-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a0614-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a0614-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0614-129">-ResourceId</span></span>
<span data-ttu-id="a0614-130">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a0614-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="a0614-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0614-131">CommonParameters</span></span>
<span data-ttu-id="a0614-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0614-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0614-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0614-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0614-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0614-134">INPUTS</span></span>

### <span data-ttu-id="a0614-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a0614-135">System.String</span></span>

### <span data-ttu-id="a0614-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0614-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="a0614-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0614-137">OUTPUTS</span></span>

### <span data-ttu-id="a0614-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0614-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="a0614-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0614-139">NOTES</span></span>

## <span data-ttu-id="a0614-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0614-140">RELATED LINKS</span></span>
