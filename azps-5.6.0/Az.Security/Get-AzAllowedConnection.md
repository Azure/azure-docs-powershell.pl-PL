---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 211601ac2866dab85d46e61cba79ed074f79e22d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969985"
---
# <span data-ttu-id="45ea5-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="45ea5-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="45ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="45ea5-103">Umożliwia wyświetlanie dozwolonego ruchu między zasobami dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="45ea5-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="45ea5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45ea5-104">SYNTAX</span></span>

### <span data-ttu-id="45ea5-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="45ea5-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45ea5-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="45ea5-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45ea5-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45ea5-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45ea5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="45ea5-108">DESCRIPTION</span></span>
<span data-ttu-id="45ea5-109">Pobiera listę całego możliwego ruchu między zasobami dla subskrypcji i lokalizacji na podstawie typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="45ea5-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="45ea5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45ea5-110">EXAMPLES</span></span>

### <span data-ttu-id="45ea5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45ea5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="45ea5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="45ea5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="45ea5-113">Pobiera listę całego możliwego ruchu między zasobami dla subskrypcji i lokalizacji na podstawie typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="45ea5-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="45ea5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45ea5-114">PARAMETERS</span></span>

### <span data-ttu-id="45ea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ea5-115">-DefaultProfile</span></span>
<span data-ttu-id="45ea5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45ea5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ea5-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="45ea5-117">-Location</span></span>
<span data-ttu-id="45ea5-118">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="45ea5-118">Location.</span></span>

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

### <span data-ttu-id="45ea5-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="45ea5-119">-Name</span></span>
<span data-ttu-id="45ea5-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="45ea5-120">Resource name.</span></span>

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

### <span data-ttu-id="45ea5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ea5-121">-ResourceGroupName</span></span>
<span data-ttu-id="45ea5-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45ea5-122">Resource group name.</span></span>

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

### <span data-ttu-id="45ea5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45ea5-123">-ResourceId</span></span>
<span data-ttu-id="45ea5-124">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="45ea5-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="45ea5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ea5-125">CommonParameters</span></span>
<span data-ttu-id="45ea5-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ea5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ea5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ea5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ea5-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45ea5-128">INPUTS</span></span>

### <span data-ttu-id="45ea5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="45ea5-129">System.String</span></span>

## <span data-ttu-id="45ea5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45ea5-130">OUTPUTS</span></span>

### <span data-ttu-id="45ea5-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="45ea5-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="45ea5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45ea5-132">NOTES</span></span>

## <span data-ttu-id="45ea5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45ea5-133">RELATED LINKS</span></span>
