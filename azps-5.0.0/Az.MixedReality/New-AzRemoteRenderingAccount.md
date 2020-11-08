---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231781"
---
# <span data-ttu-id="a28d1-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="a28d1-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="a28d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a28d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d1-103">Tworzenie konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="a28d1-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="a28d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a28d1-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a28d1-105">DESCRIPTION</span></span>
<span data-ttu-id="a28d1-106">Utwórz nowe konto renderingu zdalnego w pewnych abonamentach, grupach zasobów i regionach.</span><span class="sxs-lookup"><span data-stu-id="a28d1-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="a28d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a28d1-107">EXAMPLES</span></span>

### <span data-ttu-id="a28d1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a28d1-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="a28d1-109">Utwórz nowe konto renderowania zdalnego "przykład" w bieżącym abonamentu, grupie zasobów "RG1" i centrali my.</span><span class="sxs-lookup"><span data-stu-id="a28d1-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="a28d1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a28d1-110">PARAMETERS</span></span>

### <span data-ttu-id="a28d1-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a28d1-111">-Confirm</span></span>
<span data-ttu-id="a28d1-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a28d1-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d1-113">-DefaultProfile</span></span>
<span data-ttu-id="a28d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a28d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a28d1-115">-Location</span></span>
<span data-ttu-id="a28d1-116">Lokalizacja konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="a28d1-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a28d1-117">-Name</span></span>
<span data-ttu-id="a28d1-118">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="a28d1-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="a28d1-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a28d1-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28d1-121">-WhatIf</span></span>
<span data-ttu-id="a28d1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a28d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a28d1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a28d1-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d1-124">CommonParameters</span></span>
<span data-ttu-id="a28d1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a28d1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28d1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a28d1-127">INPUTS</span></span>

### <span data-ttu-id="a28d1-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a28d1-128">None</span></span>

## <span data-ttu-id="a28d1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a28d1-129">OUTPUTS</span></span>

### <span data-ttu-id="a28d1-130">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="a28d1-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="a28d1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a28d1-131">NOTES</span></span>

## <span data-ttu-id="a28d1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a28d1-132">RELATED LINKS</span></span>
