---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 2836445eabc4b3986a548adf7013ceaa7e75dc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549303"
---
# <span data-ttu-id="312ef-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="312ef-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="312ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="312ef-102">SYNOPSIS</span></span>
<span data-ttu-id="312ef-103">Ustawia wartość domyślną w bieżącym kontekście</span><span class="sxs-lookup"><span data-stu-id="312ef-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="312ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="312ef-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="312ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="312ef-105">DESCRIPTION</span></span>
<span data-ttu-id="312ef-106">Polecenie cmdlet Set-AzureRmDefault powoduje dodanie lub zmianę wartości domyślnych w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="312ef-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="312ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="312ef-107">EXAMPLES</span></span>

### <span data-ttu-id="312ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="312ef-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="312ef-109">To polecenie ustawia domyślną grupę zasobów dla grupy zasobów określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="312ef-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="312ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="312ef-110">PARAMETERS</span></span>

### <span data-ttu-id="312ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312ef-111">-DefaultProfile</span></span>
<span data-ttu-id="312ef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="312ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312ef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="312ef-113">-Force</span></span>
<span data-ttu-id="312ef-114">Tworzenie nowej grupy zasobów, jeśli określona wartość domyślna nie istnieje</span><span class="sxs-lookup"><span data-stu-id="312ef-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="312ef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312ef-115">-ResourceGroupName</span></span>
<span data-ttu-id="312ef-116">Nazwa grupy zasobów ustawiana jako domyślna</span><span class="sxs-lookup"><span data-stu-id="312ef-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312ef-117">-Zakres</span><span class="sxs-lookup"><span data-stu-id="312ef-117">-Scope</span></span>
<span data-ttu-id="312ef-118">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="312ef-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312ef-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="312ef-119">-Confirm</span></span>
<span data-ttu-id="312ef-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="312ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="312ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="312ef-121">-WhatIf</span></span>
<span data-ttu-id="312ef-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="312ef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="312ef-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="312ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="312ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312ef-124">CommonParameters</span></span>
<span data-ttu-id="312ef-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="312ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312ef-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="312ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312ef-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="312ef-127">INPUTS</span></span>

### <span data-ttu-id="312ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="312ef-128">System.String</span></span>

## <span data-ttu-id="312ef-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="312ef-129">OUTPUTS</span></span>

### <span data-ttu-id="312ef-130">Microsoft. Azure. Commands. profile. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="312ef-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="312ef-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="312ef-131">NOTES</span></span>

## <span data-ttu-id="312ef-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="312ef-132">RELATED LINKS</span></span>
