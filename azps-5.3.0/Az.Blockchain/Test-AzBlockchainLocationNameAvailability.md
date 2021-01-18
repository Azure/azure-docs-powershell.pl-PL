---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504246"
---
# <span data-ttu-id="50fa5-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="50fa5-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="50fa5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="50fa5-103">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="50fa5-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="50fa5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50fa5-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50fa5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="50fa5-106">Aby sprawdzić, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="50fa5-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="50fa5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50fa5-107">EXAMPLES</span></span>

### <span data-ttu-id="50fa5-108">Przykład 1. Sprawdź, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="50fa5-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="50fa5-109">Polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="50fa5-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="50fa5-110">Przykład 2: Sprawdzanie, czy nazwa zasobu jest dostępna</span><span class="sxs-lookup"><span data-stu-id="50fa5-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="50fa5-111">Polecenie sprawdza, czy nazwa zasobu jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="50fa5-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="50fa5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50fa5-112">PARAMETERS</span></span>

### <span data-ttu-id="50fa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fa5-113">-DefaultProfile</span></span>
<span data-ttu-id="50fa5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50fa5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50fa5-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="50fa5-115">-Location</span></span>
<span data-ttu-id="50fa5-116">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="50fa5-116">Location Name.</span></span>

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

### <span data-ttu-id="50fa5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50fa5-117">-Name</span></span>
<span data-ttu-id="50fa5-118">Pobiera lub ustawia nazwę do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="50fa5-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="50fa5-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="50fa5-119">-SubscriptionId</span></span>
<span data-ttu-id="50fa5-120">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="50fa5-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="50fa5-121">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="50fa5-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="50fa5-122">-Type</span><span class="sxs-lookup"><span data-stu-id="50fa5-122">-Type</span></span>
<span data-ttu-id="50fa5-123">Pobiera lub ustawia typ zasobu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="50fa5-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="50fa5-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50fa5-124">-Confirm</span></span>
<span data-ttu-id="50fa5-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50fa5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fa5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fa5-126">-WhatIf</span></span>
<span data-ttu-id="50fa5-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50fa5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fa5-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50fa5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fa5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fa5-129">CommonParameters</span></span>
<span data-ttu-id="50fa5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fa5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fa5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50fa5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fa5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50fa5-132">INPUTS</span></span>

## <span data-ttu-id="50fa5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50fa5-133">OUTPUTS</span></span>

### <span data-ttu-id="50fa5-134">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="50fa5-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="50fa5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50fa5-135">NOTES</span></span>

<span data-ttu-id="50fa5-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="50fa5-136">ALIASES</span></span>

## <span data-ttu-id="50fa5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50fa5-137">RELATED LINKS</span></span>

