---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177938"
---
# <span data-ttu-id="56926-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56926-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="56926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56926-102">SYNOPSIS</span></span>
<span data-ttu-id="56926-103">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="56926-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="56926-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56926-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56926-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="56926-105">DESCRIPTION</span></span>
<span data-ttu-id="56926-106">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="56926-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="56926-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56926-107">EXAMPLES</span></span>

### <span data-ttu-id="56926-108">Przykład 1. Sprawdzanie, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="56926-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="56926-109">To polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="56926-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="56926-110">Przykład 2. Sprawdzanie, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="56926-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="56926-111">To polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="56926-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="56926-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56926-112">PARAMETERS</span></span>

### <span data-ttu-id="56926-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56926-113">-DefaultProfile</span></span>
<span data-ttu-id="56926-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56926-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56926-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="56926-115">-Location</span></span>
<span data-ttu-id="56926-116">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="56926-116">Location Name.</span></span>

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

### <span data-ttu-id="56926-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56926-117">-Name</span></span>
<span data-ttu-id="56926-118">Pobiera lub ustawia nazwę do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="56926-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="56926-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56926-119">-SubscriptionId</span></span>
<span data-ttu-id="56926-120">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56926-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56926-121">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="56926-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="56926-122">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="56926-122">-Type</span></span>
<span data-ttu-id="56926-123">Pobiera lub ustawia typ zasobu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="56926-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="56926-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56926-124">-Confirm</span></span>
<span data-ttu-id="56926-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56926-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56926-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56926-126">-WhatIf</span></span>
<span data-ttu-id="56926-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56926-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56926-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56926-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56926-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56926-129">CommonParameters</span></span>
<span data-ttu-id="56926-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56926-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56926-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56926-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56926-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56926-132">INPUTS</span></span>

## <span data-ttu-id="56926-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56926-133">OUTPUTS</span></span>

### <span data-ttu-id="56926-134">Microsoft.Azure.PowerShell.cmdlet.u20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="56926-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="56926-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56926-135">NOTES</span></span>

<span data-ttu-id="56926-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="56926-136">ALIASES</span></span>

## <span data-ttu-id="56926-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56926-137">RELATED LINKS</span></span>

