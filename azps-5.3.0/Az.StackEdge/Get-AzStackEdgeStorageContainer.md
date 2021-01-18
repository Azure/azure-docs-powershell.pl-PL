---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502749"
---
# <span data-ttu-id="be004-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="be004-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="be004-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be004-102">SYNOPSIS</span></span>
<span data-ttu-id="be004-103">Pobiera kontenery dla konta magazynu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="be004-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="be004-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be004-104">SYNTAX</span></span>

### <span data-ttu-id="be004-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be004-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be004-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be004-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be004-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be004-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be004-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be004-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="be004-109">Opis</span><span class="sxs-lookup"><span data-stu-id="be004-109">DESCRIPTION</span></span>
<span data-ttu-id="be004-110">Polecenie cmdlet **Get-AzStackEdgeStorageContainer** Pobiera kontener magazynu dla konta magazynu Edge na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="be004-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="be004-111">Możesz określić nazwę jako parametr w poleceniu cmdlet, aby pobrać szczegóły określonego kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="be004-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="be004-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be004-112">EXAMPLES</span></span>

### <span data-ttu-id="be004-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be004-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="be004-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be004-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="be004-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="be004-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="be004-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be004-116">PARAMETERS</span></span>

### <span data-ttu-id="be004-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be004-117">-DefaultProfile</span></span>
<span data-ttu-id="be004-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be004-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be004-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="be004-119">-DeviceName</span></span>
<span data-ttu-id="be004-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="be004-120">Device Name</span></span>

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

### <span data-ttu-id="be004-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="be004-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="be004-122">Podaj nazwę istniejącego EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="be004-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="be004-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="be004-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="be004-124">Dostarczenie istniejącego obiektu EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="be004-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="be004-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be004-125">-Name</span></span>
<span data-ttu-id="be004-126">Nazwa EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="be004-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="be004-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be004-127">-ResourceGroupName</span></span>
<span data-ttu-id="be004-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="be004-128">Resource Group Name</span></span>

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

### <span data-ttu-id="be004-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be004-129">-ResourceId</span></span>
<span data-ttu-id="be004-130">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="be004-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="be004-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be004-131">CommonParameters</span></span>
<span data-ttu-id="be004-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be004-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be004-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be004-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be004-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be004-134">INPUTS</span></span>

### <span data-ttu-id="be004-135">System. String</span><span class="sxs-lookup"><span data-stu-id="be004-135">System.String</span></span>

### <span data-ttu-id="be004-136">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="be004-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="be004-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be004-137">OUTPUTS</span></span>

### <span data-ttu-id="be004-138">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="be004-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="be004-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be004-139">NOTES</span></span>

## <span data-ttu-id="be004-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be004-140">RELATED LINKS</span></span>
