---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195339"
---
# <span data-ttu-id="86623-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="86623-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="86623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86623-102">SYNOPSIS</span></span>
<span data-ttu-id="86623-103">Wyświetla klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="86623-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="86623-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="86623-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86623-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="86623-105">DESCRIPTION</span></span>
<span data-ttu-id="86623-106">Wyświetla klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="86623-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="86623-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="86623-107">EXAMPLES</span></span>

### <span data-ttu-id="86623-108">Przykład 1. Lista wszystkich kluczy sklepu z konfiguracją aplikacji</span><span class="sxs-lookup"><span data-stu-id="86623-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="86623-109">To polecenie zawiera listę wszystkich kluczy magazynu magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86623-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="86623-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86623-110">PARAMETERS</span></span>

### <span data-ttu-id="86623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86623-111">-DefaultProfile</span></span>
<span data-ttu-id="86623-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="86623-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86623-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="86623-113">-Name</span></span>
<span data-ttu-id="86623-114">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="86623-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="86623-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86623-115">-ResourceGroupName</span></span>
<span data-ttu-id="86623-116">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="86623-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="86623-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86623-117">-SubscriptionId</span></span>
<span data-ttu-id="86623-118">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="86623-118">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="86623-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86623-119">-Confirm</span></span>
<span data-ttu-id="86623-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86623-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86623-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86623-121">-WhatIf</span></span>
<span data-ttu-id="86623-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86623-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86623-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="86623-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86623-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86623-124">CommonParameters</span></span>
<span data-ttu-id="86623-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86623-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86623-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86623-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86623-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86623-127">INPUTS</span></span>

## <span data-ttu-id="86623-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86623-128">OUTPUTS</span></span>

### <span data-ttu-id="86623-129">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="86623-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="86623-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="86623-130">NOTES</span></span>

<span data-ttu-id="86623-131">ALIASY</span><span class="sxs-lookup"><span data-stu-id="86623-131">ALIASES</span></span>

## <span data-ttu-id="86623-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86623-132">RELATED LINKS</span></span>

