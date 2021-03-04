---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: df65bd7b8dfd2f3091590b8830059965e599c029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975722"
---
# <span data-ttu-id="650b8-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="650b8-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="650b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650b8-102">SYNOPSIS</span></span>
<span data-ttu-id="650b8-103">Tworzenie konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="650b8-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="650b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="650b8-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="650b8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="650b8-105">DESCRIPTION</span></span>
<span data-ttu-id="650b8-106">Utwórz nowe konto renderowania zdalnego w określonej subskrypcji, grupie zasobów i regionie.</span><span class="sxs-lookup"><span data-stu-id="650b8-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="650b8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="650b8-107">EXAMPLES</span></span>

### <span data-ttu-id="650b8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="650b8-108">Example 1</span></span>
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

<span data-ttu-id="650b8-109">Tworzenie nowego "przykładu" dla konta renderowania zdalnego w bieżącej subskrypcji, grupy zasobów "rg1" i środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="650b8-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="650b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650b8-110">PARAMETERS</span></span>

### <span data-ttu-id="650b8-111">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="650b8-111">-Confirm</span></span>
<span data-ttu-id="650b8-112">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="650b8-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650b8-113">-DefaultProfile</span></span>
<span data-ttu-id="650b8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="650b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="650b8-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="650b8-115">-Location</span></span>
<span data-ttu-id="650b8-116">Lokalizacja konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="650b8-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="650b8-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="650b8-117">-Name</span></span>
<span data-ttu-id="650b8-118">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="650b8-118">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="650b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="650b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="650b8-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="650b8-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="650b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650b8-121">-WhatIf</span></span>
<span data-ttu-id="650b8-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="650b8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650b8-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="650b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650b8-124">CommonParameters</span></span>
<span data-ttu-id="650b8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="650b8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="650b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650b8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650b8-127">INPUTS</span></span>

### <span data-ttu-id="650b8-128">Brak</span><span class="sxs-lookup"><span data-stu-id="650b8-128">None</span></span>

## <span data-ttu-id="650b8-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650b8-129">OUTPUTS</span></span>

### <span data-ttu-id="650b8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="650b8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="650b8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="650b8-131">NOTES</span></span>

## <span data-ttu-id="650b8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650b8-132">RELATED LINKS</span></span>
