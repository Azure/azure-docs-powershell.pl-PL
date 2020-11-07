---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 374a43b6b094622808f4704daf7063a4c4c0c153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704764"
---
# <span data-ttu-id="954fe-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="954fe-101">Get-AzDefault</span></span>

## <span data-ttu-id="954fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="954fe-102">SYNOPSIS</span></span>
<span data-ttu-id="954fe-103">Uzyskiwanie wartości domyślnych ustawionych przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="954fe-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="954fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="954fe-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="954fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="954fe-105">DESCRIPTION</span></span>
<span data-ttu-id="954fe-106">Polecenie cmdlet Get-AzDefault pobiera grupę zasobów, którą Użytkownik ustawił jako domyślny w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="954fe-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="954fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="954fe-107">EXAMPLES</span></span>

### <span data-ttu-id="954fe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="954fe-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="954fe-109">To polecenie zwraca bieżące ustawienia domyślne, jeśli są ustawione wartości domyślne, lub zwraca wartość Nothing, jeśli nie ustawiono żadnego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="954fe-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="954fe-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="954fe-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="954fe-111">To polecenie zwraca bieżącą domyślną grupę zasobów, jeśli jest ustawiona wartość domyślna, lub zwraca wartość Nothing, jeśli nie ustawiono żadnego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="954fe-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="954fe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="954fe-112">PARAMETERS</span></span>

### <span data-ttu-id="954fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954fe-113">-DefaultProfile</span></span>
<span data-ttu-id="954fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="954fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="954fe-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="954fe-115">-ResourceGroup</span></span>
<span data-ttu-id="954fe-116">Wyświetl domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="954fe-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954fe-117">CommonParameters</span></span>
<span data-ttu-id="954fe-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954fe-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="954fe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954fe-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="954fe-120">INPUTS</span></span>

### <span data-ttu-id="954fe-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="954fe-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="954fe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="954fe-122">OUTPUTS</span></span>

### <span data-ttu-id="954fe-123">Microsoft. Azure. Commands. profile. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="954fe-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="954fe-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="954fe-124">NOTES</span></span>

## <span data-ttu-id="954fe-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="954fe-125">RELATED LINKS</span></span>
