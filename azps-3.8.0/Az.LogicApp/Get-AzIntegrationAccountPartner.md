---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895133"
---
# <span data-ttu-id="e8dd0-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e8dd0-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="e8dd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dd0-103">Umożliwia pobieranie partnerów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-103">Gets integration account partners.</span></span>

## <span data-ttu-id="e8dd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8dd0-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8dd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dd0-106">Polecenie cmdlet **Get-AzIntegrationAccountPartner umożliwia otrzymywanie** partnerów kont integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="e8dd0-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="e8dd0-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e8dd0-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e8dd0-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e8dd0-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e8dd0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8dd0-112">EXAMPLES</span></span>

### <span data-ttu-id="e8dd0-113">Przykład 1: uzyskiwanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="e8dd0-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="e8dd0-114">To polecenie uzyskuje partnera kont integracji o nazwie IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="e8dd0-115">Przykład 2: uzyskiwanie partnerów z kontami integracyjnymi przy użyciu nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="e8dd0-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="e8dd0-116">To polecenie pobiera partnerów kont integracyjnych dla konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="e8dd0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8dd0-117">PARAMETERS</span></span>

### <span data-ttu-id="e8dd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8dd0-118">-DefaultProfile</span></span>
<span data-ttu-id="e8dd0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e8dd0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8dd0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8dd0-120">-Name</span></span>
<span data-ttu-id="e8dd0-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd0-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="e8dd0-122">-PartnerName</span></span>
<span data-ttu-id="e8dd0-123">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8dd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8dd0-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e8dd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dd0-126">CommonParameters</span></span>
<span data-ttu-id="e8dd0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8dd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dd0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8dd0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dd0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8dd0-129">INPUTS</span></span>

### <span data-ttu-id="e8dd0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8dd0-130">System.String</span></span>

## <span data-ttu-id="e8dd0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8dd0-131">OUTPUTS</span></span>

### <span data-ttu-id="e8dd0-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e8dd0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="e8dd0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8dd0-133">NOTES</span></span>

## <span data-ttu-id="e8dd0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8dd0-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8dd0-135">Nowe — AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e8dd0-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="e8dd0-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e8dd0-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="e8dd0-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e8dd0-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


