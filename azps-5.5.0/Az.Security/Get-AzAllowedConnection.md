---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178610"
---
# <span data-ttu-id="8fe91-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="8fe91-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="8fe91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe91-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe91-103">Umożliwia wyświetlanie dozwolonego ruchu między zasobami dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8fe91-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="8fe91-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8fe91-104">SYNTAX</span></span>

### <span data-ttu-id="8fe91-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8fe91-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe91-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8fe91-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe91-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe91-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fe91-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8fe91-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe91-109">Pobiera listę całego możliwego ruchu między zasobami dla subskrypcji i lokalizacji w zależności od typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="8fe91-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="8fe91-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8fe91-110">EXAMPLES</span></span>

### <span data-ttu-id="8fe91-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fe91-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="8fe91-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8fe91-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="8fe91-113">Pobiera listę całego możliwego ruchu między zasobami dla subskrypcji i lokalizacji na podstawie typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="8fe91-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="8fe91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fe91-114">PARAMETERS</span></span>

### <span data-ttu-id="8fe91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe91-115">-DefaultProfile</span></span>
<span data-ttu-id="8fe91-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe91-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fe91-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8fe91-117">-Location</span></span>
<span data-ttu-id="8fe91-118">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="8fe91-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe91-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8fe91-119">-Name</span></span>
<span data-ttu-id="8fe91-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8fe91-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe91-121">-ResourceGroupName</span></span>
<span data-ttu-id="8fe91-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8fe91-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe91-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe91-123">-ResourceId</span></span>
<span data-ttu-id="8fe91-124">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="8fe91-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe91-125">CommonParameters</span></span>
<span data-ttu-id="8fe91-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe91-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe91-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe91-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fe91-128">INPUTS</span></span>

### <span data-ttu-id="8fe91-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe91-129">System.String</span></span>

## <span data-ttu-id="8fe91-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8fe91-130">OUTPUTS</span></span>

### <span data-ttu-id="8fe91-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="8fe91-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="8fe91-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8fe91-132">NOTES</span></span>

## <span data-ttu-id="8fe91-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fe91-133">RELATED LINKS</span></span>
