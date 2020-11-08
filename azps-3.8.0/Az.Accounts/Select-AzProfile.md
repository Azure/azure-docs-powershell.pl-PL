---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050187"
---
# <span data-ttu-id="dd344-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="dd344-101">Select-AzProfile</span></span>

## <span data-ttu-id="dd344-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd344-102">SYNOPSIS</span></span>
<span data-ttu-id="dd344-103">W przypadku modułów obsługujących wiele profilów usługi — Załaduj polecenia cmdlet odpowiadające danemu profilowi usługi.</span><span class="sxs-lookup"><span data-stu-id="dd344-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="dd344-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd344-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd344-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd344-105">DESCRIPTION</span></span>
<span data-ttu-id="dd344-106">W przypadku modułów obsługujących wiele profilów usługi — Załaduj polecenia cmdlet odpowiadające danemu profilowi usługi.</span><span class="sxs-lookup"><span data-stu-id="dd344-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="dd344-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd344-107">EXAMPLES</span></span>

### <span data-ttu-id="dd344-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd344-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="dd344-109">Załaduj polecenia cmdlet dla profilu AzureStack z marca 2019</span><span class="sxs-lookup"><span data-stu-id="dd344-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="dd344-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd344-110">PARAMETERS</span></span>

### <span data-ttu-id="dd344-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd344-111">-Name</span></span>
<span data-ttu-id="dd344-112">Nazwa profilu do wybrania</span><span class="sxs-lookup"><span data-stu-id="dd344-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="dd344-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd344-113">-PassThru</span></span>
<span data-ttu-id="dd344-114">Gdy jest obecny, wymusza, aby polecenie cmdlet zwracało wartość w przypadku udanego wykonania</span><span class="sxs-lookup"><span data-stu-id="dd344-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="dd344-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd344-115">-Confirm</span></span>
<span data-ttu-id="dd344-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd344-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd344-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd344-117">-WhatIf</span></span>
<span data-ttu-id="dd344-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd344-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd344-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd344-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd344-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd344-120">CommonParameters</span></span>
<span data-ttu-id="dd344-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd344-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd344-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd344-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd344-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd344-123">INPUTS</span></span>

### <span data-ttu-id="dd344-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dd344-124">None</span></span>

## <span data-ttu-id="dd344-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd344-125">OUTPUTS</span></span>

### <span data-ttu-id="dd344-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="dd344-126">System.Object</span></span>
## <span data-ttu-id="dd344-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd344-127">NOTES</span></span>

## <span data-ttu-id="dd344-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd344-128">RELATED LINKS</span></span>
