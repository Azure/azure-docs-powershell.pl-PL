---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063231"
---
# <span data-ttu-id="792b6-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="792b6-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="792b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="792b6-102">SYNOPSIS</span></span>
<span data-ttu-id="792b6-103">Służy do wyświetlania dozwolonego ruchu między zasobami dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="792b6-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="792b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="792b6-104">SYNTAX</span></span>

### <span data-ttu-id="792b6-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="792b6-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792b6-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="792b6-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792b6-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="792b6-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="792b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="792b6-108">DESCRIPTION</span></span>
<span data-ttu-id="792b6-109">Pobiera listę wszystkich możliwych danych między zasobami dla subskrypcji i lokalizacji na podstawie typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="792b6-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="792b6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="792b6-110">EXAMPLES</span></span>

### <span data-ttu-id="792b6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="792b6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="792b6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="792b6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="792b6-113">Pobiera listę wszystkich możliwych danych między zasobami dla subskrypcji i lokalizacji na podstawie typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="792b6-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="792b6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="792b6-114">PARAMETERS</span></span>

### <span data-ttu-id="792b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792b6-115">-DefaultProfile</span></span>
<span data-ttu-id="792b6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="792b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792b6-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="792b6-117">-Location</span></span>
<span data-ttu-id="792b6-118">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="792b6-118">Location.</span></span>

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

### <span data-ttu-id="792b6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="792b6-119">-Name</span></span>
<span data-ttu-id="792b6-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="792b6-120">Resource name.</span></span>

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

### <span data-ttu-id="792b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="792b6-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="792b6-122">Resource group name.</span></span>

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

### <span data-ttu-id="792b6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="792b6-123">-ResourceId</span></span>
<span data-ttu-id="792b6-124">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="792b6-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="792b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792b6-125">CommonParameters</span></span>
<span data-ttu-id="792b6-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792b6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792b6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792b6-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="792b6-128">INPUTS</span></span>

### <span data-ttu-id="792b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="792b6-129">System.String</span></span>

## <span data-ttu-id="792b6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="792b6-130">OUTPUTS</span></span>

### <span data-ttu-id="792b6-131">Microsoft. Azure. Commands. Security. models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="792b6-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="792b6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="792b6-132">NOTES</span></span>

## <span data-ttu-id="792b6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="792b6-133">RELATED LINKS</span></span>
