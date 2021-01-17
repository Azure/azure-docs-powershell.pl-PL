---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347014"
---
# <span data-ttu-id="93b7b-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="93b7b-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="93b7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="93b7b-103">Tworzenie obiektu w pamięci dla DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="93b7b-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93b7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93b7b-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="93b7b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="93b7b-106">Tworzenie obiektu w pamięci dla DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="93b7b-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93b7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="93b7b-108">Przykład 1. Tworzenie DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="93b7b-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="93b7b-109">Tworzenie DigitalTwinsIdentityObject według identyfikatora i lokalizacji</span><span class="sxs-lookup"><span data-stu-id="93b7b-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="93b7b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93b7b-110">PARAMETERS</span></span>

### <span data-ttu-id="93b7b-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="93b7b-111">-EndpointName</span></span>
<span data-ttu-id="93b7b-112">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="93b7b-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="93b7b-113">-ID</span><span class="sxs-lookup"><span data-stu-id="93b7b-113">-Id</span></span>
<span data-ttu-id="93b7b-114">Ścieżka tożsamości zasobu.</span><span class="sxs-lookup"><span data-stu-id="93b7b-114">Resource identity path.</span></span>

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

### <span data-ttu-id="93b7b-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="93b7b-115">-Location</span></span>
<span data-ttu-id="93b7b-116">Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="93b7b-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93b7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="93b7b-118">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="93b7b-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93b7b-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93b7b-119">-ResourceName</span></span>
<span data-ttu-id="93b7b-120">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="93b7b-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93b7b-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="93b7b-121">-SubscriptionId</span></span>
<span data-ttu-id="93b7b-122">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="93b7b-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="93b7b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b7b-123">CommonParameters</span></span>
<span data-ttu-id="93b7b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b7b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b7b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93b7b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b7b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93b7b-126">INPUTS</span></span>

## <span data-ttu-id="93b7b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93b7b-127">OUTPUTS</span></span>

### <span data-ttu-id="93b7b-128">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="93b7b-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93b7b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93b7b-129">NOTES</span></span>

<span data-ttu-id="93b7b-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="93b7b-130">ALIASES</span></span>

## <span data-ttu-id="93b7b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93b7b-131">RELATED LINKS</span></span>

