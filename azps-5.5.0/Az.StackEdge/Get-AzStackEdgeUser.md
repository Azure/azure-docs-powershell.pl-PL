---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183219"
---
# <span data-ttu-id="8230d-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8230d-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="8230d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8230d-102">SYNOPSIS</span></span>
<span data-ttu-id="8230d-103">Pobiera użytkowników skonfigurowanych dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="8230d-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="8230d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8230d-104">SYNTAX</span></span>

### <span data-ttu-id="8230d-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8230d-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8230d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8230d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8230d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8230d-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8230d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8230d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8230d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8230d-109">DESCRIPTION</span></span>
<span data-ttu-id="8230d-110">Polecenie **cmdlet Get-AzStackEdgeUser** wyświetla listę użytkowników skonfigurowanych dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="8230d-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="8230d-111">Możesz wspomnieć nazwę w parametrach, aby uzyskać szczegółowe informacje o określonym użytkowniku.</span><span class="sxs-lookup"><span data-stu-id="8230d-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="8230d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8230d-112">EXAMPLES</span></span>

### <span data-ttu-id="8230d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8230d-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="8230d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8230d-114">PARAMETERS</span></span>

### <span data-ttu-id="8230d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8230d-115">-DefaultProfile</span></span>
<span data-ttu-id="8230d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8230d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8230d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8230d-117">-DeviceName</span></span>
<span data-ttu-id="8230d-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="8230d-118">Device Name</span></span>

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

### <span data-ttu-id="8230d-119">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8230d-119">-DeviceObject</span></span>
<span data-ttu-id="8230d-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="8230d-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8230d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8230d-121">-Name</span></span>
<span data-ttu-id="8230d-122">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="8230d-122">Username</span></span>

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

### <span data-ttu-id="8230d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8230d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8230d-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8230d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8230d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8230d-125">-ResourceId</span></span>
<span data-ttu-id="8230d-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8230d-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8230d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8230d-127">CommonParameters</span></span>
<span data-ttu-id="8230d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8230d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8230d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8230d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8230d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8230d-130">INPUTS</span></span>

### <span data-ttu-id="8230d-131">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8230d-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="8230d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8230d-132">OUTPUTS</span></span>

### <span data-ttu-id="8230d-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8230d-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="8230d-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8230d-134">NOTES</span></span>

## <span data-ttu-id="8230d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8230d-135">RELATED LINKS</span></span>
