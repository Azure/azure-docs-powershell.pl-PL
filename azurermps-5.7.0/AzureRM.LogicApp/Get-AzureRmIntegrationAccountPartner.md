---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 7063fb81705a14f1c1d8f0d02a2dc51d8a5617ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717740"
---
# <span data-ttu-id="1e924-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1e924-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="1e924-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e924-102">SYNOPSIS</span></span>
<span data-ttu-id="1e924-103">Umożliwia pobieranie partnerów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="1e924-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e924-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e924-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e924-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e924-105">DESCRIPTION</span></span>
<span data-ttu-id="1e924-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountPartner umożliwia otrzymywanie** partnerów kont integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e924-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="1e924-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="1e924-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="1e924-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="1e924-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1e924-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1e924-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1e924-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="1e924-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1e924-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="1e924-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1e924-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e924-112">EXAMPLES</span></span>

### <span data-ttu-id="1e924-113">Przykład 1: uzyskiwanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="1e924-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="1e924-114">To polecenie uzyskuje partnera kont integracji o nazwie IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="1e924-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="1e924-115">Przykład 2: uzyskiwanie partnerów z kontami integracyjnymi przy użyciu nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="1e924-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="1e924-116">To polecenie pobiera partnerów kont integracyjnych dla konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="1e924-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="1e924-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e924-117">PARAMETERS</span></span>

### <span data-ttu-id="1e924-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e924-118">-DefaultProfile</span></span>
<span data-ttu-id="1e924-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1e924-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e924-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e924-120">-Name</span></span>
<span data-ttu-id="1e924-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1e924-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e924-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="1e924-122">-PartnerName</span></span>
<span data-ttu-id="1e924-123">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="1e924-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e924-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e924-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e924-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e924-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e924-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e924-126">CommonParameters</span></span>
<span data-ttu-id="1e924-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e924-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e924-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e924-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e924-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e924-129">INPUTS</span></span>

### <span data-ttu-id="1e924-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1e924-130">None</span></span>
<span data-ttu-id="1e924-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1e924-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e924-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e924-132">OUTPUTS</span></span>

### <span data-ttu-id="1e924-133">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1e924-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="1e924-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e924-134">NOTES</span></span>

## <span data-ttu-id="1e924-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e924-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e924-136">Nowe — AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1e924-136">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="1e924-137">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1e924-137">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="1e924-138">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1e924-138">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


