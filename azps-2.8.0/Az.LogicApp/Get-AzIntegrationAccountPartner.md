---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: c1f96d462d1556078159d70a47a9869ec21a0e63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705043"
---
# <span data-ttu-id="5659f-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="5659f-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="5659f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5659f-102">SYNOPSIS</span></span>
<span data-ttu-id="5659f-103">Umożliwia pobieranie partnerów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="5659f-103">Gets integration account partners.</span></span>

## <span data-ttu-id="5659f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5659f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5659f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5659f-105">DESCRIPTION</span></span>
<span data-ttu-id="5659f-106">Polecenie cmdlet **Get-AzIntegrationAccountPartner umożliwia otrzymywanie** partnerów kont integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5659f-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="5659f-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="5659f-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="5659f-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="5659f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5659f-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5659f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5659f-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5659f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5659f-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="5659f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5659f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5659f-112">EXAMPLES</span></span>

### <span data-ttu-id="5659f-113">Przykład 1: uzyskiwanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="5659f-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="5659f-114">To polecenie uzyskuje partnera kont integracji o nazwie IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="5659f-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="5659f-115">Przykład 2: uzyskiwanie partnerów z kontami integracyjnymi przy użyciu nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="5659f-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="5659f-116">To polecenie pobiera partnerów kont integracyjnych dla konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="5659f-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="5659f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5659f-117">PARAMETERS</span></span>

### <span data-ttu-id="5659f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5659f-118">-DefaultProfile</span></span>
<span data-ttu-id="5659f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5659f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5659f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5659f-120">-Name</span></span>
<span data-ttu-id="5659f-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5659f-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5659f-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="5659f-122">-PartnerName</span></span>
<span data-ttu-id="5659f-123">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="5659f-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="5659f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5659f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5659f-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5659f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5659f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5659f-126">CommonParameters</span></span>
<span data-ttu-id="5659f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5659f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5659f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5659f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5659f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5659f-129">INPUTS</span></span>

### <span data-ttu-id="5659f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5659f-130">System.String</span></span>

## <span data-ttu-id="5659f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5659f-131">OUTPUTS</span></span>

### <span data-ttu-id="5659f-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="5659f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="5659f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5659f-133">NOTES</span></span>

## <span data-ttu-id="5659f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5659f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5659f-135">Nowe — AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="5659f-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="5659f-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="5659f-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="5659f-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="5659f-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

