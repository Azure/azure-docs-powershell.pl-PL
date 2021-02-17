---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190498"
---
# <span data-ttu-id="6cda1-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="6cda1-101">Get-AzDefault</span></span>

## <span data-ttu-id="6cda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cda1-102">SYNOPSIS</span></span>
<span data-ttu-id="6cda1-103">Pobierz ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="6cda1-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="6cda1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cda1-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cda1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cda1-105">DESCRIPTION</span></span>
<span data-ttu-id="6cda1-106">Polecenie Get-AzDefault pobiera grupę zasobów ustawioną przez użytkownika jako domyślną w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="6cda1-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="6cda1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cda1-107">EXAMPLES</span></span>

### <span data-ttu-id="6cda1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cda1-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="6cda1-109">To polecenie zwraca bieżące ustawienia domyślne, jeśli są ustawione wartości domyślne, lub nic, jeśli nie jest ustawione żadne ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="6cda1-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="6cda1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6cda1-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="6cda1-111">To polecenie zwraca bieżącą domyślną grupę zasobów, jeśli jest ustawiony domyślny, lub nic nie zwraca, jeśli nie jest ustawione żadne ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="6cda1-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="6cda1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cda1-112">PARAMETERS</span></span>

### <span data-ttu-id="6cda1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cda1-113">-DefaultProfile</span></span>
<span data-ttu-id="6cda1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cda1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cda1-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cda1-115">-ResourceGroup</span></span>
<span data-ttu-id="6cda1-116">Wyświetl domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="6cda1-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="6cda1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cda1-117">CommonParameters</span></span>
<span data-ttu-id="6cda1-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cda1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cda1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cda1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cda1-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cda1-120">INPUTS</span></span>

### <span data-ttu-id="6cda1-121">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="6cda1-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6cda1-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cda1-122">OUTPUTS</span></span>

### <span data-ttu-id="6cda1-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cda1-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="6cda1-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cda1-124">NOTES</span></span>

## <span data-ttu-id="6cda1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cda1-125">RELATED LINKS</span></span>
