---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 84332967eadfdb2accd12cc2f6f840ee337f92ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526346"
---
# <span data-ttu-id="b35b6-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="b35b6-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="b35b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b35b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b35b6-103">Pobiera informacje rejestracyjne dotyczące dołączania węzła DSC lub hybrydowego pracownika do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b35b6-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b35b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b35b6-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b35b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b35b6-105">DESCRIPTION</span></span>
<span data-ttu-id="b35b6-106">Polecenie cmdlet **Get-AzureRmAutomationRegistrationInfo** Pobiera punkt końcowy i klucze wymagane do dołączania węzła konfiguracji stanu (DSC) lub hybrydowego pracownika do konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b35b6-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="b35b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b35b6-107">EXAMPLES</span></span>

### <span data-ttu-id="b35b6-108">Przykład 1: uzyskiwanie informacji o rejestracji</span><span class="sxs-lookup"><span data-stu-id="b35b6-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="b35b6-109">To polecenie pobiera informacje rejestracyjne dla konta usługi Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b35b6-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="b35b6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b35b6-110">PARAMETERS</span></span>

### <span data-ttu-id="b35b6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b35b6-111">-AutomationAccountName</span></span>
<span data-ttu-id="b35b6-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera informacje rejestracyjne.</span><span class="sxs-lookup"><span data-stu-id="b35b6-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="b35b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35b6-113">-DefaultProfile</span></span>
<span data-ttu-id="b35b6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b35b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b35b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="b35b6-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b35b6-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b35b6-117">To polecenie cmdlet umożliwia pobieranie informacji o rejestracji dla grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b35b6-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35b6-118">CommonParameters</span></span>
<span data-ttu-id="b35b6-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35b6-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b35b6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35b6-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35b6-121">INPUTS</span></span>

### <span data-ttu-id="b35b6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b35b6-122">System.String</span></span>

## <span data-ttu-id="b35b6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b35b6-123">OUTPUTS</span></span>

### <span data-ttu-id="b35b6-124">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="b35b6-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="b35b6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b35b6-125">NOTES</span></span>

## <span data-ttu-id="b35b6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b35b6-126">RELATED LINKS</span></span>

[<span data-ttu-id="b35b6-127">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b35b6-127">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="b35b6-128">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b35b6-128">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b35b6-129">Nowe — AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="b35b6-129">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)

