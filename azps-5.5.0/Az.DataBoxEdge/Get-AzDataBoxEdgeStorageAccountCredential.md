---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242866"
---
# <span data-ttu-id="bc3d1-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bc3d1-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bc3d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3d1-103">Pobiera poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="bc3d1-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="bc3d1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc3d1-104">SYNTAX</span></span>

### <span data-ttu-id="bc3d1-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bc3d1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3d1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3d1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc3d1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3d1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3d1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3d1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="bc3d1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc3d1-109">DESCRIPTION</span></span>
<span data-ttu-id="bc3d1-110">Polecenie **cmdlet Get-AzDataBoxEdgeStorageAccountCredential** pobiera poświadczenia konta magazynu dla odpowiedniego konta magazynu na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="bc3d1-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="bc3d1-111">Możesz określić parametry Nazwa, Nazwa grupy zasobów i Nazwa urządzenia, aby uzyskać informacje o określonym poświadczeń konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="bc3d1-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="bc3d1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc3d1-112">EXAMPLES</span></span>

### <span data-ttu-id="bc3d1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc3d1-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="bc3d1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc3d1-114">PARAMETERS</span></span>

### <span data-ttu-id="bc3d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3d1-115">-DefaultProfile</span></span>
<span data-ttu-id="bc3d1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc3d1-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bc3d1-117">-DeviceName</span></span>
<span data-ttu-id="bc3d1-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="bc3d1-118">Device Name</span></span>

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

### <span data-ttu-id="bc3d1-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bc3d1-119">-DeviceObject</span></span>
<span data-ttu-id="bc3d1-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="bc3d1-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="bc3d1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc3d1-121">-Name</span></span>
<span data-ttu-id="bc3d1-122">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="bc3d1-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="bc3d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc3d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc3d1-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bc3d1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bc3d1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc3d1-125">-ResourceId</span></span>
<span data-ttu-id="bc3d1-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc3d1-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bc3d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3d1-127">CommonParameters</span></span>
<span data-ttu-id="bc3d1-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3d1-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc3d1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3d1-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc3d1-130">INPUTS</span></span>

### <span data-ttu-id="bc3d1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bc3d1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bc3d1-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc3d1-132">OUTPUTS</span></span>

### <span data-ttu-id="bc3d1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bc3d1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bc3d1-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc3d1-134">NOTES</span></span>

## <span data-ttu-id="bc3d1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc3d1-135">RELATED LINKS</span></span>
