---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499142"
---
# <span data-ttu-id="7ab23-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="7ab23-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="7ab23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ab23-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab23-103">Tworzenie obiektu w pamięci dla DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab23-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7ab23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ab23-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="7ab23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ab23-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab23-106">Tworzenie obiektu w pamięci dla DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab23-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7ab23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ab23-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab23-108">Przykład 1. Tworzenie DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="7ab23-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="7ab23-109">Tworzenie DigitalTwinsIdentityObject według identyfikatora i lokalizacji</span><span class="sxs-lookup"><span data-stu-id="7ab23-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="7ab23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ab23-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab23-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7ab23-111">-EndpointName</span></span>
<span data-ttu-id="7ab23-112">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7ab23-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="7ab23-113">-ID</span><span class="sxs-lookup"><span data-stu-id="7ab23-113">-Id</span></span>
<span data-ttu-id="7ab23-114">Ścieżka tożsamości zasobu.</span><span class="sxs-lookup"><span data-stu-id="7ab23-114">Resource identity path.</span></span>

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

### <span data-ttu-id="7ab23-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7ab23-115">-Location</span></span>
<span data-ttu-id="7ab23-116">Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7ab23-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7ab23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab23-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ab23-118">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7ab23-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7ab23-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7ab23-119">-ResourceName</span></span>
<span data-ttu-id="7ab23-120">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7ab23-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7ab23-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7ab23-121">-SubscriptionId</span></span>
<span data-ttu-id="7ab23-122">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7ab23-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="7ab23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab23-123">CommonParameters</span></span>
<span data-ttu-id="7ab23-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab23-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ab23-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab23-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ab23-126">INPUTS</span></span>

## <span data-ttu-id="7ab23-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ab23-127">OUTPUTS</span></span>

### <span data-ttu-id="7ab23-128">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab23-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7ab23-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ab23-129">NOTES</span></span>

<span data-ttu-id="7ab23-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7ab23-130">ALIASES</span></span>

## <span data-ttu-id="7ab23-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ab23-131">RELATED LINKS</span></span>

