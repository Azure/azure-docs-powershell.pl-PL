---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219668"
---
# <span data-ttu-id="c31b0-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="c31b0-101">Select-AzProfile</span></span>

## <span data-ttu-id="c31b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c31b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c31b0-103">W przypadku modułów obsługujących wiele profilów usługi — Załaduj polecenia cmdlet odpowiadające danemu profilowi usługi.</span><span class="sxs-lookup"><span data-stu-id="c31b0-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="c31b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c31b0-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c31b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c31b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c31b0-106">W przypadku modułów obsługujących wiele profilów usługi — Załaduj polecenia cmdlet odpowiadające danemu profilowi usługi.</span><span class="sxs-lookup"><span data-stu-id="c31b0-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="c31b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c31b0-107">EXAMPLES</span></span>

### <span data-ttu-id="c31b0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c31b0-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="c31b0-109">Załaduj polecenia cmdlet dla profilu AzureStack z marca 2019</span><span class="sxs-lookup"><span data-stu-id="c31b0-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="c31b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c31b0-110">PARAMETERS</span></span>

### <span data-ttu-id="c31b0-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c31b0-111">-Name</span></span>
<span data-ttu-id="c31b0-112">Nazwa profilu do wybrania</span><span class="sxs-lookup"><span data-stu-id="c31b0-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c31b0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c31b0-113">-PassThru</span></span>
<span data-ttu-id="c31b0-114">Gdy jest obecny, wymusza, aby polecenie cmdlet zwracało wartość w przypadku udanego wykonania</span><span class="sxs-lookup"><span data-stu-id="c31b0-114">When present, forces the cmdlet to return a value on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c31b0-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c31b0-115">-Confirm</span></span>
<span data-ttu-id="c31b0-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31b0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31b0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31b0-117">-WhatIf</span></span>
<span data-ttu-id="c31b0-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31b0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c31b0-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c31b0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31b0-120">CommonParameters</span></span>
<span data-ttu-id="c31b0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31b0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c31b0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31b0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c31b0-123">INPUTS</span></span>

### <span data-ttu-id="c31b0-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c31b0-124">None</span></span>

## <span data-ttu-id="c31b0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c31b0-125">OUTPUTS</span></span>

### <span data-ttu-id="c31b0-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="c31b0-126">System.Object</span></span>
## <span data-ttu-id="c31b0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c31b0-127">NOTES</span></span>

## <span data-ttu-id="c31b0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c31b0-128">RELATED LINKS</span></span>
