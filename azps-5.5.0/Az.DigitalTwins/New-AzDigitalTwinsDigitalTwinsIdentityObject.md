---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243714"
---
# <span data-ttu-id="df635-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="df635-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="df635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df635-102">SYNOPSIS</span></span>
<span data-ttu-id="df635-103">Tworzenie obiektu w pamięci dla obiektu DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="df635-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="df635-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df635-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="df635-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="df635-105">DESCRIPTION</span></span>
<span data-ttu-id="df635-106">Tworzenie obiektu w pamięci na platformie DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="df635-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="df635-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df635-107">EXAMPLES</span></span>

### <span data-ttu-id="df635-108">Przykład 1. Tworzenie digitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="df635-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="df635-109">Tworzenie dokumentu DigitalTwinsIdentityObject według identyfikatora i lokalizacji</span><span class="sxs-lookup"><span data-stu-id="df635-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="df635-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df635-110">PARAMETERS</span></span>

### <span data-ttu-id="df635-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="df635-111">-EndpointName</span></span>
<span data-ttu-id="df635-112">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="df635-112">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-113">— Id</span><span class="sxs-lookup"><span data-stu-id="df635-113">-Id</span></span>
<span data-ttu-id="df635-114">Ścieżka tożsamości zasobu.</span><span class="sxs-lookup"><span data-stu-id="df635-114">Resource identity path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="df635-115">-Location</span></span>
<span data-ttu-id="df635-116">Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="df635-116">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df635-117">-ResourceGroupName</span></span>
<span data-ttu-id="df635-118">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="df635-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="df635-119">-ResourceName</span></span>
<span data-ttu-id="df635-120">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="df635-120">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df635-121">-SubscriptionId</span></span>
<span data-ttu-id="df635-122">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="df635-122">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df635-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df635-123">CommonParameters</span></span>
<span data-ttu-id="df635-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df635-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df635-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df635-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df635-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df635-126">INPUTS</span></span>

## <span data-ttu-id="df635-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df635-127">OUTPUTS</span></span>

### <span data-ttu-id="df635-128">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="df635-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="df635-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df635-129">NOTES</span></span>

<span data-ttu-id="df635-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="df635-130">ALIASES</span></span>

## <span data-ttu-id="df635-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df635-131">RELATED LINKS</span></span>

