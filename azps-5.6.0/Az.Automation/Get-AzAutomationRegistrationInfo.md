---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: aaa4a87f14572650fb0c1f969c11f0a3ed9cf0e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014298"
---
# <span data-ttu-id="b15ad-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="b15ad-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="b15ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b15ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b15ad-103">Pobiera informacje o rejestracji na temat dołączania węzła DSC lub pracownika hybrydowego do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b15ad-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="b15ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b15ad-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b15ad-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b15ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b15ad-106">Polecenie **cmdlet Get-AzAutomationRegistrationInfo** pobiera punkt końcowy i klucze wymagane do do ustawienia węzła lub pracownika hybrydowego żądanej konfiguracji województwa do konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b15ad-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="b15ad-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b15ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b15ad-108">Przykład 1. Uzyskiwanie informacji o rejestracji</span><span class="sxs-lookup"><span data-stu-id="b15ad-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="b15ad-109">To polecenie pobiera informacje rejestracji dla konta automatyzacji o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b15ad-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="b15ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b15ad-110">PARAMETERS</span></span>

### <span data-ttu-id="b15ad-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b15ad-111">-AutomationAccountName</span></span>
<span data-ttu-id="b15ad-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera informacje o rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b15ad-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b15ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15ad-113">-DefaultProfile</span></span>
<span data-ttu-id="b15ad-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b15ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b15ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="b15ad-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b15ad-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b15ad-117">To polecenie cmdlet pobiera informacje o rejestracji dla grupy zasobów, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b15ad-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b15ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15ad-118">CommonParameters</span></span>
<span data-ttu-id="b15ad-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b15ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15ad-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b15ad-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15ad-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b15ad-121">INPUTS</span></span>

### <span data-ttu-id="b15ad-122">System.String</span><span class="sxs-lookup"><span data-stu-id="b15ad-122">System.String</span></span>

## <span data-ttu-id="b15ad-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b15ad-123">OUTPUTS</span></span>

### <span data-ttu-id="b15ad-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="b15ad-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="b15ad-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b15ad-125">NOTES</span></span>

## <span data-ttu-id="b15ad-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b15ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="b15ad-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b15ad-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="b15ad-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b15ad-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="b15ad-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="b15ad-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


