---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322560"
---
# <span data-ttu-id="08ce9-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="08ce9-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="08ce9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="08ce9-103">Wyświetla klucz dostępu do określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="08ce9-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="08ce9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08ce9-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08ce9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="08ce9-106">Wyświetla klucz dostępu do określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="08ce9-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="08ce9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08ce9-107">EXAMPLES</span></span>

### <span data-ttu-id="08ce9-108">Przykład 1: wyświetlanie wszystkich kluczy sklepu w magazynie konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="08ce9-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="08ce9-109">To polecenie zawiera listę wszystkich kluczy sklepu w magazynie konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="08ce9-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="08ce9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08ce9-110">PARAMETERS</span></span>

### <span data-ttu-id="08ce9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ce9-111">-DefaultProfile</span></span>
<span data-ttu-id="08ce9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08ce9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ce9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08ce9-113">-Name</span></span>
<span data-ttu-id="08ce9-114">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="08ce9-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="08ce9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ce9-115">-ResourceGroupName</span></span>
<span data-ttu-id="08ce9-116">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="08ce9-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="08ce9-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="08ce9-117">-SubscriptionId</span></span>
<span data-ttu-id="08ce9-118">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08ce9-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ce9-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08ce9-119">-Confirm</span></span>
<span data-ttu-id="08ce9-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08ce9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ce9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ce9-121">-WhatIf</span></span>
<span data-ttu-id="08ce9-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08ce9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ce9-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08ce9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ce9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ce9-124">CommonParameters</span></span>
<span data-ttu-id="08ce9-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ce9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ce9-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08ce9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ce9-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08ce9-127">INPUTS</span></span>

## <span data-ttu-id="08ce9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08ce9-128">OUTPUTS</span></span>

### <span data-ttu-id="08ce9-129">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="08ce9-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="08ce9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08ce9-130">NOTES</span></span>

<span data-ttu-id="08ce9-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="08ce9-131">ALIASES</span></span>

## <span data-ttu-id="08ce9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08ce9-132">RELATED LINKS</span></span>

