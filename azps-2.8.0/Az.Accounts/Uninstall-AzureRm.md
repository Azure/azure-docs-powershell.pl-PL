---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: d2e495b58e68232bf20bd309d06207cd45cd427e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707188"
---
# <span data-ttu-id="23d89-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="23d89-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="23d89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23d89-102">SYNOPSIS</span></span>
<span data-ttu-id="23d89-103">Usuwa wszystkie moduły AzureRm z komputera.</span><span class="sxs-lookup"><span data-stu-id="23d89-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="23d89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23d89-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23d89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23d89-105">DESCRIPTION</span></span>
<span data-ttu-id="23d89-106">Usuwa wszystkie moduły AzureRm z komputera.</span><span class="sxs-lookup"><span data-stu-id="23d89-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="23d89-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23d89-107">EXAMPLES</span></span>

### <span data-ttu-id="23d89-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23d89-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="23d89-109">Uruchomienie tego polecenia spowoduje usunięcie wszystkich modułów AzureRm z komputera dla wersji programu PowerShell, w której jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d89-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="23d89-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23d89-110">PARAMETERS</span></span>

### <span data-ttu-id="23d89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d89-111">-DefaultProfile</span></span>
<span data-ttu-id="23d89-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23d89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d89-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23d89-113">-PassThru</span></span>
<span data-ttu-id="23d89-114">Zwracana lista modułów, które zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="23d89-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="23d89-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23d89-115">-Confirm</span></span>
<span data-ttu-id="23d89-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d89-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d89-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d89-117">-WhatIf</span></span>
<span data-ttu-id="23d89-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d89-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d89-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23d89-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d89-120">CommonParameters</span></span>
<span data-ttu-id="23d89-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d89-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d89-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d89-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23d89-123">INPUTS</span></span>

### <span data-ttu-id="23d89-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="23d89-124">None</span></span>

## <span data-ttu-id="23d89-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23d89-125">OUTPUTS</span></span>

### <span data-ttu-id="23d89-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23d89-126">System.String</span></span>

## <span data-ttu-id="23d89-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23d89-127">NOTES</span></span>

## <span data-ttu-id="23d89-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23d89-128">RELATED LINKS</span></span>