---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176683"
---
# <span data-ttu-id="412dd-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="412dd-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="412dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="412dd-102">SYNOPSIS</span></span>
<span data-ttu-id="412dd-103">Pobiera poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="412dd-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="412dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="412dd-104">SYNTAX</span></span>

### <span data-ttu-id="412dd-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="412dd-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="412dd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="412dd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="412dd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="412dd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="412dd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="412dd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="412dd-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="412dd-109">DESCRIPTION</span></span>
<span data-ttu-id="412dd-110">Polecenie **cmdlet Get-AzStackEdgeStorageAccountCredential** pobiera poświadczenia konta magazynu dla odpowiedniego konta magazynu na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="412dd-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="412dd-111">Możesz określić parametry Nazwa, Nazwa grupy zasobów i Nazwa urządzenia, aby uzyskać informacje o określonym poświadczeń konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="412dd-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="412dd-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="412dd-112">EXAMPLES</span></span>

### <span data-ttu-id="412dd-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="412dd-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="412dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="412dd-114">PARAMETERS</span></span>

### <span data-ttu-id="412dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412dd-115">-DefaultProfile</span></span>
<span data-ttu-id="412dd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="412dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412dd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="412dd-117">-DeviceName</span></span>
<span data-ttu-id="412dd-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="412dd-118">Device Name</span></span>

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

### <span data-ttu-id="412dd-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="412dd-119">-DeviceObject</span></span>
<span data-ttu-id="412dd-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="412dd-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="412dd-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="412dd-121">-Name</span></span>
<span data-ttu-id="412dd-122">Nazwa konta miejsca do magazynowania, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="412dd-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="412dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="412dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="412dd-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="412dd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="412dd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="412dd-125">-ResourceId</span></span>
<span data-ttu-id="412dd-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="412dd-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="412dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412dd-127">CommonParameters</span></span>
<span data-ttu-id="412dd-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412dd-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="412dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412dd-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="412dd-130">INPUTS</span></span>

### <span data-ttu-id="412dd-131">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="412dd-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="412dd-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="412dd-132">OUTPUTS</span></span>

### <span data-ttu-id="412dd-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="412dd-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="412dd-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="412dd-134">NOTES</span></span>

## <span data-ttu-id="412dd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="412dd-135">RELATED LINKS</span></span>
