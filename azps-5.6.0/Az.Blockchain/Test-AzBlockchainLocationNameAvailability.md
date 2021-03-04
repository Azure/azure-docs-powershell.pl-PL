---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969658"
---
# <span data-ttu-id="9d045-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9d045-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="9d045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d045-102">SYNOPSIS</span></span>
<span data-ttu-id="9d045-103">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="9d045-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="9d045-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d045-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d045-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d045-105">DESCRIPTION</span></span>
<span data-ttu-id="9d045-106">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="9d045-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="9d045-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d045-107">EXAMPLES</span></span>

### <span data-ttu-id="9d045-108">Przykład 1. Sprawdzanie, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="9d045-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="9d045-109">To polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="9d045-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="9d045-110">Przykład 2. Sprawdzanie, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="9d045-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="9d045-111">To polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="9d045-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="9d045-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d045-112">PARAMETERS</span></span>

### <span data-ttu-id="9d045-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d045-113">-DefaultProfile</span></span>
<span data-ttu-id="9d045-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d045-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d045-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9d045-115">-Location</span></span>
<span data-ttu-id="9d045-116">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9d045-116">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d045-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d045-117">-Name</span></span>
<span data-ttu-id="9d045-118">Pobiera lub ustawia nazwę do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="9d045-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="9d045-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d045-119">-SubscriptionId</span></span>
<span data-ttu-id="9d045-120">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d045-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d045-121">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9d045-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d045-122">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="9d045-122">-Type</span></span>
<span data-ttu-id="9d045-123">Pobiera lub ustawia typ zasobu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="9d045-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="9d045-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d045-124">-Confirm</span></span>
<span data-ttu-id="9d045-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d045-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d045-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d045-126">-WhatIf</span></span>
<span data-ttu-id="9d045-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d045-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d045-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d045-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d045-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d045-129">CommonParameters</span></span>
<span data-ttu-id="9d045-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d045-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d045-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d045-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d045-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d045-132">INPUTS</span></span>

## <span data-ttu-id="9d045-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d045-133">OUTPUTS</span></span>

### <span data-ttu-id="9d045-134">Microsoft.Azure.PowerShell.cmdlet.zyk.models.api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="9d045-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="9d045-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d045-135">NOTES</span></span>

<span data-ttu-id="9d045-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9d045-136">ALIASES</span></span>

## <span data-ttu-id="9d045-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d045-137">RELATED LINKS</span></span>

