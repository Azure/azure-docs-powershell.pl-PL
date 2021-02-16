---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194899"
---
# <span data-ttu-id="268be-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="268be-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="268be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268be-102">SYNOPSIS</span></span>
<span data-ttu-id="268be-103">Pobiera użytkowników skonfigurowanych dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="268be-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="268be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="268be-104">SYNTAX</span></span>

### <span data-ttu-id="268be-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="268be-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268be-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="268be-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268be-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="268be-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268be-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="268be-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="268be-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="268be-109">DESCRIPTION</span></span>
<span data-ttu-id="268be-110">Polecenie **cmdlet Get-AzDataBoxEdgeUser** wyświetla listę użytkowników skonfigurowanych dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="268be-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="268be-111">Możesz wspomnieć nazwę w parametrach, aby uzyskać szczegółowe informacje o określonym użytkowniku.</span><span class="sxs-lookup"><span data-stu-id="268be-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="268be-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="268be-112">EXAMPLES</span></span>

### <span data-ttu-id="268be-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="268be-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="268be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="268be-114">PARAMETERS</span></span>

### <span data-ttu-id="268be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268be-115">-DefaultProfile</span></span>
<span data-ttu-id="268be-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="268be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268be-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="268be-117">-DeviceName</span></span>
<span data-ttu-id="268be-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="268be-118">Device Name</span></span>

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

### <span data-ttu-id="268be-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="268be-119">-DeviceObject</span></span>
<span data-ttu-id="268be-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="268be-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="268be-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="268be-121">-Name</span></span>
<span data-ttu-id="268be-122">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="268be-122">Username</span></span>

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

### <span data-ttu-id="268be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268be-123">-ResourceGroupName</span></span>
<span data-ttu-id="268be-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="268be-124">Resource Group Name</span></span>

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

### <span data-ttu-id="268be-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="268be-125">-ResourceId</span></span>
<span data-ttu-id="268be-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="268be-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="268be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268be-127">CommonParameters</span></span>
<span data-ttu-id="268be-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268be-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="268be-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268be-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="268be-130">INPUTS</span></span>

### <span data-ttu-id="268be-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="268be-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="268be-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="268be-132">OUTPUTS</span></span>

### <span data-ttu-id="268be-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="268be-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="268be-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="268be-134">NOTES</span></span>

## <span data-ttu-id="268be-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="268be-135">RELATED LINKS</span></span>
