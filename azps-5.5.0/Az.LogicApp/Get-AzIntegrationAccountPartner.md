---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192291"
---
# <span data-ttu-id="ad03a-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad03a-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="ad03a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad03a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad03a-103">Otrzymuje partnerów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="ad03a-103">Gets integration account partners.</span></span>

## <span data-ttu-id="ad03a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad03a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad03a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad03a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad03a-106">Polecenie **cmdlet Get-AzIntegrationAccountPartner** pobiera partnerów konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad03a-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="ad03a-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="ad03a-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="ad03a-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ad03a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad03a-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ad03a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad03a-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="ad03a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad03a-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="ad03a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad03a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad03a-112">EXAMPLES</span></span>

### <span data-ttu-id="ad03a-113">Przykład 1. Uzyskiwanie partnera konta integracji</span><span class="sxs-lookup"><span data-stu-id="ad03a-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="ad03a-114">To polecenie pobiera partnera konta integracji o nazwie IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="ad03a-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="ad03a-115">Przykład 2. Uzyskiwanie partnerów konta integracji przy użyciu nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="ad03a-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="ad03a-116">To polecenie pobiera partnerów kont integracji dla konta integracji o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="ad03a-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="ad03a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad03a-117">PARAMETERS</span></span>

### <span data-ttu-id="ad03a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad03a-118">-DefaultProfile</span></span>
<span data-ttu-id="ad03a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ad03a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad03a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad03a-120">-Name</span></span>
<span data-ttu-id="ad03a-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad03a-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ad03a-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="ad03a-122">-PartnerName</span></span>
<span data-ttu-id="ad03a-123">Określa nazwę partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad03a-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="ad03a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad03a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad03a-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad03a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad03a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad03a-126">CommonParameters</span></span>
<span data-ttu-id="ad03a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad03a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad03a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad03a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad03a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad03a-129">INPUTS</span></span>

### <span data-ttu-id="ad03a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ad03a-130">System.String</span></span>

## <span data-ttu-id="ad03a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad03a-131">OUTPUTS</span></span>

### <span data-ttu-id="ad03a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad03a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="ad03a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad03a-133">NOTES</span></span>

## <span data-ttu-id="ad03a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad03a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad03a-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad03a-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="ad03a-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad03a-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="ad03a-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad03a-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


