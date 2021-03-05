---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 9d06873954e6a6880965781d2004d8b7b0c35bb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977642"
---
# <span data-ttu-id="a04a6-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a04a6-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="a04a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a04a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a04a6-103">Pobiera użytkowników skonfigurowanych dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a04a6-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="a04a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a04a6-104">SYNTAX</span></span>

### <span data-ttu-id="a04a6-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a04a6-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04a6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a04a6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04a6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a04a6-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04a6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a04a6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a04a6-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a04a6-109">DESCRIPTION</span></span>
<span data-ttu-id="a04a6-110">Polecenie **cmdlet Get-AzStackEdgeUser** wyświetla listę użytkowników skonfigurowanych dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a04a6-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="a04a6-111">Możesz wspomnieć nazwę w parametrach, aby uzyskać szczegółowe informacje o określonym użytkowniku.</span><span class="sxs-lookup"><span data-stu-id="a04a6-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="a04a6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a04a6-112">EXAMPLES</span></span>

### <span data-ttu-id="a04a6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a04a6-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="a04a6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a04a6-114">PARAMETERS</span></span>

### <span data-ttu-id="a04a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04a6-115">-DefaultProfile</span></span>
<span data-ttu-id="a04a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a04a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a04a6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a04a6-117">-DeviceName</span></span>
<span data-ttu-id="a04a6-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a04a6-118">Device Name</span></span>

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

### <span data-ttu-id="a04a6-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a04a6-119">-DeviceObject</span></span>
<span data-ttu-id="a04a6-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="a04a6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a04a6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a04a6-121">-Name</span></span>
<span data-ttu-id="a04a6-122">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="a04a6-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a04a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a04a6-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a04a6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a04a6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a04a6-125">-ResourceId</span></span>
<span data-ttu-id="a04a6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a04a6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a04a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04a6-127">CommonParameters</span></span>
<span data-ttu-id="a04a6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04a6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a04a6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04a6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a04a6-130">INPUTS</span></span>

### <span data-ttu-id="a04a6-131">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a04a6-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a04a6-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a04a6-132">OUTPUTS</span></span>

### <span data-ttu-id="a04a6-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a04a6-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="a04a6-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a04a6-134">NOTES</span></span>

## <span data-ttu-id="a04a6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a04a6-135">RELATED LINKS</span></span>
