---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 20d66412002e8feb1b4007608091cdbf0422b6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551692"
---
# <span data-ttu-id="06c50-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="06c50-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="06c50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06c50-102">SYNOPSIS</span></span>
<span data-ttu-id="06c50-103">Uzyskiwanie wartości domyślnych ustawionych przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="06c50-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06c50-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06c50-105">DESCRIPTION</span></span>
<span data-ttu-id="06c50-106">Polecenie cmdlet Get-AzureRmDefault pobiera grupę zasobów, którą Użytkownik ustawił jako domyślny w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="06c50-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="06c50-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06c50-107">EXAMPLES</span></span>

### <span data-ttu-id="06c50-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06c50-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="06c50-109">To polecenie zwraca bieżące ustawienia domyślne, jeśli są ustawione wartości domyślne, lub zwraca wartość Nothing, jeśli nie ustawiono żadnego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="06c50-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="06c50-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06c50-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="06c50-111">To polecenie zwraca bieżącą domyślną grupę zasobów, jeśli jest ustawiona wartość domyślna, lub zwraca wartość Nothing, jeśli nie ustawiono żadnego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="06c50-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="06c50-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06c50-112">PARAMETERS</span></span>

### <span data-ttu-id="06c50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c50-113">-DefaultProfile</span></span>
<span data-ttu-id="06c50-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06c50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c50-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06c50-115">-ResourceGroup</span></span>
<span data-ttu-id="06c50-116">Wyświetl domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="06c50-116">Display Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c50-117">CommonParameters</span></span>
<span data-ttu-id="06c50-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06c50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c50-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c50-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c50-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06c50-120">INPUTS</span></span>

### <span data-ttu-id="06c50-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="06c50-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="06c50-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06c50-122">OUTPUTS</span></span>

### <span data-ttu-id="06c50-123">Microsoft. Azure. Management. Internal. zasoby. MODELES. resourceing.</span><span class="sxs-lookup"><span data-stu-id="06c50-123">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="06c50-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06c50-124">NOTES</span></span>

## <span data-ttu-id="06c50-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06c50-125">RELATED LINKS</span></span>

