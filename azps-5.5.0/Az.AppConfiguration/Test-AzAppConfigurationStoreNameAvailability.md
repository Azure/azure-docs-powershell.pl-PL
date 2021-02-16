---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195330"
---
# <span data-ttu-id="c2101-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c2101-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="c2101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2101-102">SYNOPSIS</span></span>
<span data-ttu-id="c2101-103">Sprawdza, czy nazwa magazynu konfiguracji jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="c2101-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="c2101-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2101-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2101-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2101-105">DESCRIPTION</span></span>
<span data-ttu-id="c2101-106">Sprawdza, czy nazwa magazynu konfiguracji jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="c2101-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="c2101-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2101-107">EXAMPLES</span></span>

### <span data-ttu-id="c2101-108">Przykład 1. Testowanie dostępności nazwy sklepu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2101-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="c2101-109">To polecenie sprawdza dostępność nazwy magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c2101-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="c2101-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2101-110">PARAMETERS</span></span>

### <span data-ttu-id="c2101-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2101-111">-DefaultProfile</span></span>
<span data-ttu-id="c2101-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2101-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2101-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2101-113">-Name</span></span>
<span data-ttu-id="c2101-114">Nazwa do sprawdzenia dostępności.</span><span class="sxs-lookup"><span data-stu-id="c2101-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="c2101-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2101-115">-SubscriptionId</span></span>
<span data-ttu-id="c2101-116">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2101-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="c2101-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2101-117">-Confirm</span></span>
<span data-ttu-id="c2101-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2101-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2101-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2101-119">-WhatIf</span></span>
<span data-ttu-id="c2101-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2101-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2101-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2101-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2101-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2101-122">CommonParameters</span></span>
<span data-ttu-id="c2101-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2101-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2101-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2101-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2101-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2101-125">INPUTS</span></span>

## <span data-ttu-id="c2101-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2101-126">OUTPUTS</span></span>

### <span data-ttu-id="c2101-127">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="c2101-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="c2101-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2101-128">NOTES</span></span>

<span data-ttu-id="c2101-129">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c2101-129">ALIASES</span></span>

## <span data-ttu-id="c2101-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2101-130">RELATED LINKS</span></span>

