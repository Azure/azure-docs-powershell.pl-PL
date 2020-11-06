---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524406"
---
# <span data-ttu-id="adaa3-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="adaa3-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="adaa3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="adaa3-103">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="adaa3-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adaa3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adaa3-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adaa3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="adaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="adaa3-106">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="adaa3-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="adaa3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adaa3-107">EXAMPLES</span></span>

### <span data-ttu-id="adaa3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adaa3-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="adaa3-109">Tworzenie obiektu RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="adaa3-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="adaa3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adaa3-110">PARAMETERS</span></span>

### <span data-ttu-id="adaa3-111">-Action</span><span class="sxs-lookup"><span data-stu-id="adaa3-111">-Action</span></span>
<span data-ttu-id="adaa3-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="adaa3-112">Type of Actions.</span></span>
<span data-ttu-id="adaa3-113">Możliwe wartości obejmują: "dozwolone", "Zablokuj", "log".</span><span class="sxs-lookup"><span data-stu-id="adaa3-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaa3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaa3-114">-DefaultProfile</span></span>
<span data-ttu-id="adaa3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="adaa3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adaa3-116">-Override</span><span class="sxs-lookup"><span data-stu-id="adaa3-116">-Override</span></span>
<span data-ttu-id="adaa3-117">W tym artykule opisano overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="adaa3-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="adaa3-118">Możliwe wartości obejmują: "sqliniekcja", "XSS"</span><span class="sxs-lookup"><span data-stu-id="adaa3-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaa3-119">CommonParameters</span></span>
<span data-ttu-id="adaa3-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adaa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaa3-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adaa3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaa3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adaa3-122">INPUTS</span></span>

### <span data-ttu-id="adaa3-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="adaa3-123">None</span></span>

## <span data-ttu-id="adaa3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adaa3-124">OUTPUTS</span></span>

### <span data-ttu-id="adaa3-125">Microsoft. Azure. Commands. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="adaa3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="adaa3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adaa3-126">NOTES</span></span>

## <span data-ttu-id="adaa3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adaa3-127">RELATED LINKS</span></span>

[<span data-ttu-id="adaa3-128">Nowe — AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="adaa3-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
