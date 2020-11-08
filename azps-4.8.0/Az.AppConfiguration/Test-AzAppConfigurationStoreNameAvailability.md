---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062450"
---
# <span data-ttu-id="17d1c-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="17d1c-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="17d1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="17d1c-103">Sprawdza, czy nazwa magazynu konfiguracji jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="17d1c-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="17d1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17d1c-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17d1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="17d1c-106">Sprawdza, czy nazwa magazynu konfiguracji jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="17d1c-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="17d1c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17d1c-107">EXAMPLES</span></span>

### <span data-ttu-id="17d1c-108">Przykład 1: testowanie dostępności nazwy magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="17d1c-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="17d1c-109">To polecenie sprawdza dostępność nazwy magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17d1c-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="17d1c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17d1c-110">PARAMETERS</span></span>

### <span data-ttu-id="17d1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d1c-111">-DefaultProfile</span></span>
<span data-ttu-id="17d1c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17d1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17d1c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17d1c-113">-Name</span></span>
<span data-ttu-id="17d1c-114">Nazwa służąca do sprawdzania dostępności.</span><span class="sxs-lookup"><span data-stu-id="17d1c-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="17d1c-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="17d1c-115">-SubscriptionId</span></span>
<span data-ttu-id="17d1c-116">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17d1c-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="17d1c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17d1c-117">-Confirm</span></span>
<span data-ttu-id="17d1c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17d1c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17d1c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d1c-119">-WhatIf</span></span>
<span data-ttu-id="17d1c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17d1c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d1c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17d1c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17d1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d1c-122">CommonParameters</span></span>
<span data-ttu-id="17d1c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17d1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d1c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17d1c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d1c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17d1c-125">INPUTS</span></span>

## <span data-ttu-id="17d1c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17d1c-126">OUTPUTS</span></span>

### <span data-ttu-id="17d1c-127">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="17d1c-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="17d1c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17d1c-128">NOTES</span></span>

<span data-ttu-id="17d1c-129">PISUJE</span><span class="sxs-lookup"><span data-stu-id="17d1c-129">ALIASES</span></span>

## <span data-ttu-id="17d1c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17d1c-130">RELATED LINKS</span></span>

