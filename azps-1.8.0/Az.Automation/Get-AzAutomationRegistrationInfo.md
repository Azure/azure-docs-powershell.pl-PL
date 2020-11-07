---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: f915d1637226e7381cf7da53c0a3aea022060be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710572"
---
# <span data-ttu-id="cb94d-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="cb94d-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="cb94d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb94d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb94d-103">Pobiera informacje rejestracyjne dotyczące dołączania węzła DSC lub hybrydowego pracownika do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cb94d-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="cb94d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb94d-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb94d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cb94d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb94d-106">Polecenie cmdlet **Get-AzAutomationRegistrationInfo** Pobiera punkt końcowy i klucze wymagane do dołączania węzła konfiguracji stanu (DSC) lub hybrydowego pracownika do konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cb94d-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="cb94d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb94d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb94d-108">Przykład 1: uzyskiwanie informacji o rejestracji</span><span class="sxs-lookup"><span data-stu-id="cb94d-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="cb94d-109">To polecenie pobiera informacje rejestracyjne dla konta usługi Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cb94d-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="cb94d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb94d-110">PARAMETERS</span></span>

### <span data-ttu-id="cb94d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb94d-111">-AutomationAccountName</span></span>
<span data-ttu-id="cb94d-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera informacje rejestracyjne.</span><span class="sxs-lookup"><span data-stu-id="cb94d-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="cb94d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb94d-113">-DefaultProfile</span></span>
<span data-ttu-id="cb94d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cb94d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb94d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb94d-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb94d-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb94d-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cb94d-117">To polecenie cmdlet umożliwia pobieranie informacji o rejestracji dla grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cb94d-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb94d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb94d-118">CommonParameters</span></span>
<span data-ttu-id="cb94d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb94d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb94d-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb94d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb94d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb94d-121">INPUTS</span></span>

### <span data-ttu-id="cb94d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cb94d-122">System.String</span></span>

## <span data-ttu-id="cb94d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb94d-123">OUTPUTS</span></span>

### <span data-ttu-id="cb94d-124">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="cb94d-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="cb94d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb94d-125">NOTES</span></span>

## <span data-ttu-id="cb94d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb94d-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb94d-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb94d-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="cb94d-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cb94d-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cb94d-129">Nowe — AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="cb94d-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


